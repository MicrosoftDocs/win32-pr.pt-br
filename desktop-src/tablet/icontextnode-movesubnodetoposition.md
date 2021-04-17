---
description: Reordena um objeto IContextNode filho especificado para o índice especificado.
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: 'Método IContextNode:: MoveSubNodeToPosition (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.MoveSubNodeToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 398a56cf2c30c93a72e061dfe968de24276888f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763422"
---
# <a name="icontextnodemovesubnodetoposition-method"></a>Método IContextNode:: MoveSubNodeToPosition

Reordena um objeto [**IContextNode**](icontextnode.md) filho especificado para o índice especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSubnodeToMove* \[ no\]
</dt> <dd>

O objeto [**IContextNode**](icontextnode.md) a ser movido.

</dd> <dt>

*ulNewIndex* \[ no\]
</dt> <dd>

O índice da nova posição do subnó.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Retorna **E \_ INVALIDARG** se *pSubnodeToMove* não for um nó filho desse [**IContextNode**](icontextnode.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




