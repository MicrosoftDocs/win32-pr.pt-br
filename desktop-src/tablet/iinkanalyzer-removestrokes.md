---
description: Remove os traços especificados do IInkAnalyzer.
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: 'Método IInkAnalyzer:: RemoveStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 00f065e01f9a4ff1459988d76fc9393ba24aa894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090521"
---
# <a name="iinkanalyzerremovestrokes-method"></a>Método IInkAnalyzer:: RemoveStrokes

Remove os traços especificados do [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulStrokeIdCount* \[ no\]
</dt> <dd>

O número de identificadores de traço em *plStrokes*.

</dd> <dt>

*plStrokes* \[ no\]
</dt> <dd>

Os identificadores para os traços a serem removidos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Esse método remove os dados de pacote e faz referência aos traços especificados do [**IInkAnalyzer**](iinkanalyzer.md).

Esse método remove os traços do nó de contexto folha que faz referência aos traços. Se qualquer [**IContextNode**](icontextnode.md) não fizer mais referência a traços, esse método excluirá os objetos **IContextNode** e **IContextNode** ancestral que não têm mais nenhum nó filho.

Depois que esse método remove os traços do [**IContextNode**](icontextnode.md), ele atualiza a região suja do objeto [**IInkAnalyzer**](iinkanalyzer.md) (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) para incluir a caixa delimitadora dos traços removidos.

Se um traço identificado em *plStrokes* não estiver associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método ignorará o identificador.

Se nenhum dos traços identificados em *plStrokes* estiver associado ao analisador de tinta, esse método retornará sem Atualizar o [**IInkAnalyzer**](iinkanalyzer.md).

Esse método retorna e o código de erro quando *plStrokes* é nulo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer:: addstroke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer:: RemoveStroke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




