---
description: Altera o tipo dos traços especificados.
ms.assetid: 8d954a7d-c987-41cf-9933-b2e6bacc9489
title: 'Método IInkAnalyzer:: setstrokestype (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de3f4e56b24226c2f74c6572561082c1d00afc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768389"
---
# <a name="iinkanalyzersetstrokestype-method"></a>Método IInkAnalyzer:: setstrokestype

Altera o tipo dos traços especificados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetStrokesType(
  [in] ULONG      strokeIdCount,
  [in] LONG       *plStrokes,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strokeIdCount* \[ no\]
</dt> <dd>

O número de identificadores de traço em *plStrokes*.

</dd> <dt>

*plStrokes* \[ no\]
</dt> <dd>

Uma matriz que contém os identificadores de traço dos traços aos quais atribuir *StrokeType*.

</dd> <dt>

*StrokeType* \[ no\]
</dt> <dd>

O valor de [**StrokeType**](stroketype.md) a ser atribuído aos traços.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Se o tipo do traço for o [**valor de StrokeType**](stroketype.md) como não **\_ classificado**, o [**IInkAnalyzer**](iinkanalyzer.md) classificará o traço durante a análise de tinta. Caso contrário, o **IInkAnalyzer** usará o tipo definido no traço.

O [**IInkAnalyzer**](iinkanalyzer.md) não define o valor do tipo Stroke como parte da análise de tinta. Para especificar ou alterar o tipo de traço, use o método [**IInkAnalyzer:: Setstroketype**](iinkanalyzer-setstroketype.md) ou **IInkAnalyzer:: setstrokestype**.

Se um traço estiver associado a um [**IContextNode**](icontextnode.md) que não seja um nó de tinta não classificado (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)), esse método move o traço para um nó de tinta não classificado que contém traços do mesmo idioma. Se esse nó de contexto não existir, esse método criará um novo nó de tinta não classificada e adicionará o traço a ele. Um nó de tinta não classificado é um **IContextNode** que é do tipo UnclassifiedInk.

Se esse método mover um traço de um [**IContextNode**](icontextnode.md) que não seja um nó de tinta não classificado, esse método também adicionará a caixa delimitadora do traço à região suja do Ink Analyzer (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Esse método não moverá um traço se o parâmetro *StrokeType* corresponder ao tipo atual do traço.

Se um traço identificado em *strokeIds* não estiver associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método ignorará o identificador.

Se nenhum dos traços especificados identificar um traço associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método retornará sem Atualizar o **IInkAnalyzer**.

Definir o tipo de traço em traços associados a um ContextNode que tenha NodeTypeAndProperties confirmado gerará um InvalidOperationException.

Esse método retorna um código de erro quando *plStrokes* é **nulo**.

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

[**Método IInkAnalyzer:: getstroketype**](iinkanalyzer-getstroketype.md)
</dt> <dt>

[**Método IInkAnalyzer:: setstroketype**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




