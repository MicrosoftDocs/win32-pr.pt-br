---
title: Escrevendo um substituto personalizado
description: Escrevendo um substituto personalizado
ms.assetid: 510e38e5-1965-46f4-b09c-6fa585cff993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c6098f4d0e9d99be86956bacce413e7e8a4b864a91212d6c2a1a257d9c1db7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047654"
---
# <a name="writing-a-custom-surrogate"></a>Escrevendo um substituto personalizado

Embora o substituto fornecido pelo sistema seja mais do que adequado para a maioria das situações, há alguns casos em que a escrita de um substituto personalizado pode valer a pena. A seguir estão alguns exemplos:

-   Um substituto personalizado pode fornecer algumas otimizações ou semânticas não presentes no substituto do sistema.
-   Se uma DLL em processo contiver código que dependa de estar no mesmo processo que o cliente, o servidor DLL não funcionará corretamente se estiver em execução no substituto do sistema. Um substituto personalizado pode ser adaptado a uma DLL específica para lidar com isso.
-   O substituto do sistema dá suporte a um modelo de threading misto para que ele possa carregar DLLs de modelo livre e apartment. Um substituto personalizado pode ser personalizado para carregar apenas DLLs de apartment por motivos de eficiência ou para aceitar um argumento de linha de comando para o tipo de DLL que ele tem permissão para carregar.
-   Um substituto personalizado pode usar parâmetros de linha de comando extras que o substituto do sistema não faz.
-   O substituto do sistema chama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e informa a ele para usar as configurações de segurança existentes encontradas na [chave AppID](appid-key.md) no Registro. Um substituto personalizado pode usar outro contexto de segurança.
-   Interfaces que não são remotas (como aquelas para OCXs recentes) não funcionarão com o substituto do sistema. Um substituto personalizado pode envolver as interfaces da DLL com sua própria implementação e usar DLLs de proxy/stub com uma definição de IDL remota que permitiria que a interface fosse remota.

O thread substituto principal normalmente deve executar as seguintes etapas de instalação:

1.  Chame [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar o thread e definir o modelo de threading.
2.  Se você quiser que os servidores DLL que devem ser executados no servidor sejam capazes de usar as configurações de segurança na chave do Registro **AppID,** chame [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) com a funcionalidade APPID do \_ EOAC. Caso contrário, as configurações de segurança herddas serão usadas.
3.  Chame [**CoRegisterSurrogate para**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) registrar a interface substituta no COM.
4.  Chame [**ISurrogate::LoadDllServer para**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) o CLSID solicitado.
5.  Coloque o thread principal em um loop para chamar [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) periodicamente.
6.  Quando COM chama [**ISurrogate::FreeSurrogate,**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate)revoga todas as fábricas de classes e sai.

Um processo substituto deve implementar a interface [**ISurrogate.**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) Essa interface deve ser registrada quando um novo substituto é iniciado e depois de chamar [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Conforme indicado nas etapas anteriores, a interface **ISurrogate** tem dois métodos que o COM chama: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), para carregar dinamicamente novos servidores DLL em substitutos existentes; e [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), para liberar o substituto.

A implementação de [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), que chama COM com uma solicitação de carregamento, deve primeiro criar um objeto de fábrica de classe que dá suporte a [**IUnknown,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)e [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)e, em seguida, chamar [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) para registrar o objeto como o factory de classe para o CLSID solicitado.

A fábrica de classes registrada pelo processo substituto não é a fábrica de classe real implementada pelo servidor DLL, mas é uma fábrica de classes genérica implementada pelo processo substituto que dá suporte a [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) e [**IMarshal.**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) Como é a fábrica de classes do substituto, em vez do servidor DLL que está sendo registrado, a fábrica de classes do substituto precisará usar a fábrica de classe real para criar uma instância do objeto para o CLSID registrado. O [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) do substituto deve ser algo parecido com o exemplo a seguir:


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



A fábrica de classes do substituto também deve dar suporte a [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) porque uma chamada para [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) pode solicitar qualquer interface da fábrica de classes registrada, não apenas [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Além disso, como a fábrica de classes genéricas dá suporte apenas a [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) e **IClassFactory,** as solicitações para outras interfaces devem ser direcionadas para o objeto real. Portanto, deve haver um [**método MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) que deve ser semelhante ao seguinte:


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



O substituto que acobre um servidor DLL deve publicar os objetos de classe do servidor DLL com uma chamada para [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject). Todas as fábricas de classes para substitutos de DLL devem ser registradas como REGCLS \_ SURROGATE. REGCLS SINGLUSE e REGCLS MULTIPLEUSE não devem ser usados para servidores \_ \_ DLL carregados em substitutos.

Seguir essas diretrizes para criar um processo substituto quando for necessário fazer isso deve garantir o comportamento adequado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Substitutos de DLL](dll-surrogates.md)
</dt> </dl>

 

 