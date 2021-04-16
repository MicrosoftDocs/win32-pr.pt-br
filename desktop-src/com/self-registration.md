---
title: Self-Registration
description: O auto-registro é o meio padrão pelo qual um módulo de servidor pode empacotar suas próprias operações de registro, registro e cancelamento de registro, no próprio módulo.
ms.assetid: fb5dcb2b-b0e3-4f37-a8e7-b84b9a265227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c95d422213b8e33ac89b89408ed95724f0769b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454374"
---
# <a name="self-registration"></a><span data-ttu-id="ba04d-103">Self-Registration</span><span class="sxs-lookup"><span data-stu-id="ba04d-103">Self-Registration</span></span>

<span data-ttu-id="ba04d-104">À medida que o software do componente continua crescendo como um mercado, haverá mais e mais instâncias em que um usuário Obtém um novo componente de software como um único módulo DLL ou EXE, como ao baixar um novo componente de um serviço online ou receber um de um amigo em um disquete.</span><span class="sxs-lookup"><span data-stu-id="ba04d-104">As component software continues to grow as a market, there will be more and more instances where a user obtains a new software component as a single DLL or EXE module, such as when downloading a new component from an on-line service or receiving one from a friend on a floppy disk.</span></span> <span data-ttu-id="ba04d-105">Nesses casos, não é prático exigir que o usuário passe por um procedimento de instalação demorado ou programa de instalação.</span><span class="sxs-lookup"><span data-stu-id="ba04d-105">In these cases, it is not practical to require the user to go through a lengthy installation procedure or setup program.</span></span> <span data-ttu-id="ba04d-106">Além dos problemas de licenciamento, que são manipulados por meio do [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), um procedimento de instalação normalmente cria as entradas de Registro necessárias para que um componente seja executado corretamente no contexto com e OLE.</span><span class="sxs-lookup"><span data-stu-id="ba04d-106">Besides the licensing issues, which are handled through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), an installation procedure typically creates the necessary registry entries for a component to run properly in the COM and OLE context.</span></span>

<span data-ttu-id="ba04d-107">O auto-registro é o meio padrão pelo qual um módulo de servidor pode empacotar suas próprias operações de registro, registro e cancelamento de registro, no próprio módulo.</span><span class="sxs-lookup"><span data-stu-id="ba04d-107">Self-registration is the standard means through which a server module can package its own registry operations, both registration and unregistration, into the module itself.</span></span> <span data-ttu-id="ba04d-108">Quando usado com licenciamento manipulado por meio de [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), um servidor pode se tornar um módulo totalmente independente, sem a necessidade de programas de instalação externos ou arquivos. reg.</span><span class="sxs-lookup"><span data-stu-id="ba04d-108">When used with licensing handled through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), a server can become an entirely self-contained module with no need for external installation programs or .reg files.</span></span>

<span data-ttu-id="ba04d-109">Qualquer módulo de registro automático, DLL ou EXE, deve primeiro incluir uma cadeia de caracteres "OleSelfRegister" na seção [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) de seu recurso de informações de versão, como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="ba04d-109">Any self-registering module, DLL or EXE, should first include an "OleSelfRegister" string in the [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) section of its version information resource, as shown here.</span></span>

``` syntax
VS_VERSION_INFO VERSIONINFO 
 
 ... 
 
 BEGIN 
   BLOCK "StringFileInfo" 
    BEGIN 
#ifdef UNICODE 
     BLOCK "040904B0" // Lang=US English, CharSet=Unicode 
#else 
     BLOCK "040904E4" // Lang=US English, CharSet=Windows Multilingual 
#endif 
      BEGIN 
       ... 
       VALUE "OLESelfRegister", "\0" 
      END 
 
   ... 
 
   END 
 
 ... 
 
 END 
 
```

<span data-ttu-id="ba04d-110">A existência desses dados permite que qualquer parte interessada, como um aplicativo que queira integrar esse novo componente, determine se o servidor dá suporte a Autoregistro sem precisar carregar primeiro a DLL ou o EXE.</span><span class="sxs-lookup"><span data-stu-id="ba04d-110">The existence of this data allows any interested party, such as an application that wishes to integrate this new component, to determine whether the server supports self-registration without having to load the DLL or EXE first.</span></span>

<span data-ttu-id="ba04d-111">Se o servidor for empacotado em um módulo de DLL, a DLL deverá exportar as funções [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span><span class="sxs-lookup"><span data-stu-id="ba04d-111">If the server is packaged in a DLL module, the DLL must export the functions [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="ba04d-112">Qualquer aplicativo que queira instruir o servidor a se registrar (ou seja, todos os seus CLSIDs e IDs de biblioteca de tipos) pode obter um ponteiro para **DllRegisterServer** por meio da função [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ba04d-112">Any application that wishes to instruct the server to register itself (that is, all its CLSIDs and type library IDs) can obtain a pointer to **DllRegisterServer** through the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function.</span></span> <span data-ttu-id="ba04d-113">Dentro de **DllRegisterServer**, a dll cria todas as suas entradas de Registro necessárias, armazenando o caminho correto para a dll para todas as entradas [InprocServer32](inprocserver32.md) ou [InprocHandler32](inprochandler32.md) .</span><span class="sxs-lookup"><span data-stu-id="ba04d-113">Within **DllRegisterServer**, the DLL creates all its necessary registry entries, storing the correct path to the DLL for all [InprocServer32](inprocserver32.md) or [InprocHandler32](inprochandler32.md) entries.</span></span>

<span data-ttu-id="ba04d-114">Quando um aplicativo deseja remover o componente do sistema, ele deve cancelar o registro desse componente chamando [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span><span class="sxs-lookup"><span data-stu-id="ba04d-114">When an application wishes to remove the component from the system, it should unregister that component by calling [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="ba04d-115">Nessa chamada, o servidor remove exatamente as entradas que ele criou anteriormente em [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span><span class="sxs-lookup"><span data-stu-id="ba04d-115">Within this call, the server removes exactly those entries it previously created in [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span></span> <span data-ttu-id="ba04d-116">O servidor não deve remover de forma oculta todas as entradas de suas classes porque outro software pode ter armazenado entradas adicionais, como uma chave [Treats](treatas.md) .</span><span class="sxs-lookup"><span data-stu-id="ba04d-116">The server should not blindly remove all entries for its classes because other software may have stored additional entries, such as a [TreatAs](treatas.md) key.</span></span>

<span data-ttu-id="ba04d-117">Se o servidor for empacotado em um módulo EXE, o aplicativo que deseja registrar o servidor iniciará o servidor EXE com o argumento de linha de comando **/RegServer** ou **-RegServer** (não diferencia maiúsculas de minúsculas).</span><span class="sxs-lookup"><span data-stu-id="ba04d-117">If the server is packaged in an EXE module, the application wishing to register the server launches the EXE server with the command-line argument **/RegServer** or **-RegServer** (case-insensitive).</span></span> <span data-ttu-id="ba04d-118">Se o aplicativo quiser cancelar o registro do servidor, ele iniciará o EXE com o argumento de linha de comando **opção/UnregServer** ou **-UnregServer**.</span><span class="sxs-lookup"><span data-stu-id="ba04d-118">If the application wishes to unregister the server, it launches the EXE with the command-line argument **/UnregServer** or **-UnregServer**.</span></span> <span data-ttu-id="ba04d-119">O EXE de registro automático detecta esses argumentos de linha de comando e invoca as mesmas operações que uma DLL dentro de [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver), respectivamente, registrando seu caminho de módulo em [LocalServer32](localserver32.md) em vez de **InprocServer32** ou **InprocHandler32**.</span><span class="sxs-lookup"><span data-stu-id="ba04d-119">The self-registering EXE detects these command-line arguments and invokes the same operations as a DLL would within [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver), respectively, registering its module path under [LocalServer32](localserver32.md) instead of **InprocServer32** or **InprocHandler32**.</span></span>

<span data-ttu-id="ba04d-120">O servidor deve registrar o caminho completo para o local de instalação do módulo DLL ou EXE para suas respectivas chaves **InprocServer32**, **InprocHandler32** e **LocalServer32** no registro.</span><span class="sxs-lookup"><span data-stu-id="ba04d-120">The server must register the full path to the installation location of the DLL or EXE module for their respective **InprocServer32**, **InprocHandler32**, and **LocalServer32** keys in the registry.</span></span> <span data-ttu-id="ba04d-121">O caminho do módulo é facilmente obtido por meio da função [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .</span><span class="sxs-lookup"><span data-stu-id="ba04d-121">The module path is easily obtained through the [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba04d-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba04d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba04d-123">Instalando como um aplicativo de serviço</span><span class="sxs-lookup"><span data-stu-id="ba04d-123">Installing as a Service Application</span></span>](installing-as-a-service-application.md)
</dt> <dt>

[<span data-ttu-id="ba04d-124">Registrando uma classe na instalação</span><span class="sxs-lookup"><span data-stu-id="ba04d-124">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="ba04d-125">Registrando um servidor EXE em execução</span><span class="sxs-lookup"><span data-stu-id="ba04d-125">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
</dt> <dt>

[<span data-ttu-id="ba04d-126">Registrando objetos no corrompidos</span><span class="sxs-lookup"><span data-stu-id="ba04d-126">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> </dl>

 

 