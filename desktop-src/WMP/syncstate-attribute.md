---
title: Atributo SyncState
description: O atributo SyncState é uma representação de cadeia de caracteres de um valor de 32 bits que o Windows Media Player usa quando sincroniza as listas de reprodução com dispositivos portáteis.
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
ms.openlocfilehash: 2a948f6c649d548b375ccb676134177b0273c85c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761581"
---
# <a name="syncstate-attribute"></a>Atributo SyncState

O atributo **SyncState** é uma representação de cadeia de caracteres de um valor de 32 bits que o Windows Media Player usa quando sincroniza as listas de reprodução com dispositivos portáteis.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Outros itens](other-item-attributes.md)
-   [Itens de foto](photo-item-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo consiste em valores de 16 2 bits, cada um dos quais Especifica o estado de sincronização de um dispositivo portátil. O bit mais significativo (MSB) desse valor de 32 bits corresponde ao dispositivo 16. O bit menos significativo (LSB) corresponde ao dispositivo 1.

O MSB de cada valor de 2 bits indica se o Windows Media Player sincronizou o conteúdo com o dispositivo correspondente. Um valor de 1 indica que ele fez. Um valor de 0 indica que ele não foi.

Se o MSB for 0, o LSB especificará por que a sincronização falhou. Um valor de 1 no LSB indica que não havia espaço livre suficiente para o conteúdo. Um valor de 0 no LSB indica algum outro motivo que impediu a sincronização.

Para recuperar o estado de sincronização de um determinado dispositivo, você deve fazer o seguinte:

1.  Invocar **IWMPSyncDevice:: get \_ status** para determinar se um determinado dispositivo está sincronizado.
2.  Se estiver sincronizada, invoque **IWMPSyncDevice:: get \_ partnershipIndex** para recuperar o índice do par de bits do dispositivo no atributo **SyncState** .
3.  Usando esse índice, mascara o par de bits correspondente do atributo **SyncState** e examine o resultado para determinar o estado de sincronização da lista de reprodução com o dispositivo.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

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

[**IWMPSyncDevice:: obter \_ partnershipIndex**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[**IWMPSyncDevice:: obter \_ status**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 





