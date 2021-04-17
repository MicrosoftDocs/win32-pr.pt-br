---
title: Atributos de sincronização
description: Os atributos Sync01 por meio de Sync16 são representações de cadeia de caracteres de valores de 32 bits que o Windows Media Player usa quando sincroniza as listas de reprodução com um de até 16 dispositivos portáteis.
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
ms.openlocfilehash: 5af26ae563a38efcc40b0bcd319c5fc62b4776dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787612"
---
# <a name="sync-attributes"></a>Atributos de sincronização

Os atributos **Sync01** por meio de **Sync16** são representações de cadeia de caracteres de valores de 32 bits que o Windows Media Player usa quando sincroniza as listas de reprodução com um de até 16 dispositivos portáteis.

## <a name="applies-to"></a>Aplica-se A

-   [Playlists](playlist-attributes-ref.md)

## <a name="remarks"></a>Comentários

Esses são atributos de leitura/gravação. Um valor de zero indica que o Windows Media Player não deve sincronizar a lista de reprodução com o dispositivo associado. Um valor maior que zero indica uma prioridade de sincronização para a lista de reprodução fornecida.

Com base na entrada do usuário, o Windows Media Player define esse atributo para cada uma das listas de reprodução na biblioteca. Quando o Windows Media Player tenta sincronizar uma lista de reprodução com um dispositivo portátil, ele examina cada playlist para comparar os valores dos atributos **Sync**_XX_ que representam a parceria do dispositivo. As listas de reprodução que têm valores menores de **sincronização**_XX_ recebem prioridade de sincronização maior.

Por exemplo, a biblioteca pode conter as quatro listas de reprodução a seguir e os respectivos valores de **sincronização**_XX_ :



| Nome da playlist | Valor de Sync01 |
|---------------|--------------|
| GymMusic. WPL  | 0x0000000D   |
| Relaxar. WPL     | 0x00000020   |
| DriveHome. WPL | 0x00000001   |
| NoGo. WPL      | 0x00000000   |



 

Quando o Windows Media Player sincroniza o dispositivo associado ao atributo, ele sincronizará as listas de reprodução na seguinte ordem:

1.  DriveHome. WPL
2.  GymMusic. WPL
3.  Relaxar. WPL

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

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

 

 





