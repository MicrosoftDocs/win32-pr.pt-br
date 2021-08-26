---
description: Modifica o tipo de confirmação, que controla o que o objeto IInkAnalyzer pode alterar sobre o IContextNode.
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: Método IContextNode::Confirm (IACom.h)
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
ms.openlocfilehash: 248eb78f364f7e938d78846c3e830cc170587961b81dfedcc046e10c59e4fd18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008446"
---
# <a name="icontextnodeconfirm-method"></a>Método IContextNode::Confirm

Modifica o tipo de confirmação, que controla o que o [**objeto IInkAnalyzer**](iinkanalyzer.md) pode alterar sobre [**o IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*confirmType* \[ Em\]
</dt> <dd>

O [**ConfirmationType**](confirmationtype.md) aplicado ao nó.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Use esse método para permitir que o usuário final confirme se [**o IInkAnalyzer**](iinkanalyzer.md) analisou corretamente os traços. Depois **que IContextNode::Confirm** for chamado, **o IInkAnalyzer** não alterará os objetos [**IContextNode**](icontextnode.md) para esses traços durante a análise posterior.

Use **IContextNode::Confirme** quando o usuário confirmou os resultados da análise e não deseja que o [**IInkAnalyzer**](iinkanalyzer.md) altere [**um IContextNode**](icontextnode.md) durante a análise posterior. Por exemplo, se o usuário grava a palavra "para" e, em seguida, o aplicativo chama [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md), o analisador de tinta gera um nó InkWord com o valor de "to". Se o usuário, em seguida, adiciona "me" depois de "a" como uma palavra e o aplicativo chama **IInkAnalyzer::Analyze Method** novamente, o analisador de tinta pode remover o nó InkWord anterior e criar um novo nó InkWord com o valor "tome". No entanto, se após a primeira chamada ao método **IInkAnalyzer::Analyze**, o aplicativo chamar **IContextNode::Confirm** no nó InkWord para "to" com o valor **ConfirmationTypeAndProperties**, antes que o usuário adiciona o "me", quando o aplicativo chamar **IInkAnalyzer::Analyze Method**, o analisador de tinta não removerá nem alterará o nó "para". [](confirmationtype.md) Em vez disso, o analisador de tinta pode reconhecer dois nós InkWord para "to" e "me".

[**IContextNode**](icontextnode.md) só pode confirmar objetos do tipo InkWord e InkDrawing (consulte [Tipos de nó de contexto](context-node-types.md)). **IContextNode::Confirm** retorna **E \_ INVALIDARG** quando o nó não é um nó folha.

[**Método IInkAnalyzer::RemoveStrke**](iinkanalyzer-removestroke.md) e Método [**IInkAnalyzer::RemoveStrkes**](iinkanalyzer-removestrokes.md) não confirmam nenhum nó do qual removem dados de traço.

[**IContextNode::SetStrkes**](icontextnode-setstrokes.md), [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md)e [**IInkAnalyzer::SetStrkeType**](iinkanalyzer-setstroketype.md) **retornarão CORE \_ E \_ INVALIDOPERATION** se o objeto [**IContextNode**](icontextnode.md) já tiver sido confirmado.

[**IContextNode::ReparentStrkeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) retornará um erro se o nó de origem ou de destino for confirmado.

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

[**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




