---
title: Criando e registrando uma DLL de proxy
description: Se você escolher marshaling de proxy/stub para seu aplicativo, os arquivos. c e. h que o MIDL gerado devem ser compilados e vinculados para criar uma DLL de proxy, e essa DLL deve ser inserida no registro do sistema para que os clientes possam localizar suas interfaces.
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b0dcd28359172ff2f90391d44a66f8f51a4cbf
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641903"
---
# <a name="building-and-registering-a-proxy-dll"></a><span data-ttu-id="758f7-103">Criando e registrando uma DLL de proxy</span><span class="sxs-lookup"><span data-stu-id="758f7-103">Building and Registering a Proxy DLL</span></span>

<span data-ttu-id="758f7-104">Se você escolher marshaling de proxy/stub para seu aplicativo, os arquivos. c e. h que o MIDL gerado devem ser compilados e vinculados para criar uma DLL de proxy, e essa DLL deve ser inserida no registro do sistema para que os clientes possam localizar suas interfaces.</span><span class="sxs-lookup"><span data-stu-id="758f7-104">If you chose proxy/stub marshaling for your application, the .c and .h files that MIDL generated must be compiled and linked to create a proxy DLL, and that DLL must be entered into the system registry so that clients can locate your interfaces.</span></span> <span data-ttu-id="758f7-105">O arquivo gerado pelo MIDL dlldata. c contém as rotinas necessárias e outras informações para compilar e registrar uma DLL de proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="758f7-105">The MIDL-generated file Dlldata.c contains the necessary routines and other information to build and register a proxy/stub DLL.</span></span>

<span data-ttu-id="758f7-106">A primeira etapa na criação da DLL é gravar um arquivo de definição de módulo para o vinculador, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="758f7-106">The first step in building the DLL is to write a module definition file for the linker, as shown in the following example:</span></span>

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

<span data-ttu-id="758f7-107">Como alternativa, você pode especificar essas funções exportadas na linha de comando do LINK do makefile.</span><span class="sxs-lookup"><span data-stu-id="758f7-107">Alternatively, you can specify these exported functions on the LINK command line of your makefile.</span></span>

<span data-ttu-id="758f7-108">As funções exportadas são declaradas em RpcProxy. h, que dlldata. c inclui, e as implementações padrão fazem parte da biblioteca de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="758f7-108">The exported functions are declared in Rpcproxy.h, which Dlldata.c includes, and default implementations are part of the RPC run-time library.</span></span> <span data-ttu-id="758f7-109">COM usa essas funções para criar uma fábrica de classes, descarregar DLLs (depois de certificar-se de que não existam objetos ou bloqueios), recuperar informações sobre a DLL de proxy e registrar em Autoregistro e cancelar o registro da DLL de proxy.</span><span class="sxs-lookup"><span data-stu-id="758f7-109">COM uses these functions to create a class factory, unload DLLs (after making sure that no objects or locks exist), retrieve information about the proxy DLL, and to self-register and unregister the proxy DLL.</span></span> <span data-ttu-id="758f7-110">Para aproveitar essas funções predefinidas, você precisa invocar a opção Cpreprocessor/D (ou-D) ao compilar os arquivos dlldata. c e example \_ p. c, conforme mostrado no seguinte makefile:</span><span class="sxs-lookup"><span data-stu-id="758f7-110">To take advantage of these predefined functions, you need to invoke the Cpreprocessor /D (or -D) option when you compile the Dlldata.c and Example\_p.c files, as shown in the following makefile:</span></span>

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcndr.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(ORIXYSTUBLIBS)
    regsvr32 /s proxy.dll
 
```

<span data-ttu-id="758f7-111">Se você não especificar essas definições de pré-processador em tempo de compilação, essas funções não serão definidas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="758f7-111">If you do not specify these preprocessor definitions at compile time, these functions are not automatically defined.</span></span> <span data-ttu-id="758f7-112">(Ou seja, as macros em RpcProxy. c expandem para Nothing.) Você precisaria defini-las explicitamente em outro arquivo de origem, cujo módulo também seria incluído na vinculação e compilação final na linha de comando do compilador C.</span><span class="sxs-lookup"><span data-stu-id="758f7-112">(That is, the macros in Rpcproxy.c expand to nothing.) You would have to have defined them explicitly in another source file, whose module would also be included in the final linking and compilation on the C compiler command line.</span></span>

<span data-ttu-id="758f7-113">Quando o \_ registro \_ dll de proxy é definido, o RpcProxy. h fornece um controle de compilação condicional adicional com proxy \_ CLSID =*GUID*, proxy \_ CLSID \_ é =*valor explícito de GUID* e prefixo de entrada \_ =*cadeia de caracteres de prefixo*.</span><span class="sxs-lookup"><span data-stu-id="758f7-113">When REGISTER\_PROXY\_DLL is defined, Rpcproxy.h provides for additional conditional compilation control with PROXY\_CLSID=*guid*, PROXY\_CLSID\_IS=*explicit value of guid*, and ENTRY\_PREFIX=*prefix string*.</span></span> <span data-ttu-id="758f7-114">Essas definições de macro são descritas mais detalhadamente em [definições de compilador C para proxy/stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) no guia do programador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="758f7-114">These macro definitions are described in greater detail in [C-Compiler Definitions for Proxy/Stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) in the MIDL Programmer's Guide.</span></span>

## <a name="manually-registering-the-proxy-dll"></a><span data-ttu-id="758f7-115">Registrando manualmente a DLL de proxy</span><span class="sxs-lookup"><span data-stu-id="758f7-115">Manually Registering the Proxy DLL</span></span>

<span data-ttu-id="758f7-116">Se, por alguma razão, você não puder usar as rotinas de registro de stub de proxy padrão, poderá registrar manualmente a DLL adicionando as seguintes entradas ao registro do sistema, usando Regedt32.exe.</span><span class="sxs-lookup"><span data-stu-id="758f7-116">If for some reason you cannot use the default proxy stub registration routines, you can manually register the DLL by adding the following entries to the system registry, using Regedt32.exe.</span></span>

```
HKEY_CLASSES_ROOT
   Interface
      iid
         (Default) = ICustomInterfaceName
         ProxyStubClsid32 = {clsid}
```

```
HKEY_CLASSES_ROOT
   CLSID
      clsid
         (Default) = ICustomInterfaceName_PSFactory
         InprocServer32 = proxstub.dll
```

## <a name="related-topics"></a><span data-ttu-id="758f7-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="758f7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="758f7-118">C-definições de compilador para proxy/stubs</span><span class="sxs-lookup"><span data-stu-id="758f7-118">C-Compiler Definitions for Proxy/Stubs</span></span>](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[<span data-ttu-id="758f7-119">Registrando servidores COM</span><span class="sxs-lookup"><span data-stu-id="758f7-119">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="758f7-120">Registro automático</span><span class="sxs-lookup"><span data-stu-id="758f7-120">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 