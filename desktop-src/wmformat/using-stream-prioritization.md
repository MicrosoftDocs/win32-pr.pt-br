---
title: Usando a priorização de fluxo
description: Usando a priorização de fluxo
ms.assetid: 5fff212e-b47b-49a6-817f-f0e09c895b3a
keywords:
- SDK do Windows Media Format, priorização de fluxo
- perfis, priorização de fluxo
- fluxos, priorização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a6b0bd3d49db9523ef9ea5585803b4c703c279
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916971"
---
# <a name="using-stream-prioritization"></a>Usando a priorização de fluxo

A priorização de fluxo permite que você tenha mais controle sobre a reprodução de conteúdo, permitindo que você especifique a ordem de prioridade para os fluxos em um perfil. Quando o leitor e o servidor de streaming encontram uma falta de largura de banda durante a reprodução, os exemplos podem ter que ser descartados para fornecer reprodução ininterrupta. Se você especificar uma ordem de prioridade com um objeto de priorização de fluxo no perfil, os exemplos serão removidos dos fluxos de prioridade mais baixos primeiro.

Ao contrário dos objetos de compartilhamento de largura de banda e de exclusão mútua, um objeto de priorização de fluxo não usa a interface [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist) para controlar a lista de fluxos. Em vez disso, você deve usar uma matriz de estruturas de [**registro de prioridade de fluxo do WM \_ \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record) . As estruturas devem ser organizadas na matriz em ordem decrescente de prioridade. Além de conter um número de fluxo, a estrutura de prioridade de fluxo também permite que você especifique se um fluxo é obrigatório. Os fluxos obrigatórios não serão removidos, independentemente de sua posição na lista.

O código de exemplo a seguir mostra como incluir uma priorização de fluxo em um perfil. Esse perfil é para uma apresentação da sala de aula, com um fluxo de áudio do palestrante, um fluxo de vídeo do palestrante e um fluxo de vídeo capturando os slides da apresentação. O fluxo de áudio é o mais importante e será obrigatório. Os slides de apresentação terão a menor prioridade, pois a imagem será bastante constante, portanto, alguns quadros serão perdidos e não haverá muita diferença.


```C++
IWMProfileManager*       pProfileMgr = NULL;
IWMProfile*              pProfileTmp = NULL;
IWMProfile3*             pProfile    = NULL;
IWMStreamPrioritization* pPriority   = NULL;

WM_STREAM_PRIORITY_RECORD StreamArray[3];
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager object.
hr = WMCreateProfileManager(&pProfileMgr);

// Create an empty profile.
hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, &pProfileTmp)

// Get the IWMProfile3 for the new profile, then release the old one.
hr = pProfileTmp->QueryInterface(IID_IWMProfile3, (void**)&pProfile);
pProfileTmp->Release();
pProfileTmp = NULL;

// Give the new profile a name and description.
hr = pProfile->SetName(L"Prioritization_Example");
hr = pProfile->SetDescription(L"Only for use with example code.");

// Create the first stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Audio, &pStream);

// TODO: configure the stream as needed for the scenario.

// Set the stream number.
hr = pStream->SetStreamNumber(1);

// Give the stream a name for clarity.
hr = pStream->SetStreamName(L"Lecturer_Audio");

// Include the new stream in the profile.
hr = pProfile->AddStream(pStream);

// Release the stream configuration interface.
pStream->Release();
pStream = NULL;

// Repeat for the other two streams.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// TODO: configure the stream as needed for the scenario.
hr = pStream->SetStreamNumber(2);
hr = pStream->SetStreamName(L"Lecturer_Video");
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// TODO: configure the stream as needed for the scenario.
hr = pStream->SetStreamNumber(3);
hr = pStream->SetStreamName(L"Slide_Video");
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Create a stream prioritization object.
hr = pProfile->CreateNewStreamPrioritization(&pPriority);

// Fill the array with data.
StreamArray[0].wStreamNum = 1;
StreamArray[0].fMandatory = TRUE;

StreamArray[1].wStreamNum = 2;
StreamArray[1].fMandatory = FALSE;

StreamArray[2].wStreamNum = 3;
StreamArray[2].fMandatory = FALSE;

// Assign the stream array to the stream prioritization object.
hr = pPriority->SetPriorityRecords(StreamArray, 3);

// Add the stream prioritization to the profile.
hr = pProfile->SetStreamPrioritization(pPriority);

// Release the stream prioritization object.
pPriority->Release();
pPriority = NULL;

// TODO: Save the profile to a string, and save the string to a file.
// For more information, see To Save a Custom Profile.

// Release the remaining interfaces.
pProfile->Release();
pProfile = NULL;

pProfileMgr->Release();
pProfileMgr = NULL;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com perfis**](working-with-profiles.md)
</dt> </dl>

 

 




