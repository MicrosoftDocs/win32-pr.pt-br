---
title: Propriedade IWMPCdromRip ripProgress
description: A propriedade ripProgress Obtém o andamento da cópia de CD como porcentagem concluída.
ms.assetid: 00d4f074-a16d-4c5f-930f-4411b90303f1
keywords:
- Propriedade ripProgress Windows Media Player
- Propriedade ripProgress Windows Media Player, interface IWMPCdromRip
- Interface IWMPCdromRip Windows Media Player, Propriedade ripProgress
topic_type:
- apiref
api_name:
- IWMPCdromRip.ripProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 113b9fc716698156aa4f7731a7b19888e0edf438
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812292"
---
# <a name="iwmpcdromripripprogress-property"></a>Propriedade IWMPCdromRip:: ripProgress

A propriedade **ripProgress** Obtém o andamento da cópia de CD como porcentagem concluída.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 ripProgress {get; set;}
```


```VB

Public ReadOnly Property ripProgress As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o valor de progresso. Os valores de progresso variam de 0 a 100.

## <a name="remarks"></a>Comentários

O valor de progresso representa a porcentagem completa de todo o processo de cópia de CDs. Para determinar o progresso de uma faixa específica, use [IWMPMedia. getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) com **RipProgress** como o nome do atributo. Para obter o índice da faixa que está sendo copiada no momento, chame IWMPPlaylist. getItemInfo com "CurrentRipTrackIndex" como o nome do atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPCdromRip (VB e C#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**Copiando um CD**](ripping-a-cd.md)
</dt> </dl>

 

 





