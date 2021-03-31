---
title: C-definições de compilador para proxy/stubs
description: O arquivo de cabeçalho RpcProxy. h inclui as seguintes definições de macro, e cada uma delas pode ser conveniente ao criar um aplicativo COM distribuído. Essas macros são invocadas com a opção de pré-processador/D (ou-D) no momento da compilação C.
ms.assetid: 697f0b63-76ae-410d-8bbf-bb95295ffba9
keywords:
- MIDL do compilador MIDL, C-Compiler, definições para proxy/stubs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1504c600c3f86a934ab3daa132b041c7310af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005914"
---
# <a name="c-compiler-definitions-for-proxystubs"></a><span data-ttu-id="8f5ff-105">C-definições de compilador para proxy/stubs</span><span class="sxs-lookup"><span data-stu-id="8f5ff-105">C-Compiler Definitions for Proxy/Stubs</span></span>

<span data-ttu-id="8f5ff-106">O arquivo de cabeçalho RpcProxy. h inclui as seguintes definições de macro, e cada uma delas pode ser conveniente ao criar um aplicativo COM distribuído.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-106">The header file Rpcproxy.h includes the following macro definitions, each of which may be convenient when building distributed COM application.</span></span> <span data-ttu-id="8f5ff-107">Essas macros são invocadas com a opção de pré-processador [**/d**](-d.md) (ou-D) no momento da compilação C.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-107">These macros are invoked with the [**/D**](-d.md) (or -D) preprocessor switch at the C-compile time.</span></span>



| <span data-ttu-id="8f5ff-108">MACRO</span><span class="sxs-lookup"><span data-stu-id="8f5ff-108">MACRO</span></span>                                                                                                                                                                                           | <span data-ttu-id="8f5ff-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f5ff-109">Description</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f5ff-110">REGISTRAR \_ dll de proxy \_</span><span class="sxs-lookup"><span data-stu-id="8f5ff-110">REGISTER\_PROXY\_DLL</span></span>                                                                                                                                                                            | <span data-ttu-id="8f5ff-111">Gera as funções **DllMain**, **DllRegisterServer** e **DLLUNREGISTERSERVER** para registrar automaticamente uma DLL de proxy.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-111">Generates **DllMain**, **DllRegisterServer**, and **DllUnregisterServer** functions for automatically registering a proxy DLL.</span></span>                                                                                       |
| <span data-ttu-id="8f5ff-112">CLSID do PROXY \_ =<clsid></span><span class="sxs-lookup"><span data-stu-id="8f5ff-112">PROXY\_CLSID=<clsid></span></span>                                                                                                                                                                      | <span data-ttu-id="8f5ff-113">Especifica um identificador de classe para o servidor.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-113">Specifies a class identifier for the server.</span></span> <span data-ttu-id="8f5ff-114">Se essa macro não estiver definida, o CLSID padrão será o primeiro identificador de interface que o compilador MIDL encontrará na especificação IDL do servidor proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-114">If this macro is not defined, the default CLSID is the first interface identifier that the MIDL compiler encounters in the IDL specification for the Proxy/Stub server.</span></span> |
| <span data-ttu-id="8f5ff-115">CLSID de PROXY \_ \_ é = {0x *8hexdigits*,*0x 4hexdigits*, 0x *4hexdigits*, {0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*,}}</span><span class="sxs-lookup"><span data-stu-id="8f5ff-115">PROXY\_CLSID\_IS={0x *8hexdigits*, 0x *4hexdigits*,0x *4hexdigits*, {0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*,}}</span></span> | <span data-ttu-id="8f5ff-116">Especifica o valor do identificador de classe do servidor no formato hexadecimal binário.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-116">Specifies the value of the server's class identifier in binary hex format.</span></span>                                                                                                                                           |



 

<span data-ttu-id="8f5ff-117">Ao definir a macro da **\_ \_ dll do proxy de registro** ao compilar dlldata. c, sua DLL de marshaling de proxy/stub incluirá automaticamente as definições padrão para as funções **DllMain**, **DllRegisterServer** e **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="8f5ff-117">By defining the **REGISTER\_PROXY\_DLL** macro when compiling Dlldata.c, your proxy/stub marshaling DLL will automatically include default definitions for the **DllMain**, **DllRegisterServer**, and **DllUnregisterServer** functions.</span></span> <span data-ttu-id="8f5ff-118">Você pode usar essas funções para registrar automaticamente sua DLL de proxy no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-118">You can use these functions to self-register your proxy DLL in the system registry.</span></span>

<span data-ttu-id="8f5ff-119">Esse código de registro padrão usa o GUID da primeira interface encontrado como o CLSID para registrar todo o servidor DLL de proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-119">This default registration code uses the GUID of the first interface encountered as the CLSID for registering the entire proxy/stub DLL server.</span></span> <span data-ttu-id="8f5ff-120">O COM mais tarde usa esse CLSID para localizar e carregar o servidor proxy/stub compilado para o marshaling de qualquer uma das interfaces que o servidor está registrado para manipular.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-120">COM later uses this CLSID to locate and load the compiled proxy/stub server for the marshaling of any of the interfaces the server is registered to handle.</span></span> <span data-ttu-id="8f5ff-121">Quando um aplicativo faz uma chamada de método de interface que cruza os limites do thread, do processo ou do computador, COM usa a entrada do registro do identificador de interface para localizar a entrada do Registro CLSID para o servidor de marshaling do proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-121">When an application makes an interface method call that crosses thread, process, or computer boundaries, COM uses the interface identifier registry entry to locate the CLSID registry entry for the proxy/stub marshaling server.</span></span> <span data-ttu-id="8f5ff-122">Em seguida, ele usa esse CLSID para carregar o servidor (se ele ainda não estiver carregado) para que a chamada de interface possa ser empacotada.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-122">It then uses this CLSID to load the server (if it isn't already loaded) so that the interface call can then be marshaled.</span></span>

<span data-ttu-id="8f5ff-123">Use a **macro \_ CLSID do proxy** = <clsid> quando desejar especificar explicitamente o CLSID do servidor de proxy/stub em vez de confiar no CLSID padrão.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-123">Use the **PROXY\_CLSID**=<clsid> macro when you want to explicitly specify the proxy/stub server's CLSID rather than rely on the default CLSID.</span></span> <span data-ttu-id="8f5ff-124">Por exemplo, se você estiver criando uma DLL de marshaling padrão como seu próprio servidor COM em processo, ou se precisar definir seu próprio **DllMain** para manipular a \_ anexação do processo de dll \_ .</span><span class="sxs-lookup"><span data-stu-id="8f5ff-124">For example, if you are building a standard marshaling DLL as your own in-process COM server, or if you need to define your own **DllMain** to handle DLL\_PROCESS\_ATTACH.</span></span>

<span data-ttu-id="8f5ff-125">Use **CLSID de proxy \_ \_ é**= macro em vez de **\_ CLSID de proxy** para definir o valor do CLSID no formato hexadecimal binário que a macro **define \_ GUID** usa.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-125">Use **PROXY\_CLSID\_IS**= macro instead of **PROXY\_CLSID** to define the value of the CLSID in the binary hexadecimal format that the **DEFINE\_GUID** macro uses.</span></span>

<span data-ttu-id="8f5ff-126">Observe também que, quando a função **DllRegisterServer** padrão é executada, ela registra o servidor com ThreadingModel = both.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-126">Also note that when the default **DllRegisterServer** function runs, it registers the server with ThreadingModel=Both.</span></span>

<span data-ttu-id="8f5ff-127">O exemplo de makefile a seguir usa a **\_ \_ dll de registro de proxy** e o **proxy \_ CLSID**= macros:</span><span class="sxs-lookup"><span data-stu-id="8f5ff-127">The following makefile example uses the **REGISTER\_PROXY\_DLL** and **PROXY\_CLSID**= macros:</span></span>

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL \
    /DPROXY_CLSID=7a98c250-6808-11cf-b73b-00aa00b677a7
example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
```

<span data-ttu-id="8f5ff-128">Para obter mais informações sobre a opção [**/d**](-d.md) pré-processador, consulte a documentação do compilador do C.</span><span class="sxs-lookup"><span data-stu-id="8f5ff-128">For more information on the [**/D**](-d.md) preprocessor option, see your C compiler documentation.</span></span>

 

 




