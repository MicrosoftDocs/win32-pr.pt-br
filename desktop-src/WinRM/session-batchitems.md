---
title: Session.BatPropriedade chItems (WSManDisp. h)
description: Define e Obtém o número de itens em cada lote de enumeração.
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows da propriedade BatchItems
- Gerenciamento Remoto do Windows da propriedade BatchItems, objeto Session
- objeto de sessão Gerenciamento Remoto do Windows, propriedade BatchItems
topic_type:
- apiref
api_name:
- Session.BatchItems
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59e395eb27be2b922cf9d53e40f1d8cea0fc13a5dcf7b62b95ac606ec8f3f96f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795336"
---
# <a name="sessionbatchitems-property"></a>Session.BatPropriedade chItems

Define e Obtém o número de itens em cada lote de enumeração. Esse valor não pode ser alterado durante uma enumeração. O provedor de recursos pode definir um limite.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Session.BatchItems As long
```



## <a name="property-value"></a>Valor da propriedade

Especifica o número máximo de elementos retornados para cada chamada de rede subjacente ao serviço. O padrão é 20.

## <a name="remarks"></a>Comentários

Esse é um recurso de otimização que controla a frequência com que as chamadas de rede são feitas entre o cliente e o servidor. Atualmente, ele é usado apenas para enumerações. Para obter mais informações sobre como enumerar recursos, consulte [**enumerar**](session-enumerate.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Sessão**](session.md)
</dt> <dt>

[**Enumerar**](session-enumerate.md)
</dt> <dt>

[**Enumerator. ReadItem**](enumerator-readitem.md)
</dt> </dl>

 

 





