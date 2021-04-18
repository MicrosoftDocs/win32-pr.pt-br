---
description: Modifica o tipo de confirmação, que controla o que o objeto IInkAnalyzer pode alterar sobre o IContextNode.
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: 'Método IContextNode:: Confirm (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Confirm
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3703bb735c0707c412b7c1e41c43819904d83ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750561"
---
# <a name="icontextnodeconfirm-method"></a>Método IContextNode:: Confirm

Modifica o tipo de confirmação, que controla o que o objeto [**IInkAnalyzer**](iinkanalyzer.md) pode alterar sobre o [**IContextNode**](icontextnode.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*confirmable* \[ no\]
</dt> <dd>

O [**Confirmtype**](confirmationtype.md) que é aplicado ao nó.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Use esse método para permitir que o usuário final confirme se o [**IInkAnalyzer**](iinkanalyzer.md) analisou corretamente os traços. Após **IContextNode:: Confirm** ser chamado, o **IInkAnalyzer** não alterará os objetos [**IContextNode**](icontextnode.md) para esses traços durante a análise posterior.

Use **IContextNode:: Confirm** quando o usuário tiver confirmado os resultados da análise e não quiser que o [**IInkAnalyzer**](iinkanalyzer.md) altere um [**IContextNode**](icontextnode.md) durante a análise posterior. Por exemplo, se o usuário gravar a palavra "em" e, em seguida, o aplicativo chamar o [**método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md), o analisador de tinta gerará um nó InkWord com o valor de "to". Se o usuário adicionar "me" após "to", uma palavra e o aplicativo chamarão o **método IInkAnalyzer:: Analyze** novamente, o analisador de tinta poderá remover o nó InkWord anterior e criar um novo nó InkWord com o valor "Tomé". No entanto, se após a primeira chamada para o **método IInkAnalyzer:: Analyze**, o aplicativo chama **IContextNode:: Confirm** no nó InkWord para "to" com o valor de [**confirmtype**](confirmationtype.md) **NodeTypeAndProperties**, antes que o usuário adicione o "me", quando o aplicativo chama o **método IInkAnalyzer:: Analyze**, o analisador de tinta não remove nem altera o nó "para". Em vez disso, o analisador de tinta pode reconhecer dois nós InkWord para "to" e "me".

[**IContextNode**](icontextnode.md) só pode confirmar objetos do tipo InkWord e InkDrawing (consulte [tipos de nó de contexto](context-node-types.md)). **IContextNode:: Confirm** retorna **E \_ INVALIDARG** quando o nó não é um nó folha.

Método [**IInkAnalyzer:: RemoveStroke**](iinkanalyzer-removestroke.md) e [**IInkAnalyzer:: RemoveStrokes**](iinkanalyzer-removestrokes.md) não confirmam nenhum nó do qual eles removem dados de traço.

[**IContextNode:: Setstrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer:: setstrokesvalue**](iinkanalyzer-setstrokestype.md)e [**IInkAnalyzer:: Setstroketype**](iinkanalyzer-setstroketype.md) retornam **Core \_ E \_ INVALIDOPERATION** se o objeto [**IContextNode**](icontextnode.md) já estiver confirmado.

[**IContextNode:: ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) retornará um erro se o nó de origem ou de destino for confirmado.

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

[**IContextNode:: IsDeleted**](icontextnode-isconfirmed.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




