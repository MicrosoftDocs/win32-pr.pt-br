---
title: Método IMsTscAxEvents OnUserNameAcquired
description: Chamado quando o nome de usuário foi adquirido pelo controle.
ms.assetid: 0653B28B-2D46-429F-8A36-5656786C0B26
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnUserNameAcquired
- Método OnUserNameAcquired Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnUserNameAcquired
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnUserNameAcquired
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5d77f0eb739daa54f8385112b79f67f279eae9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810435"
---
# <a name="imstscaxeventsonusernameacquired-method"></a>Método IMsTscAxEvents:: OnUserNameAcquired

Chamado quando o nome de usuário foi adquirido pelo controle.

## <a name="syntax"></a>Sintaxe


```C++
void OnUserNameAcquired(
   BSTR bstrUserName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrUserName* 
</dt> <dd>

O nome do usuário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





