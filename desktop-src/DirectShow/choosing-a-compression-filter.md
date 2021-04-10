---
description: Escolhendo um filtro de compactação
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: Escolhendo um filtro de compactação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64ebebf41c35ed6aed9ab47d853c03ba720a31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104088775"
---
# <a name="choosing-a-compression-filter"></a>Escolhendo um filtro de compactação

Vários tipos de componentes de software podem executar a compactação de vídeo ou áudio, como:

-   Filtros do DirectShow nativo
-   Codecs do VCM (Gerenciador de compactação de vídeo)
-   Codecs do Gerenciador de compactação de áudio (ACM)
-   DMOs (objetos de mídia do DirectX)

No DirectShow, os codecs VCM são encapsulados pelo [filtro de compressor AVI](avi-compressor-filter.md)e os codecs do ACM são encapsulados pelo [filtro de invólucro do ACM](acm-wrapper-filter.md). DMOs são encapsuladas pelo [filtro de invólucro do DMO](dmo-wrapper-filter.md). O enumerador de dispositivo do sistema fornece uma maneira consistente de enumerar e criar qualquer um desses tipos de compressor, sem se preocupar com o modelo subjacente.

Para obter detalhes sobre o enumerador de dispositivo do sistema, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md). Resumidamente, todos os filtros do DirectShow são classificados por categoria e cada categoria é identificada por um GUID. Para os compactadores de vídeo, o GUID da categoria é CLSID \_ VideoCompressorCategory. Para os compactadores de áudio, é CLSID \_ AudioCompressorCategory. Para enumerar uma determinada categoria, o enumerador de dispositivo do sistema cria um objeto *enumerador* que dá suporte à interface [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) . O aplicativo usa essa interface para recuperar monikers de dispositivo, onde cada moniker de dispositivo representa uma instância de um filtro do DirectShow. Você pode usar o moniker para criar o filtro ou para obter o nome amigável do dispositivo sem criar o filtro.

Para enumerar os compactadores de vídeo ou áudio disponíveis no sistema do usuário, faça o seguinte:

1.  Chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o enumerador de dispositivo do sistema, que tem uma ID de classe de CLSID \_ SystemDeviceEnum.
2.  Chame [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) com o GUID da categoria de filtro. O método retorna um ponteiro de interface **IEnumMoniker** .
3.  Use o método IEnumMoniker:: Next para enumerar os monikers de dispositivo. Esse método retorna uma interface [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) , que representa o moniker.

Para obter o nome amigável de um moniker, faça o seguinte:

1.  Chame o método **IMoniker:: BindToStorage** . Esse método retorna um ponteiro de interface **IPropertyBag** .
2.  Use o método **IPropertyBag:: Read** para ler a propriedade **FriendlyName** .

Normalmente, um aplicativo exibiria uma lista de compactadores, para que o usuário pudesse escolher um. Por exemplo, o código a seguir preenche uma caixa de listagem com os nomes dos compactadores de vídeo disponíveis.


```C++
void OnInitDialog(HWND hDlg)
{
    HRESULT hr;
    ICreateDevEnum *pSysDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    IMoniker *pMoniker = NULL;

    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, 
        (void**)&pSysDevEnum);
    if (FAILED(hr))
    {
        // Handle the error.
    }    

    hr = pSysDevEnum->CreateClassEnumerator(
             CLSID_VideoCompressorCategory, &pEnum, 0);
    if (hr == S_OK)  // S_FALSE means nothing in this category.
    {
        while (S_OK == pEnum->Next(1, &pMoniker, NULL))
        {
            IPropertyBag *pPropBag = NULL;
            pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
                (void **)&pPropBag);
            VARIANT var;
            VariantInit(&var);
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
            if (SUCCEEDED(hr))
            {
                LRESULT iSel = AddString(GetDlgItem(hDlg, 
                    IDC_CODEC_LIST), var.bstrVal);
            }   
            VariantClear(&var); 
            pPropBag->Release();
            pMoniker->Release();
        }
    }

    SendDlgItemMessage(hDlg, IDC_CODEC_LIST, 
                       LB_SETCURSEL, 0, 0);
    pSysDevEnum->Release();
    pEnum->Release();
}
```



Para criar uma instância de filtro a partir do moniker, chame o método **IMoniker:: BindToObject** . O método retorna um ponteiro [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .


```C++
IBaseFilter *pFilter = NULL;
hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, 
                                       (void**)&pFilter);
if (SUCCEEDED(hr))
{
    // Use the filter. 
    // Remember to release the IBaseFilter interface.
}
```



Para codecs VCM, cada moniker representa um codec específico, embora todos os codecs sejam encapsulados pelo mesmo filtro de compactação AVI. Chamar **BindToObject** cria uma instância desse filtro, inicializada para esse codec. Por esse motivo, você não pode chamar **CoCreateInstance** diretamente no filtro de compactação avi. Você deve passar pelo enumerador de dispositivo do sistema.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recompactando um arquivo AVI](recompressing-an-avi-file.md)
</dt> </dl>

 

 
