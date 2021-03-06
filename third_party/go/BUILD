package(default_visibility = ['PUBLIC'])

go_get(
    name = 'logging',
    get = 'gopkg.in/op/go-logging.v1',
    revision = 'b2cb9fa56473e98db8caba80237377e83fe44db5',
)

go_get(
    name = 'terminal',
    get = 'golang.org/x/crypto/ssh/terminal',
    revision = '7b85b097bf7527677d54d3220065e966a0e3b613',
)

go_get(
    name = 'cover',
    get = 'golang.org/x/tools/cover',
    revision = 'c0008c5889c0d5091cdfefd2bfb08bff96527879',
)

go_get(
    name = 'gcfg',
    get = 'gopkg.in/gcfg.v1',
    patch = 'gcfg_dynamic_fields.patch',
    revision = '27e4946190b4a327b539185f2b5b1f7c84730728',
)

go_get(
    name = 'go-bindata',
    binary = True,
    get = 'github.com/jteeuwen/go-bindata/...',
    revision = 'a0ff2567cfb70903282db057e799fd826784d41d',
)

go_get(
    name = 'go-flags',
    get = 'github.com/jessevdk/go-flags',
    patch = 'flags_subcommand.patch',
    revision = '5695738f733662da3e9afc2283bba6f3c879002d',
)

go_get(
    name = 'humanize',
    get = 'github.com/dustin/go-humanize',
    revision = '8929fe90cee4b2cb9deb468b51fb34eba64d1bf0',
)

go_get(
    name = 'mux',
    get = 'github.com/gorilla/mux',
    revision = '9c068cf16d982f8bd444b8c352acbeec34c4fe5b',
    deps = [
        ':gorilla_context',
    ],
)

go_get(
    name = 'gorilla_context',
    get = 'github.com/gorilla/context',
    revision = '1c83b3eabd45b6d76072b66b746c20815fb2872d',
)

go_get(
    name = 'context',
    get = 'golang.org/x/net/context',
    revision = '57efc9c3d9f91fb3277f8da1cff370539c4d3dc5',
)

go_get(
    name = 'grpc',
    exported_deps = [':context'],
    get = 'google.golang.org/grpc',
    install = ['google.golang.org/grpc/health'],
    revision = 'v1.7.0',
    deps = [':protobuf'],
)

go_get(
    name = 'protobuf',
    get = 'github.com/golang/protobuf/ptypes',
    install = ['github.com/golang/protobuf/protoc-gen-go/descriptor'],
    revision = '130e6b02ab059e7b717a096f397c5b60111cae74',
)

go_get(
    name = 'protoc-gen-go',
    binary = True,
    get = 'github.com/golang/protobuf/protoc-gen-go',
    revision = '130e6b02ab059e7b717a096f397c5b60111cae74',
    deps = [
        ':protobuf',
    ],
)

go_get(
    name = 'testify',
    get = 'github.com/stretchr/testify',
    install = ['github.com/stretchr/testify/require'],
    revision = 'f390dcf405f7b83c997eac1b06768bb9f44dec18',
)

go_get(
    name = 'osext',
    get = 'github.com/kardianos/osext',
    revision = '29ae4ffbc9a6fe9fb2bc5029050ce6996ea1d3bc',
)

go_get(
    name = 'prompter',
    get = 'github.com/Songmu/prompter',
    revision = 'f49666b0047d12850875d771340e1d862d9e7a0c',
    deps = [
        ':terminal',
    ],
)

go_get(
    name = 'stringer',
    binary = True,
    get = 'golang.org/x/tools/cmd/stringer',
    revision = 'f8ecfdb6b66ec67ca930b39806519a2b72d1eaca',
)

go_get(
    name = 'levenshtein',
    get = 'github.com/texttheater/golang-levenshtein/levenshtein',
    revision = '14026fface0cb806188c85e792a93d625dc37d0f',
)

go_get(
    name = 'queue',
    get = 'github.com/Workiva/go-datastructures/queue',
    revision = '064f3ea06ab2337e6eaf42052392d14f779e91cb',
)

go_get(
    name = 'fsnotify',
    get = 'github.com/fsnotify/fsnotify',
    revision = 'a8a77c9133d2d6fd8334f3260d06f60e8d80a5fb',
    deps = [':unix'],
)

go_get(
    name = 'concurrent-map',
    get = 'github.com/streamrail/concurrent-map',
    revision = '5fc745307dc80a1883243b978f7e7c0fd5ce7206',
)

go_get(
    name = 'prometheus',
    get = 'github.com/prometheus/client_golang/prometheus',
    install = ['github.com/prometheus/client_golang/prometheus/push'],
    revision = 'c5b7fccd204277076155f10851dad72b76a49317',
    deps = [
        ':grpc',
        ':procfs',
        ':protobuf',
    ],
)

go_get(
    name = 'procfs',
    get = 'github.com/prometheus/procfs',
    revision = 'abf152e5f3e97f2fafac028d2cc06c1feb87ffa5',
    strip = ['fixtures'],  # Test fixture has a symlink to /usr/bin/vim which might not exist
)

go_get(
    name = 'grpc-prometheus',
    get = 'github.com/grpc-ecosystem/go-grpc-prometheus',
    revision = '34abd90a014618f61222a1b0a7b7eb834a2d0dc3',
    deps = [
        ':grpc',
        ':procfs',
        ':prometheus',
        ':protobuf',
    ],
)

go_get(
    name = 'grpc-middleware',
    get = 'github.com/grpc-ecosystem/go-grpc-middleware',
    revision = 'f63a7dfb64c138bd93d5c5b896d8b33c4b08e000',
    deps = [
        ':context',
        ':grpc',
        ':protobuf',
    ],
)

go_get(
    name = 'shlex',
    get = 'github.com/google/shlex',
    revision = '6f45313302b9c56850fc17f99e40caebce98c716',
)

go_get(
    name = 'semver',
    get = 'github.com/coreos/go-semver/semver',
    revision = '8ab6407b697782a06568d4b7f1db25550ec2e4c6',
)

go_get(
    name = 'memberlist',
    get = 'github.com/hashicorp/memberlist',
    revision = '7ad712f5f34ec40aebe6ca47756d07898486a8d2',
)

go_get(
    name = 'atime',
    get = 'github.com/djherbis/atime',
    revision = '89517e96e10b93292169a79fd4523807bdc5d5fa',
)

go_get(
    name = 'errgroup',
    get = 'golang.org/x/sync/errgroup',
    revision = '457c5828408160d6a47e17645169cf8fa20218c4',
    deps = [':context'],
)

go_get(
    name = 'html',
    get = 'golang.org/x/net/html',
    revision = '66aacef3dd8a676686c7ae3716979581e8b03c47',
)

go_get(
    name = 'psutil',
    get = 'github.com/shirou/gopsutil',
    install = [
        'github.com/shirou/gopsutil/cpu',
        'github.com/shirou/gopsutil/mem',
    ],
    revision = 'v2.17.09',
    deps = [':unix'],
)

go_get(
    name = 'unix',
    get = 'golang.org/x/sys/unix',
    revision = 'ebfc5b4631820b793c9010c87fd8fef0f39eb082',
)

go_get(
    name = 'openpgp',
    get = 'golang.org/x/crypto/openpgp',
    revision = '077efaa604f994162e3307fafe5954640763fc08',
)
