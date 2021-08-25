---
description: Reordena um objeto IContextNode filho especificado para o índice especificado.
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: Método IContextNode::MoveSubNodeToPosition (IACom.h)
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
ms.openlocfilehash: 8d48876be10a2c45daca62b3175a358d31ed128ddd3bcb045c052e2d51308c66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773816"
---
# <a name="icontextnodemovesubnodetoposition-method"></a>Método IContextNode::MoveSubNodeToPosition

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

*pSubnodeToMove* \[ Em\]
</dt> <dd>

O [**objeto IContextNode**](icontextnode.md) a ser movimentado.

</dd> <dt>

*ulNewIndex* \[ Em\]
</dt> <dd>

O índice para a nova posição do subnódeo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Retornará **E \_ INVALIDARG** *se pSubnodeToMove* não for um nó filho deste [**IContextNode.**](icontextnode.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




