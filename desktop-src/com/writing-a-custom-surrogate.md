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
# <a name="writing-a-custom-surrogate"></a>Gravando um substituto personalizado

Embora o substituto fornecido pelo sistema seja mais do que adequado para a maioria das situações, há alguns casos em que escrever um substituto personalizado pode ser válido. A seguir estão alguns exemplos:

-   Um substituto personalizado pode fornecer algumas otimizações ou semânticas que não estão presentes no substituto do sistema.
-   Se uma DLL em processo contiver código que depende de estar no mesmo processo que o cliente, o servidor DLL não funcionará corretamente se estiver em execução no substituto do sistema. Um substituto personalizado pode ser adaptado a uma DLL específica para lidar com isso.
-   O substituto do sistema dá suporte a um modelo de Threading misto para que ele possa carregar as DLLs de modelo livre e de compartimento. Um substituto personalizado pode ser adaptado para carregar somente DLLs de apartamento por motivos de eficiência ou para aceitar um argumento de linha de comando para o tipo de DLL que ele tem permissão para carregar.
-   Um substituto personalizado poderia pegar parâmetros de linha de comando extras que o sistema substituto não.
-   O substituto do sistema chama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e o informa para usar qualquer configuração de segurança existente encontrada na chave [AppID](appid-key.md) no registro. Um substituto personalizado pode usar outro contexto de segurança.
-   As interfaces que não são remotas (como as de OCXs recentes) não funcionarão com o substituto do sistema. Um substituto personalizado pode encapsular as interfaces da DLL com sua própria implementação e usar DLLs de proxy/stub com uma definição de IDL remota que permitiria que a interface fosse remota.

O thread substituto principal normalmente deve executar as seguintes etapas de configuração:

1.  Chame [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar o thread e definir o modelo de Threading.
2.  Se você quiser que os servidores DLL que devem ser executados no servidor possam usar as configurações de segurança na chave do registro **AppID** , chame [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) com a \_ funcionalidade AppID EOAC. Caso contrário, as configurações de segurança herdadas serão usadas.
3.  Chame [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) para registrar a interface substituta em com.
4.  Chame [**ISurrogate:: LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) para o CLSID solicitado.
5.  Coloque o thread principal em um loop para chamar [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) periodicamente.
6.  Quando COM chama [**ISurrogate:: FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), revogue todas as fábricas de classe e Exit.

Um processo substituto deve implementar a interface [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) . Essa interface deve ser registrada quando um novo substituto é iniciado e depois de chamar [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Conforme indicado nas etapas anteriores, a interface **ISurrogate** tem dois métodos que chamam: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver)para carregar dinamicamente novos servidores dll em substitutos existentes; e [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), para liberar o substituto.

A implementação de [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), que chama com com uma solicitação de carregamento, deve primeiro criar um objeto de fábrica de classe que dá suporte a [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)e [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)e, em seguida, chamar [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) para registrar o objeto como a fábrica de classes para o CLSID solicitado.

A fábrica de classes registrada pelo processo substituto não é a fábrica de classes real implementada pelo servidor DLL, mas é uma fábrica de classes genérica implementada pelo processo substituto que dá suporte a [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) e [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). Como é a fábrica de classes do substituto, em vez do servidor DLL que está sendo registrado, a fábrica de classes do substituto precisará usar a fábrica de classe real para criar uma instância do objeto para o CLSID registrado. O [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) do substituto deve ser semelhante ao exemplo a seguir:


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



A fábrica de classes do substituto também deve dar suporte a [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) porque uma chamada para [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) pode solicitar qualquer interface da fábrica de classes registrada, não apenas [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Além disso, como a fábrica de classes genérica dá suporte apenas a [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) e **IClassFactory**, as solicitações para outras interfaces devem ser direcionadas para o objeto real. Portanto, deve haver um método [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) que deve ser semelhante ao seguinte:


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



O substituto que hospeda um servidor DLL deve publicar os objetos de classe do servidor DLL com uma chamada para [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject). Todas as fábricas de classe para substitutos de DLL devem ser registradas como \_ substitutos de REGCLS. REGCLS \_ SINGLUSE e REGCLS \_ MULTIPLEUSE não devem ser usados para servidores DLL carregados em substitutos.

Seguir essas diretrizes para criar um processo substituto quando for necessário fazer isso deve garantir um comportamento adequado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Substitutos de DLL](dll-surrogates.md)
</dt> </dl>

 

 