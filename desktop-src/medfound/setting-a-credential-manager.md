---
description: Configurando um Gerenciador de credenciais
ms.assetid: a20c2e6c-e9d9-438f-a57a-e3080587c11c
title: Configurando um Gerenciador de credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c98d9d9572438a63f93f916a0084f8a33a7bca5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808251"
---
# <a name="setting-a-credential-manager"></a>Configurando um Gerenciador de credenciais

Um aplicativo que fornece credenciais para a fonte de rede deve fazer o seguinte:

1.  Implemente um objeto do Gerenciador de credenciais que expõe a interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .
2.  Antes de criar a origem da rede, crie um novo repositório de propriedades.
3.  Defina a propriedade [**MFNETSOURCE \_ Credential \_ Manager**](mfnetsource-credential-manager-property.md) no repositório de propriedades. O valor da propriedade é um ponteiro para a interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .
4.  Passe um ponteiro para o repositório de propriedades para o resolvedor de origem, conforme descrito em [Configurando uma origem de mídia](configuring-a-media-source.md).

As fontes de rede usam o Gerenciador de credenciais para obter credenciais de usuário. Se a origem da rede exigir credenciais para acessar um recurso de rede, ela chamará o método [**IMFNetCredentialManager:: BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) do aplicativo. Essa chamada inicia uma solicitação assíncrona para obter as credenciais do usuário. O método **BeginGetCredentials** pode obter as credenciais do cache de credenciais ou do usuário. As credenciais são armazenadas em um *objeto de credencial*. Quando a operação for concluída, o aplicativo invocará a interface de retorno de chamada para notificar a origem da rede. A origem da rede chama [**IMFNetCredentialManager:: EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) para concluir a operação assíncrona.

Como essa é uma operação assíncrona, o aplicativo deve despachar o retorno de chamada no final da operação. Para obter instruções detalhadas sobre como escrever um método assíncrono, consulte [escrevendo um método assíncrono](writing-an-asynchronous-method.md).

O exemplo a seguir mostra como definir a propriedade [**MFNETSOURCE \_ Credential \_ Manager**](mfnetsource-credential-manager-property.md) na fonte de rede.


```C++
// Creates a media source from a URL.
//
// Demonstrates how to set a credential manager on the network source.

HRESULT CreateMediaSourceWithCredentialManager(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CCredentialManager *pCredentials = new (std::nothrow) CCredentialManager();

    if (pCredentials == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_CREDENTIAL_MANAGER;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pCredentials->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(key, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pCredentials);

    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação de origem da rede](network-source-authentication.md)
</dt> </dl>

 

 



