---
description: Evento que ocorre quando uma transferência de dados é concluída com êxito.
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: Evento WIA. OnTransferComplete
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
ms.openlocfilehash: d33685e0e8fe233f96e9841359e56f759032d17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169547"
---
# <a name="wiaontransfercomplete-event"></a>Evento WIA. OnTransferComplete

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

O objeto [**Item**](-wia-item.md) transferido.

</dd> <dt>

*Caminho* 
</dt> <dd>

O caminho e o nome do arquivo da imagem transferida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O WIA notifica o script ou o aplicativo quando uma transferência de dados, imagem ou som é concluída com êxito. Implemente a sub-rotina **objWia** \_ **OnTransferComplete ()** para permitir que seu script ou aplicativo responda à conclusão da transferência de dados.

Por exemplo, talvez você queira que um script exiba uma imagem depois que ela for transferida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




