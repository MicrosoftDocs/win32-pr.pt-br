---
description: Altera o tipo do traço especificado.
ms.assetid: 1608fed1-cd6c-46c3-a35f-3d262279ec2e
title: Método IInkAnalyzer::SetRogkeType (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6d65c01ba3618bad563ee2b8c8a9c4fee3479a12c796b2f2f570832fac1d826c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709026"
---
# <a name="iinkanalyzersetstroketype-method"></a>Método IInkAnalyzer::SetRogkeType

Altera o tipo do traço especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetStrokeType(
  [in] LONG       lStrokeId,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lStrkeId* \[ Em\]
</dt> <dd>

O identificador de traço do traço ao qual atribuir *StrokeType*.

</dd> <dt>

*StrokeType* \[ Em\]
</dt> <dd>

O [**valor strokeType**](stroketype.md) a ser atribuído ao traço.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Se o tipo do traço for o valor [**StrokeType StrokeType**](stroketype.md) **\_ Unclassified**, o [**IInkAnalyzer**](iinkanalyzer.md) classificará o traço durante a análise de tinta. Caso contrário, **o IInkAnalyzer** usará o tipo definido no traço.

O [**IInkAnalyzer**](iinkanalyzer.md) não configura o valor do tipo traço como parte da análise de tinta. Para especificar ou alterar o tipo de traço, use o Método **IInkAnalyzer::SetStrokeType** ou o Método [**IInkAnalyzer::SetRogkesType**](iinkanalyzer-setstrokestype.md).

Se um traço estiver associado a [**um IContextNode**](icontextnode.md) que não é um nó de tinta não classificado (consulte [**IContextNode::GetType**](icontextnode-gettype.md)), esse método moverá o traço para um nó de tinta não classificado que contém traços da mesma linguagem. Se esse nó de contexto não existir, esse método criará um novo nó de tinta não classificado e adiciona o traço a ele. Um nó de tinta não classificado é **um IContextNode** do tipo UnclassifiedInk.

Se esse método mover um traço de [**um IContextNode**](icontextnode.md) que não é um nó de tinta não classificado, esse método também adiciona a caixa delimitador do traço à região suja do analisador de tinta (consulte [**Método IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Esse método não move um traço se o *parâmetro StrokeType* corresponde ao tipo atual do traço.

Definir o tipo de traço em traços associados a um ContextNode que tenha NodeTypeAndProperties confirmado vai aumentar uma InvalidOperationException.

Se o traço especificado não estiver associado ao [**IInkAnalyzer,**](iinkanalyzer.md)esse método retornará sem atualizar **o IInkAnalyzer.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer::GetRogkeType**](iinkanalyzer-getstroketype.md)
</dt> <dt>

[**Método IInkAnalyzer::SetRogkesType**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




