---
title: Atributo SyncState
description: O atributo SyncState é uma representação de cadeia de caracteres de um valor de 32 bits que Windows Media Player ao sincronizar playlists com dispositivos portáteis.
ms.assetid: affc3d1c-7fe6-4811-acfc-57285cb181ca
keywords:
- Atributo SyncState Windows Media Player
topic_type:
- apiref
api_name:
- SyncState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7712a6e3bb0a01f4a713af114f91ebdcb302ef172c77e1cb64b8746f9ae0dcf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414856"
---
# <a name="syncstate-attribute"></a>Atributo SyncState

O **atributo SyncState** é uma representação de cadeia de caracteres de um valor de 32 bits que Windows Media Player usa ao sincronizar playlists com dispositivos portáteis.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Outros itens](other-item-attributes.md)
-   [Itens de foto](photo-item-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo consiste em 16 valores de 2 bits, cada um especificando o estado de sincronização de um dispositivo portátil. O MSB (bit mais significativo) desse valor de 32 bits corresponde ao dispositivo 16. O LSB (bit menos significativo) corresponde ao dispositivo 1.

O MSB de cada valor de 2 bits indica se Windows Media Player o conteúdo foi sincronizado com o dispositivo correspondente. Um valor de 1 indica que ele fez isso. Um valor de 0 indica que não.

Se o MSB for 0, o LSB especificará por que a sincronização falhou. Um valor de 1 no LSB indica que não havia espaço livre suficiente para o conteúdo. Um valor de 0 no LSB indica algum outro motivo para impedir a sincronização.

Para recuperar o estado de sincronização de um determinado dispositivo, faça o seguinte:

1.  **Invoque \_ o status IWMPSyncDevice::get** para determinar se um determinado dispositivo está sincronizado.
2.  Se ele estiver sincronizado, invoque **IWMPSyncDevice::get \_ partnershipIndex** para recuperar o índice do par de bits do dispositivo no atributo **SyncState.**
3.  Usando esse índice, mascara o par de bits correspondente do atributo **SyncState** e examina o resultado para determinar o estado de sincronização da playlist com o dispositivo.

Para determinar se você pode alterar o valor desse atributo, use o [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------|
| Versão<br/> | Windows Media Player 10 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> <dt>

[**Determinando o estado de sincronização da playlist**](determining-playlist-synchronization-state.md)
</dt> <dt>

[**IWMPSyncDevice::get \_ partnershipIndex**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[**IWMPSyncDevice::get \_ status**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 





