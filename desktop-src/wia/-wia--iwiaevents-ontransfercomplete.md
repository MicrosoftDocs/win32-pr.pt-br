---
description: Evento que ocorre quando uma transferência de dados é concluída com êxito.
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: Evento Wia.OnTransferComplete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnTransferComplete
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 9095302a2f3fe75e1939ebb979ec4aad4d87b0462a5b40997e5523e7313d98e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209270"
---
# <a name="wiaontransfercomplete-event"></a>Evento Wia.OnTransferComplete

Evento que ocorre quando uma transferência de dados é concluída com êxito.

## <a name="syntax"></a>Sintaxe


```JScript
Wia.OnTransferComplete(
  Item,
  Path
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Item* 
</dt> <dd>

O [**objeto Item**](-wia-item.md) transferido.

</dd> <dt>

*Caminho* 
</dt> <dd>

O caminho e o nome do arquivo da imagem transferida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O WIA notifica o script ou o aplicativo quando uma transferência de dados, imagem ou som é concluída com êxito. Implemente a sub-rotina **objWia** \_ **OnTransferComplete()** para permitir que seu script ou aplicativo responda à conclusão da transferência de dados.

Por exemplo, talvez você queira um script para exibir uma imagem depois que ela for transferida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4.90 ou posterior)</dt> </dl> |



 

 




