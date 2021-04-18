---
description: Move os dados de traço deste IContextNode para o IContextNode especificado.
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: 'Método IContextNode:: ReparentStrokeByIdToNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ReparentStrokeByIdToNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3984153a0551de999563b8775ceb5acba1696e39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789607"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a>Método IContextNode:: ReparentStrokeByIdToNode

Move os dados de traço deste [**IContextNode**](icontextnode.md) para o **IContextNode** especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lStrokeId* \[ no\]
</dt> <dd>

O identificador do traço a ser movido.

</dd> <dt>

*pContextNodeDestination* \[ no\]
</dt> <dd>

O objeto [**IContextNode**](icontextnode.md) para o qual mover os dados de traço.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

O objeto [**IContextNode**](icontextnode.md) especificado deve ser um dos tipos a seguir das constantes [de tipos de nó de contexto](context-node-types.md) : **InkWord**, **InkDrawing**, **InkBullet** ou **UnclassifiedInk**. A tentativa de mover um traço para qualquer outro tipo de objeto **IContextNode** resulta em um valor de retorno de **E \_ INVALIDARG**.

Esse método pode ser chamado de qualquer objeto [**IContextNode**](icontextnode.md) , incluindo objetos **IContextNode** folha que não são de tinta. O traço especificado deve ser referenciado por um dos descendentes deste objeto **IContextNode** ou **E \_ INVALIDARG** é retornado.

Se esse [**IContextNode**](icontextnode.md) ou **IContextNode** em *pContextNodeDestination* for confirmado, **e \_ INVALIDARG** será retornado (consulte [**IContextNode::**](icontextnode-isconfirmed.md)IsDeleted).

O analisador de tinta não exclui nós de contexto vazios de sua árvore de resultados em resposta a esse método.

-   Um nó folha de tinta que não faz referência a nenhum dado de traço é um nó vazio.
-   Um nó de contêiner que não faz referência a nós filho é um nó vazio.

Um nó vazio gera erros se estiver na árvore durante uma operação de análise de tinta. Para remover um nó da árvore do analisador de tinta, chame o método [**IContextNode::D eletesubnode**](icontextnode-deletesubnode.md) do nó pai (consulte [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md)).

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

[**IContextNode:: settraços**](icontextnode-setstrokes.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




