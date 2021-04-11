---
title: Usando a exclusão mútua de taxa de bits múltiplas
description: Usando a exclusão mútua de taxa de bits múltiplas
ms.assetid: 69898b4d-fe10-422e-9ed2-87b65aa7bdb3
keywords:
- taxa de bits múltipla (MBR), exclusão mútua
- MBR (taxa de bits múltipla), exclusão mútua
- exclusão mútua, taxa de bits múltipla (MBR)
- perfis, taxa de bits múltipla (MBR)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be77c7615845d10d07982676dfdb4dc8c617cebe
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293755"
---
# <a name="using-multiple-bit-rate-mutual-exclusion"></a>Usando a exclusão mútua de taxa de bits múltiplas

A exclusão mútua de taxa de bits múltipla (MBR) é útil quando você deseja codificar o conteúdo para uma variedade de cenários de reprodução. Uma saída de vídeo MBR consiste em uma única entrada codificada várias vezes, cada uma com diferentes configurações de taxa de bits. Quando um arquivo com codificação MBR é lido, o leitor determinará qual fluxo usar com base na largura de banda disponível.

O SDK do Windows Media Format dá suporte à codificação MBR para fluxos de áudio e vídeo. Além disso, você pode criar um tipo especial de codificação de MBR chamado codificação MBR de tamanho de vários vídeos. As funções de vídeo MBR de tamanho múltiplo de vídeo são idênticas ao vídeo MBR normal, exceto que você pode especificar tamanhos de imagem diferentes para os fluxos de vídeo na exclusão mútua.

O exemplo a seguir demonstra como configurar um perfil para vídeo MBR com vários tamanhos de vídeo. Ele cria um novo perfil com três fluxos de vídeo de diferentes taxas e tamanhos de bits e os inclui em um objeto de exclusão mútua.


```C++
IWMProfileManager*  pProfileMgr = NULL;
IWMProfile*         pProfile    = NULL;
IWMMutualExclusion* pMutex      = NULL;
IWMStreamConfig*    pStream     = NULL;
IWMMediaProps*      pMediaProps = NULL;

WM_MEDIA_TYPE*      pMediaType  = NULL;
DWORD               cbMediaType = 0;

HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager object.
hr = WMCreateProfileManager(&pProfileMgr);

// Create an empty profile.
hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, &pProfile);

// Give the new profile a name and description.
hr = pProfile->SetName(L"MBR_Video_3_Stream_test");
hr = pProfile->SetDescription(L"Only for use with example code.");

// Create the first stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// Get the media properties interface for the new stream.
hr = pStream->QueryInterface(IID_IWMMediaProps, (void**)&pMediaProps);

// Get the media-type structure.
// First, get the size of the media-type structure.
hr = pMediaProps->GetMediaType(NULL, &cbMediaType);

// Allocate memory for the structure based on the retrieved size.
pMediaType = (WM_MEDIA_TYPE*) new BYTE[cbMediaType];

// Retrieve the media-type structure.
hr = pMediaProps->GetMediaType(pMediaType, &cbMediaType);

// Change the video size to 640 x 480.
pMediaType->pbFormat->bmiHeader.biWidth  = 640;
pMediaType->pbFormat->bmiHeader.biHeight = 480;

// Replace the WM_MEDIA_TYPE in the profile with the one just changed.
hr = pMediaProps->SetMediaType(pMediaType);

// Release the media properties interface and delete the structure.
pMediaProps->Release();
pMediaProps = NULL;
delete[] pMediaType;
pMediaType = NULL;

// Set the bit rate to 200.
hr = pStream->SetBitrate(200000);

// Set the stream number.
hr = pStream->SetStreamNumber(1);

// Include the new stream in the profile.
hr = pProfile->AddStream(pStream);

// Release the stream configuration interface.
pStream->Release();
pStream = NULL;

// For the remaining two streams, leave the video at its default size of
// 320 x 240 <entity type="ndash"/>- just change the bit rates.

// Repeat for a 100K stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);
hr = pStream->SetBitrate(100000);
hr = pStream->SetStreamNumber(2);
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Repeat for a 56K stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);
hr = pStream->SetBitrate(56000);
hr = pStream->SetStreamNumber(3);
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Now that we have three streams, create a mutual exclusion object.
hr = pProfile->CreateNewMutualExclusion(&pMutex);

// Add the three streams to the mutual exclusion.
hr = pMutex->AddStream(1);
hr = pMutex->AddStream(2);
hr = pMutex->AddStream(3);

// Configure the mutual exclusion for MBR video.
hr = pMutex->SetType(CLSID_WMMUTEX_Bitrate);

// Add the mutual exclusion to the profile.
hr = pProfile->AddMutualExclusion(pMutex);

// Release the mutual exclusion object.
pMutex->Release();
pMutex = NULL;

// TODO: Save the profile to a string, and save the string to a file.
// For more information, see To Save a Custom Profile.

// Release remaining interfaces.
pProfile->Release();
pProfile = NULL;

pProfileMgr->Release();
pProfileMgr = NULL;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**Interface IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**Interface IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interface IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[**Usando a exclusão mútua**](using-mutual-exclusion.md)
</dt> <dt>

[**\_tipo de mídia do WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)
</dt> </dl>

 

 




