---
description: Move os dados de traço desse IContextNode para o IContextNode especificado.
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: Método IContextNode::ReparentRogkeByIdToNode (IACom.h)
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
ms.openlocfilehash: a915425900bccb15145546658d51d50dcaee14880f8f219bd1908efaa17bd3c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008406"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a>Método IContextNode::ReparentStrkeByIdToNode

Move os dados de traço deste [**IContextNode**](icontextnode.md) para o **IContextNode especificado.**

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lStrkeId* \[ Em\]
</dt> <dd>

O identificador do traço a ser movimentado.

</dd> <dt>

*pContextNodeDestination* \[ Em\]
</dt> <dd>

O [**objeto IContextNode**](icontextnode.md) para o qual mover os dados de traço.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

O objeto [**IContextNode**](icontextnode.md) especificado deve ser um [](context-node-types.md) dos seguintes tipos das constantes Tipos de Nó de Contexto: **InkWord,** **InkDrawing,** **InkBullet** ou **UnclassifiedInk.** Tentar mover um traço para qualquer outro tipo de **objeto IContextNode** resulta em um valor de retorno **de E \_ INVALIDARG.**

Esse método pode ser chamado de qualquer [**objeto IContextNode,**](icontextnode.md) incluindo objetos **IContextNode** não folha de tinta. O traço especificado deve ser referenciado por um dos descendentes desse objeto **IContextNode** ou **E \_ INVALIDARG** é retornado.

Se este [**IContextNode**](icontextnode.md) ou **o IContextNode** em *pContextNodeDestination* for confirmado, **E \_ INVALIDARG** será retornado (consulte [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)).

O analisador de tinta não exclui nós de contexto vazios de sua árvore de resultados em resposta a esse método.

-   Um nó folha de tinta que não faz referência a nenhum dado de traço é um nó vazio.
-   Um nó de contêiner que não faz referência a nenhum nó filho é um nó vazio.

Um nó vazio gerará erros se ele estiver na árvore durante uma operação de análise de tinta. Para remover um nó da árvore do analisador de tinta, chame o método [**IContextNode::D eleteSubNode**](icontextnode-deletesubnode.md) do nó pai (consulte [**IContextNode::GetParentNode**](icontextnode-getparentnode.md)).

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

[**IContextNode::SetRogkes**](icontextnode-setstrokes.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




