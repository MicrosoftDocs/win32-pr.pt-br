---
title: Determinando o estado de sincronização da playlist
description: Determinando o estado de sincronização da playlist
ms.assetid: 634b659b-c3ae-4957-b17e-18fd92e915be
keywords:
- Windows Media Player, playlists de sincronização
- Windows Media Player modelo de objeto, playlists de sincronização
- modelo de objeto, playlists de sincronização
- Windows Media Player Mobile, synchronization playlists
- Windows Media Player ActiveX controle, listas de reprodução de sincronização
- Windows Media Player Controle de ActiveX móvel, listas de reprodução de sincronização
- ActiveX controle, listas de reprodução de sincronização
- playlists, sincronização
- playlists de metafile, sincronização
- Windows Playlists de metadados de mídia, sincronização
- dispositivos portáteis, determinando o estado da lista de reprodução de sincronização
- playlists de sincronização, estado de sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14af59f66d1b21eac00208ecc805f756761256e47a35042694bcd65e6f96558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579455"
---
# <a name="determining-playlist-synchronization-state"></a>Determinando o estado de sincronização da playlist

Windows Media Player 10 ou posterior usa o atributo **SyncState** para conter informações sobre se um arquivo de mídia digital específico foi copiado para um dispositivo portátil e, no caso de uma falha, se a cópia falhou porque o dispositivo não tinha memória suficiente.

O código de exemplo a seguir cria uma função que recupera essas informações de um arquivo de mídia digital. A função assume os seguintes parâmetros:

-   *pMedia*. Ponteiro para uma interface **IWMPMedia** que representa o arquivo de mídia digital a ser inspecionado.
-   *lPsIndex.* Índice de parceria do dispositivo atual.
-   *pulOnDevice.* Ponteiro para uma **variável** longa que recebe o valor que indica se o arquivo de mídia digital foi copiado para o dispositivo.
-   *pulDidNotFit.* Ponteiro para uma **variável** longa que recebe o valor que indica se a operação de cópia falhou porque o dispositivo não tinha memória suficiente.

As informações contidas no atributo **SyncState** são codificadas de maneira bit a bit. Você pode ver como essa função é usada no código de exemplo em [Enumerando os Itens de Mídia](enumerating-the-media-items.md).


```C++
STDMETHODIMP CSyncSettings::GetPartnershipSyncState(IWMPMedia* pMedia, long lPsIndex, ULONG *pulOnDevice, ULONG *pulDidNotFit)
{
    ATLASSERT(pMedia); 
    ATLASSERT(lPsIndex > 0 && 
              lPsIndex < 17);
    ATLASSERT(pulOnDevice);
    ATLASSERT(pulDidNotFit);
  
    CComVariant varSyncStateVal;   
    CComPtr<IWMPMedia> spMedia(pMedia); 
    CComPtr<IWMPMedia3> spMedia3;     
    HRESULT hr = spMedia.QueryInterface(&spMedia3); 
    ULONG ulSyncState = 0; // Stores the ulVal member of varSyncStateVal. 
    ULONG lLSB = 0; // Represents least significant bit: Did the media fail to copy because it would not fit?
    ULONG lMSB = 0; // Represents most significant bit: Is the media on the device?

    // Calculate the bit shift required to isolate the partnership bit 
    // pair from the SyncState attribute.
    const int iRshift = (lPsIndex - 1) * 2;

    if(SUCCEEDED(hr) && spMedia3)
    {       
        hr = spMedia3->getItemInfoByType(CComBSTR("SyncState"), CComBSTR(""), 0, &varSyncStateVal);
    }

    if(SUCCEEDED(hr) && varSyncStateVal.vt == VT_UI4)
    {   
        // Get the value.
        ulSyncState = varSyncStateVal.ulVal;

        // Shift the bit pair to the rightmost position.
        ulSyncState >>= iRshift; 

        // Mask the rightmost bit pair.
        ulSyncState &= 3;

        // Get the LSB         
        lLSB = ulSyncState & ~2; // Sets the 2E1 bit to zero. 

        // Get the MSB
        ulSyncState >>= 1;
        lMSB = ulSyncState;       
    }

    // Return the bits.
    *pulOnDevice = lMSB;
    *pulDidNotFit = lLSB;

    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMPMedia Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPMedia3::getItemInfoByType**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype)
</dt> <dt>

[**Gerenciando listas de reprodução de sincronização**](managing-synchronization-playlists.md)
</dt> <dt>

[**Atributo SyncState**](syncstate-attribute.md)
</dt> </dl>

 

 




