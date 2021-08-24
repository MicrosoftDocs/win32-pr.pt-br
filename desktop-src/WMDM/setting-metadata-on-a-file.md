---
title: Definindo metadados em um arquivo
description: Definindo metadados em um arquivo
ms.assetid: 478a5412-e8b4-41c8-802f-9c2748dbaeae
keywords:
- Windows Mídia Gerenciador de Dispositivos, metadados
- Gerenciador de Dispositivos, metadados
- guia de programação, metadados
- aplicativos da área de trabalho, metadados
- criando Windows mídia Gerenciador de Dispositivos aplicativos, metadados
- escrevendo arquivos em dispositivos, metadados
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64bdd173258272801886b90dca2265425eb65fd8ec3e5a25d01db37453d7eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766266"
---
# <a name="setting-metadata-on-a-file"></a>Definindo metadados em um arquivo

Você pode definir metadados em um arquivo antes de escrevê-lo no dispositivo (ao usar [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)) ou em um armazenamento existente (chamando [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)). Você pode definir atributos somente em um armazenamento existente (chamando [**IWMDMStorage::SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes) ou [**IWMDMStorage2::SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)).

A configuração de metadados é feita criando e preenchendo uma interface [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) passada para [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3). No entanto, esse método pode limpar todos os metadados existentes no arquivo, além dos metadados codificados armazenados no próprio sistema de arquivos, como o nome ou o tamanho do arquivo. Portanto, você deve copiar todos os metadados existentes que deseja manter na interface IWMDMMetaData que você enviar. Como Windows Media Gerenciador de Dispositivos não pode ser usado para recuperar metadados de arquivos locais, você deve usar o SDK de Formato de Mídia do Windows (ou alguma outra ferramenta) para recuperar esses metadados.

Para usar o Windows SDK de Formato de Mídia para recuperar propriedades de arquivo ASF, siga estas etapas:

1.  Crie um objeto do editor de metadados chamando **WMCreateEditor** e solicitando uma interface **IWMMetadataEditor.**
2.  Abra o arquivo para leitura de metadados chamando **IWMMetadataEditor::Open**.
3.  Se o arquivo for um arquivo ASF válido e puder ser aberto, consulte o editor para a interface **IWMHeaderInfo.**
4.  Recupere as propriedades do arquivo chamando **IWMHeaderInfo::GetAttributeByName,** passando a constante de propriedade do SDK de Formato de Windows Mídia desejada. Uma lista de constantes do SDK de formato com constantes Windows mídia Gerenciador de Dispositivos SDK equivalentes é apresentada na tabela a seguir.



| Windows Constante do SDK de Formato de Mídia    | Windows Constante do SDK Gerenciador de Dispositivos mídia      |
|--------------------------------------|------------------------------------------------|
| g \_ wszWMTitle                        | g \_ wszWMDMTitle                                |
| g \_ wszWMAuthor                       | g \_ wszWMDMAuthor                               |
| g \_ wszWMAlbumTitle                   | g \_ wszWMDMAlbumTitle                           |
| g \_ wszWMGenre                        | g \_ wszWMDMGenre                                |
| g \_ wszWMYear                         | g \_ wszWMDMYear                                 |
| g \_ wszWMTrackNumber ou g \_ wszWMTrack | g \_ wszWMDMTrack                                |
| g \_ wszWMComposer                     | g \_ wszWMDMComposer                             |
| g \_ wszWMDuration                     | g \_ wszWMDMDuration                             |
| g \_ wszWMCopyright                    | g \_ wszWMDMProviderCopyright                    |
| g \_ wszWMDescription                  | g \_ wszWMDMDescription                          |
| g \_ wszWMBitrate                      | g \_ wszWMDMBitrate                              |
| g \_ wszWMRating                       | g \_ wszWMDMUserRating                           |
| g \_ wszWMAlbumArtist                  | g \_ wszWMDMAlbumArtist                          |
| g \_ wszWMParentalRating               | g \_ wszWMDMParentalRating                       |
| g \_ wszWMRadioStationName             | g \_ wszWMDMMediaStationName                     |
| g \_ wszWMSubTitle                     | g \_ wszWMDMSubTitle                             |
| g \_ wszWMVideoWidth                   | g \_ wszWMDMWidth                                |
| g \_ wszWMVideoHeight                  | g \_ wszWMDMHeight                               |
| g \_ wszWMMood                         | g \_ wszWMDMTrackMood                            |
| g \_ wszWMCodec                        | g \_ wszAudioWAVECodec ou g \_ wszVideoCodec |



 

O código de exemplo C++ a seguir demonstra a recuperação de várias propriedades de metadados de um arquivo ASF usando o SDK de Formato de Mídia do Windows e convertendo-as nos valores Windows Media Gerenciador de Dispositivos equivalentes.


```C++
// Structure and array to hold equivalent Windows Media Format SDK 
// and Windows Media Device Manager SDK metadata property names.
struct EquivalentProperty
{
    LPCWSTR FormatSDKConst;
    LPCWSTR WMDMSDKConst;
};
EquivalentProperty EquivalentProperties []= 
{
    {g_wszWMTitle,        g_wszWMDMTitle},
    {g_wszWMAuthor,      g_wszWMDMAuthor},
    {g_wszWMAlbumTitle,  g_wszWMDMAlbumTitle},
    {g_wszWMGenre,       g_wszWMDMGenre},
    {g_wszWMYear,        g_wszWMDMYear},
    {g_wszWMTrackNumber, g_wszWMDMTrack},
    {g_wszWMTrack,       g_wszWMDMTrack},
    {g_wszWMComposer,    g_wszWMDMComposer},
    {g_wszWMBitrate,     g_wszWMDMBitrate},
    {g_wszWMDuration,    g_wszWMDMDuration},
    {g_wszWMCopyright,   g_wszWMDMProviderCopyright},
    {g_wszWMDescription, g_wszWMDMDescription},
    {g_wszWMRating,      g_wszWMDMUserRating},
    {g_wszWMAlbumArtist, g_wszWMDMAlbumArtist},
    {g_wszWMParentalRating,    g_wszWMDMParentalRating},
    {g_wszWMRadioStationName,  g_wszWMDMMediaStationName},
    {g_wszWMSubTitle,    g_wszWMDMSubTitle},
    {g_wszWMVideoWidth,  g_wszWMDMWidth},
    {g_wszWMVideoHeight, g_wszWMDMHeight},
    {g_wszWMMood,        g_wszWMDMTrackMood},
    {g_wszWMCodec,       g_wszAudioWAVECodec},
    {g_wszWMCodec,       g_wszVideoFourCCCodec}
};
// Function that tries to get metadata by using the Format SDK. 
// If it cannot open the file, it returns E_FAIL.
HRESULT GetFileMetadataFromFormatSDK(IWMDMMetaData* pMetadata, LPCWSTR file)
{
    if ((pMetaData == NULL) || (file == NULL)) return E_INVALIDPARAM;
    HRESULT hr = S_OK;
    CComPtr<IWMMetadataEditor> pEditor;

    // Do loop to allow easy error trapping. Even if there are no errors, 
    // the loop executes only once.
    do {
        hr = WMCreateEditor(&pEditor);
        if (FAILED(hr)) 
            break;

        // Open the file.
        hr = pEditor->Open(file);
        if (FAILED(hr)) 
            break;

        CComPtr<IWMHeaderInfo>pHeaderInfo;
        hr = pEditor->QueryInterface(__uuidof(IWMHeaderInfo), (void**)&pHeaderInfo);
        if (FAILED(hr))
            break;

        // Copy values from Format SDK to equivalent WMDM SDK metadata values.

        // Loop through all known values
        WORD stream = 0;
        WMT_ATTR_DATATYPE wmfType;
        WORD len = 0;
        BYTE* value = NULL;
        WMDM_TAG_DATATYPE wmdmType;
        for (int i = 0; i < sizeof(EquivalentProperties) / sizeof(EquivalentProperties[0]); i++)
        {
            // Request each value from our equivalency list by name.
            // The function is called twice: once to get the buffer size,
            // and once to get the value in the allocated buffer.
            if (FAILED(pHeaderInfo->GetAttributeByName(
                &stream, EquivalentProperties[i].FormatSDKConst, &wmfType, NULL, &len)))
            {
                continue;
            }

            value = new BYTE[len];
            if (value == NULL) continue;

            if (FAILED(pHeaderInfo->GetAttributeByName(&stream, EquivalentProperties[i].FormatSDKConst, &wmfType, value, &len)))
            {
                delete[] value;
                continue;
            }

            // Send the data to the equivalent WMDM metadata value.
            // First, find the equivalent WMDM type for the WMF type.
            switch(wmfType)
            {
            case WMT_TYPE_BINARY:
                wmdmType = WMDM_TYPE_BINARY;
                break;
            case WMT_TYPE_DWORD:
                wmdmType = WMDM_TYPE_DWORD;
                break;
            case WMT_TYPE_STRING:
                wmdmType = WMDM_TYPE_STRING;
                break;
            case WMT_TYPE_BOOL:
                wmdmType = WMDM_TYPE_BOOL;
                break;
            case WMT_TYPE_QWORD:
                wmdmType = WMDM_TYPE_QWORD;
                break;
            case WMT_TYPE_WORD:
                wmdmType = WMDM_TYPE_WORD;
                break;
            case WMT_TYPE_GUID:
                wmdmType = WMDM_TYPE_GUID;
                break;
            default:
                wmdmType = WMDM_TYPE_BINARY;
                break;
            }

            // Don't worry about trapping errors, because there's nothing 
            // we can do about it.
            pMetadata->AddItem(wmdmType, 
                EquivalentProperties[i].WMDMSDKConst, value, len);
            delete[] value;
        } // Add next value.
    } while (FALSE); // End Do loop error trap.

    // Close the file opened with IWMMetadataEditor.
    pEditor->Close();
    return hr;
}
```



A função de exemplo C++ a seguir mostra como usar DirectShow para obter algumas informações de arquivo e adicioná-la aos metadados.


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
HRESULT GetFileMetadataFromDShow(IWMDMMetaData* pMetadata, LPCWSTR file)
{
    HRESULT hr = S_OK;

    // Add file metadata properties from DirectShow. 
    // This is good for non-ASF files, or to add any information
    // that the Format SDK didn't get.

    // Do loop to allow easy error trapping. Even if there are no errors, 
    // the loop executes only once.
    do
    {
        // Create the Media Detector object.
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (FAILED(hr)) 
            break;

        // Open the file.
        hr = pIMediaDet->put_Filename(BSTR(file));
        if (FAILED(hr))
            break;

        // Get the media type for the default stream.
        AM_MEDIA_TYPE mediaType;
        hr = pIMediaDet->get_StreamMediaType(&mediaType);
        if (FAILED(hr))
            break;

        // We have the file open, so start requesting information from the 
        // Media Detector and adding it to the metadata. When adding 
        // individual metadata values, ignore the HRESULT, because failure 
        // to add these metadata values is not a breaking issue.

        // Get major and minor types.
        WCHAR strMediaType[64];
        ZeroMemory(strMediaType, 64);

        //Change the major type to a string, then add to IWMDMMetaData.
        StringFromGUID2(reinterpret_cast<GUID&>(mediaType.majortype),
            (LPOLESTR)strMediaType, 64);
        hr = pMetadata->AddItem(WMDM_TYPE_STRING, 
             g_wszWMDMediaClassPrimaryID, 
            (BYTE*) strMediaType, 
             sizeof(strMediaType) / sizeof(strMediaType[0]));

        // Clear local string, then retrieve subtype the same way.
        ZeroMemory(strMediaType, 64);
        StringFromGUID2(reinterpret_cast<GUID&>(mediaType.subtype),
            (LPOLESTR)strMediaType, 64);
        hr = pMetadata->AddItem(WMDM_TYPE_STRING, 
            g_wszWMDMMediaClassSecondaryID, (BYTE*) strMediaType,
            sizeof(strMediaType) / sizeof(strMediaType[0]));

        // Get the duration. Duration is retrieved in seconds, but set 
        // in 100-nanosecond units.
        double duration = 0;
        hr = pIMediaDet->get_StreamLength(&duration);
        if (duration > 0)
        {
            duration *= 10E7;
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMDuration, (BYTE*) &duration, sizeof(duration));
        }

        // Get the frame rate.
        double frameRate = 0;
        hr = pIMediaDet->get_FrameRate(&frameRate);
        if (frameRate > 0)
        {
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMFrameRate, 
                (BYTE*) &frameRate,
                sizeof(frameRate));
        }

        // Get the structure for the default stream's major type and 
        // fill in additional information.

        if (IsEqualGUID(mediaType.formattype, FORMAT_VideoInfo))
        {
            VIDEOINFOHEADER* data = (VIDEOINFOHEADER*) mediaType.pbFormat;
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMVideoBitrate, 
               (BYTE*) &data->dwBitRate, sizeof(DWORD));
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMHeight, 
               (BYTE*) &data->bmiHeader.biHeight, sizeof(LONG));
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMWidth, 
               (BYTE*) &data->bmiHeader.biWidth, sizeof(LONG));
        }

        if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
        {
            WAVEFORMATEX* data = (WAVEFORMATEX*) mediaType.pbFormat;
            hr = pMetadata->AddItem(WMDM_TYPE_WORD, g_wszWMDMBlockAlignment, 
                (BYTE*) &data->nBlockAlign, sizeof(WORD));
            hr = pMetadata->AddItem(WMDM_TYPE_WORD, g_wszWMDMNumChannels, 
               (BYTE*) &data->nChannels, sizeof(WORD));
        }
    } while (FALSE); // End of error loop.
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Escrevendo arquivos no dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




