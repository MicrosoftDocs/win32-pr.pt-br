---
description: Associa os traços especificados a este IContextNode.
ms.assetid: 5ce8893a-da59-4cec-a349-d5ffc4f43905
title: 'Método IContextNode:: setstrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be7fd1645af70e34c747894bc8ab4317b08e2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772603"
---
# <a name="icontextnodesetstrokes-method"></a>Método IContextNode:: setstrokes

Associa os traços especificados a este [**IContextNode**](icontextnode.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetStrokes(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulStrokeIdsCount* \[ no\]
</dt> <dd>

O número de identificadores de traço em *plStrokeIds*.

</dd> <dt>

*plStrokeIds* \[ no\]
</dt> <dd>

Os identificadores dos traços a serem associados a este [**IContextNode**](icontextnode.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Esse método não atualiza a região suja do Ink Analyzer (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Use esse método quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md). Use esse método para atribuir dados de traço a um nó de contexto específico. Para obter mais informações sobre como sincronizar os dados do aplicativo com o **IInkAnalyzer**, consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).

Se qualquer um dos traços especificados já estiver associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método retornará **E \_ INVALIDARG**.

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

[**Método IInkAnalyzer:: addstroke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokeToCustomRecognizer**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**Método IInkAnalyzer:: RemoveStroke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Método IInkAnalyzer:: RemoveStrokes**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**IContextNode:: getstrokeid**](icontextnode-getstrokeid.md)
</dt> <dt>

[**IContextNode::GetStrokeIds**](icontextnode-getstrokeids.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




