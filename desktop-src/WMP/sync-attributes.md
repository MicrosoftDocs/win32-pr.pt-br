---
title: Atributos de sincronização
description: Os atributos Sync01 a Sync16 são representações de cadeia de caracteres de valores de 32 bits que o Windows Media Player usa ao sincronizar playlists com um de até 16 dispositivos portáteis.
ms.assetid: b9ae3420-aa09-4969-8637-f16d438942f3
keywords:
- Atributos de sincronização Windows Media Player
topic_type:
- apiref
api_name:
- Sync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e720598b17db6b073524d80afc8f39dd6e6f87e777246b5bdb60294b161fa1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134749"
---
# <a name="sync-attributes"></a>Atributos de sincronização

Os atributos **Sync01** a **Sync16** são representações de cadeia de caracteres de valores de 32 bits que Windows Media Player usa ao sincronizar playlists com um de até 16 dispositivos portáteis.

## <a name="applies-to"></a>Aplica-se A

-   [Playlists](playlist-attributes-ref.md)

## <a name="remarks"></a>Comentários

Esses são atributos de leitura/gravação. Um valor de zero indica que Windows Media Player não deve sincronizar a playlist com o dispositivo associado. Um valor maior que zero indica uma prioridade de sincronização para a playlist determinada.

Com base na entrada do usuário, Windows Media Player define esse atributo para cada uma das playlists na biblioteca. Quando Windows Media Player tenta sincronizar uma playlist com um dispositivo portátil, ele examina cada playlist para comparar os valores dos atributos **Sync**_XX_ que representam a parceria do dispositivo. As listas de reprodução que têm valores **de Sincronização**_XX menores_ recebem prioridade de sincronização mais alta.

Por exemplo, a biblioteca pode conter as quatro listas de reprodução a seguir e os respectivos **valores de Sincronização**_XX:_



| Nome da playlist | Valor de Sync01 |
|---------------|--------------|
| Music.WPL  | 0x0000000D   |
| Relax.WPL     | 0x00000020   |
| DriveHome.WPL | 0x00000001   |
| NoGo.WPL      | 0x00000000   |



 

Quando Windows Media Player sincroniza o dispositivo associado ao atributo , ele sincroniza as playlists na seguinte ordem:

1.  DriveHome.WPL
2.  Music.WPL
3.  Relax.WPL

Para determinar se você pode alterar o valor desse atributo, use o [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------|
| Versão<br/> | Windows Media Player 10 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> <dt>

[**Enumerando listas de reprodução de sincronização**](enumerating-synchronization-playlists.md)
</dt> </dl>

 

 





