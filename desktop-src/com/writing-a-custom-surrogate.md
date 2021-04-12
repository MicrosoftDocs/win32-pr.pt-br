---
title: Gravando um substituto personalizado
description: Gravando um substituto personalizado
ms.assetid: 510e38e5-1965-46f4-b09c-6fa585cff993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0899702f6626d586f8a819e8fee2c2e67b7c80
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294519"
---
# <a name="writing-a-custom-surrogate"></a><span data-ttu-id="e7d4a-103">Gravando um substituto personalizado</span><span class="sxs-lookup"><span data-stu-id="e7d4a-103">Writing a Custom Surrogate</span></span>

<span data-ttu-id="e7d4a-104">Embora o substituto fornecido pelo sistema seja mais do que adequado para a maioria das situações, há alguns casos em que escrever um substituto personalizado pode ser válido.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-104">While the system-supplied surrogate will be more than adequate for most situations, there are some cases where writing a custom surrogate could be worthwhile.</span></span> <span data-ttu-id="e7d4a-105">A seguir estão alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="e7d4a-105">Following are some examples:</span></span>

-   <span data-ttu-id="e7d4a-106">Um substituto personalizado pode fornecer algumas otimizações ou semânticas que não estão presentes no substituto do sistema.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-106">A custom surrogate could provide some optimizations or semantics not present in the system surrogate.</span></span>
-   <span data-ttu-id="e7d4a-107">Se uma DLL em processo contiver código que depende de estar no mesmo processo que o cliente, o servidor DLL não funcionará corretamente se estiver em execução no substituto do sistema.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-107">If an in-process DLL contains code that depends on being in the same process as the client, the DLL server will not function correctly if it is running in the system surrogate.</span></span> <span data-ttu-id="e7d4a-108">Um substituto personalizado pode ser adaptado a uma DLL específica para lidar com isso.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-108">A custom surrogate could be tailored to a specific DLL to deal with this.</span></span>
-   <span data-ttu-id="e7d4a-109">O substituto do sistema dá suporte a um modelo de Threading misto para que ele possa carregar as DLLs de modelo livre e de compartimento.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-109">The system surrogate supports a mixed-threading model so that it can load both free and apartment model DLLs.</span></span> <span data-ttu-id="e7d4a-110">Um substituto personalizado pode ser adaptado para carregar somente DLLs de apartamento por motivos de eficiência ou para aceitar um argumento de linha de comando para o tipo de DLL que ele tem permissão para carregar.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-110">A custom surrogate might be tailored to load only apartment DLLs for reasons of efficiency or to accept a command-line argument for the type of DLL it is allowed to load.</span></span>
-   <span data-ttu-id="e7d4a-111">Um substituto personalizado poderia pegar parâmetros de linha de comando extras que o sistema substituto não.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-111">A custom surrogate could take extra command-line parameters that the system surrogate does not.</span></span>
-   <span data-ttu-id="e7d4a-112">O substituto do sistema chama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e o informa para usar qualquer configuração de segurança existente encontrada na chave [AppID](appid-key.md) no registro.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-112">The system surrogate calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) and tells it to use any existing security settings found under the [AppID](appid-key.md) key in the registry.</span></span> <span data-ttu-id="e7d4a-113">Um substituto personalizado pode usar outro contexto de segurança.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-113">A custom surrogate could use another security context.</span></span>
-   <span data-ttu-id="e7d4a-114">As interfaces que não são remotas (como as de OCXs recentes) não funcionarão com o substituto do sistema.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-114">Interfaces that aren't remotable (such as those for recent OCXs) will not work with the system surrogate.</span></span> <span data-ttu-id="e7d4a-115">Um substituto personalizado pode encapsular as interfaces da DLL com sua própria implementação e usar DLLs de proxy/stub com uma definição de IDL remota que permitiria que a interface fosse remota.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-115">A custom surrogate could wrap the DLL's interfaces with its own implementation and use proxy/stub DLLs with a remotable IDL definition that would allow the interface to be remoted.</span></span>

<span data-ttu-id="e7d4a-116">O thread substituto principal normalmente deve executar as seguintes etapas de configuração:</span><span class="sxs-lookup"><span data-stu-id="e7d4a-116">The main surrogate thread should typically perform the following setup steps:</span></span>

1.  <span data-ttu-id="e7d4a-117">Chame [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar o thread e definir o modelo de Threading.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-117">Call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the thread and set the threading model.</span></span>
2.  <span data-ttu-id="e7d4a-118">Se você quiser que os servidores DLL que devem ser executados no servidor possam usar as configurações de segurança na chave do registro **AppID** , chame [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) com a \_ funcionalidade AppID EOAC.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-118">If you want the DLL servers that are to run in the server to be able to use the security settings in the **AppID** registry key, call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) with the EOAC\_APPID capability.</span></span> <span data-ttu-id="e7d4a-119">Caso contrário, as configurações de segurança herdadas serão usadas.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-119">Otherwise, legacy security settings will be used.</span></span>
3.  <span data-ttu-id="e7d4a-120">Chame [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) para registrar a interface substituta em com.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-120">Call [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) to register the surrogate interface to COM.</span></span>
4.  <span data-ttu-id="e7d4a-121">Chame [**ISurrogate:: LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) para o CLSID solicitado.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-121">Call [**ISurrogate::LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) for the requested CLSID.</span></span>
5.  <span data-ttu-id="e7d4a-122">Coloque o thread principal em um loop para chamar [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) periodicamente.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-122">Put main thread in a loop to call [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) periodically.</span></span>
6.  <span data-ttu-id="e7d4a-123">Quando COM chama [**ISurrogate:: FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), revogue todas as fábricas de classe e Exit.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-123">When COM calls [**ISurrogate::FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), revoke all class factories and exit.</span></span>

<span data-ttu-id="e7d4a-124">Um processo substituto deve implementar a interface [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) .</span><span class="sxs-lookup"><span data-stu-id="e7d4a-124">A surrogate process must implement the [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) interface.</span></span> <span data-ttu-id="e7d4a-125">Essa interface deve ser registrada quando um novo substituto é iniciado e depois de chamar [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="e7d4a-125">This interface should be registered when a new surrogate is started and after calling [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span></span> <span data-ttu-id="e7d4a-126">Conforme indicado nas etapas anteriores, a interface **ISurrogate** tem dois métodos que chamam: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver)para carregar dinamicamente novos servidores dll em substitutos existentes; e [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), para liberar o substituto.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-126">As indicated in the preceding steps, the **ISurrogate** interface has two methods that COM calls: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), to dynamically load new DLL servers into existing surrogates; and [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), to free the surrogate.</span></span>

<span data-ttu-id="e7d4a-127">A implementação de [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), que chama com com uma solicitação de carregamento, deve primeiro criar um objeto de fábrica de classe que dá suporte a [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)e [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)e, em seguida, chamar [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) para registrar o objeto como a fábrica de classes para o CLSID solicitado.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-127">The implementation of [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), which COM calls with a load request, must first create a class factory object that supports [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), and [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal), and then call [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) to register the object as the class factory for the requested CLSID.</span></span>

<span data-ttu-id="e7d4a-128">A fábrica de classes registrada pelo processo substituto não é a fábrica de classes real implementada pelo servidor DLL, mas é uma fábrica de classes genérica implementada pelo processo substituto que dá suporte a [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) e [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal).</span><span class="sxs-lookup"><span data-stu-id="e7d4a-128">The class factory registered by the surrogate process is not the actual class factory implemented by the DLL server but is a generic class factory implemented by the surrogate process that supports [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) and [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal).</span></span> <span data-ttu-id="e7d4a-129">Como é a fábrica de classes do substituto, em vez do servidor DLL que está sendo registrado, a fábrica de classes do substituto precisará usar a fábrica de classe real para criar uma instância do objeto para o CLSID registrado.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-129">Because it is the surrogate's class factory, rather than that of the DLL server that is being registered, the surrogate's class factory will need to use the real class factory to create an instance of the object for the registered CLSID.</span></span> <span data-ttu-id="e7d4a-130">O [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) do substituto deve ser semelhante ao exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="e7d4a-130">The surrogate's [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) should look something like the following example:</span></span>


```C++
STDMETHODIMP CSurrogateFactory::CreateInstance(
  IUnknown* pUnkOuter, 
  REFIID iid, 
  void** ppv)
{
    void* pcf;
    HRESULT hr;
 
    hr = CoGetClassObject(clsid, CLSCTX_INPROC_SERVER, NULL, IID_IClassFactory, &pcf);
    if ( FAILED(hr) )
        return hr;
    hr = ((IClassFactory*)pcf)->CreateInstance(pUnkOuter, iid, ppv);
    ((IClassFactory*)pcf)->Release();
    return hr;
}
 
```



<span data-ttu-id="e7d4a-131">A fábrica de classes do substituto também deve dar suporte a [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) porque uma chamada para [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) pode solicitar qualquer interface da fábrica de classes registrada, não apenas [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="e7d4a-131">The surrogate's class factory must also support [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) because a call to [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) can request any interface from the registered class factory, not just [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="e7d4a-132">Além disso, como a fábrica de classes genérica dá suporte apenas a [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) e **IClassFactory**, as solicitações para outras interfaces devem ser direcionadas para o objeto real.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-132">Further, since the generic class factory supports only [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and **IClassFactory**, requests for other interfaces must be directed to the real object.</span></span> <span data-ttu-id="e7d4a-133">Portanto, deve haver um método [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) que deve ser semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="e7d4a-133">Thus, there should be a [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) method which should be similar to the following:</span></span>


```C++
STDMETHODIMP CSurrogateFactory::MarshalInterface(
  IStream *pStm,  
  REFIID riid, void *pv, 
  WORD dwDestContext, 
  void *pvDestContext, 
  DWORD mshlflags )
{   
    void * pCF = NULL;
    HRESULT hr;
 
    hr = CoGetClassObject(clsid, CLSCTX_INPROC_SERVER, NULL, riid, &pCF);
    if ( FAILED(hr) )
        return hr;   
    hr = CoMarshalInterface(pStm, riid, (IUnknown*)pCF, dwDestContext, pvDestContext,  mshlflags);
    ((IUnknown*)pCF)->Release();
    return S_OK;
 
```



<span data-ttu-id="e7d4a-134">O substituto que hospeda um servidor DLL deve publicar os objetos de classe do servidor DLL com uma chamada para [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject).</span><span class="sxs-lookup"><span data-stu-id="e7d4a-134">The surrogate that houses a DLL server must publish the DLL server's class object(s) with a call to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject).</span></span> <span data-ttu-id="e7d4a-135">Todas as fábricas de classe para substitutos de DLL devem ser registradas como \_ substitutos de REGCLS.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-135">All class factories for DLL surrogates should be registered as REGCLS\_SURROGATE.</span></span> <span data-ttu-id="e7d4a-136">REGCLS \_ SINGLUSE e REGCLS \_ MULTIPLEUSE não devem ser usados para servidores DLL carregados em substitutos.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-136">REGCLS\_SINGLUSE and REGCLS\_MULTIPLEUSE should not be used for DLL servers loaded into surrogates.</span></span>

<span data-ttu-id="e7d4a-137">Seguir essas diretrizes para criar um processo substituto quando for necessário fazer isso deve garantir um comportamento adequado.</span><span class="sxs-lookup"><span data-stu-id="e7d4a-137">Following these guidelines for creating a surrogate process when it is necessary to do so should ensure proper behavior.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7d4a-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7d4a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7d4a-139">Substitutos de DLL</span><span class="sxs-lookup"><span data-stu-id="e7d4a-139">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 