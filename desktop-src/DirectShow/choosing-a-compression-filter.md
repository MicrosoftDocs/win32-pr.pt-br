---
description: Escolhendo um filtro de compactação
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: Escolhendo um filtro de compactação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf964aa3647086efe569263e5fb36b4e0db60ebfad73c9d2fe9dcb14f3bcf125
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999216"
---
# <a name="choosing-a-compression-filter"></a>Escolhendo um filtro de compactação

Vários tipos de componentes de software podem executar compactação de áudio ou vídeo, como:

-   Filtros DirectShow nativos
-   Codecs do VCM (Gerenciador de Compactação de Vídeo)
-   Codecs do ACM (Gerenciador de Compactação de Áudio)
-   DMOs (Objetos de Mídia DirectX)

No DirectShow, os codecs VCM são empacotados pelo Filtro [Desodor de Avi E](avi-compressor-filter.md)os codecs do ACM são empacotados pelo Filtro [wrapper do ACM.](acm-wrapper-filter.md) Os DMOs são empacotados pelo [filtro DMO Wrapper.](dmo-wrapper-filter.md) O enumerador de dispositivo do sistema fornece uma maneira consistente de enumerar e criar qualquer um desses tipos de coisas sem se preocupar com o modelo subjacente.

Para obter detalhes sobre o enumerador de dispositivo do sistema, [consulte Usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md). Resumidamente, todos DirectShow filtros são classificados por categoria e cada categoria é identificada por um GUID. Para videoclipes, o GUID da categoria é ClSID \_ VideoCompressorCategory. Para audiovisores, é CLSID \_ AudioCompressorCategory. Para enumerar uma categoria específica, o enumerador de dispositivo do sistema cria um *objeto enumerador* que dá suporte à interface [**IEnumMoniker.**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) O aplicativo usa essa interface para recuperar monikers de dispositivo, em que cada moniker de dispositivo representa uma instância de um DirectShow filtro. Você pode usar o moniker para criar o filtro ou para obter o nome amigável do dispositivo sem criar o filtro.

Para enumerar os video ou audiovisões disponíveis no sistema do usuário, faça o seguinte:

1.  Chame [**CoCreateInstance para**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) criar o enumerador de dispositivo do sistema, que tem uma ID de classe de CLSID \_ SystemDeviceEnum.
2.  Chame [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) com o GUID da categoria de filtro. O método retorna um ponteiro de interface **IEnumMoniker.**
3.  Use o método IEnumMoniker::Next para enumerar os monikers do dispositivo. Esse método retorna uma interface [**IMoniker,**](/windows/desktop/api/objidl/nn-objidl-imoniker) que representa o moniker.

Para obter o nome amigável de um moniker, faça o seguinte:

1.  Chame o **método IMoniker::BindToStorage.** Esse método retorna um ponteiro de interface **IPropertyBag.**
2.  Use o **método IPropertyBag::Read** para ler a **propriedade FriendlyName.**

Normalmente, um aplicativo exibiria uma lista de visores, para que o usuário pudesse escolher um. Por exemplo, o código a seguir preenche uma caixa de listagem com os nomes dos videoclipes disponíveis.


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



Para criar uma instância de filtro do moniker, chame o **método IMoniker::BindToObject.** O método retorna um [**ponteiro IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)


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



Para codecs VCM, cada moniker representa um codec específico, embora todos os codecs sejam empacotados pelo mesmo filtro de Compactação AVI. Chamar **BindToObject** cria uma instância desse filtro, inicializada para esse codec. Por esse motivo, você não pode chamar **CoCreateInstance** diretamente no filtro compactação AVI. Você deve passar pelo enumerador de dispositivo do sistema.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recompactando um arquivo AVI](recompressing-an-avi-file.md)
</dt> </dl>

 

 
