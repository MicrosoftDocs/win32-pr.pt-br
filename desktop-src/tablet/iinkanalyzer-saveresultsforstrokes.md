---
description: Salva os resultados da análise para os traços especificados associados a um IInkAnalyzer.
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: 'Método IInkAnalyzer:: SaveResultsForStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1371b056cf01beba75fdcbd427c526ed29d20c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296384"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a>Método IInkAnalyzer:: SaveResultsForStrokes

Salva os resultados da análise para os traços especificados associados a um [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SaveResultsForStrokes(
  [in]          ULONG ulStrokeIdsCount,
  [in]          LONG  *plStrokeIds,
  [in, out]     ULONG *pulSerializedDataSize,
  [out, retval] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulStrokeIdsCount* \[ no\]
</dt> <dd>

O número de identificadores de traço em **plStrokeIds**.

</dd> <dt>

*plStrokeIds* \[ no\]
</dt> <dd>

A matriz de identificadores de traço.

</dd> <dt>

*pulSerializedDataSize* \[ entrada, saída\]
</dt> <dd>

O número de bytes em *ppbSerializedData*.

</dd> <dt>

*ppbSerializedData* \[ out, retval\]
</dt> <dd>

Ponteiro para os dados de análise serializados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) no \* *ppbSerializedData* quando você não precisar mais das informações.

 

Esse método salva os resultados da análise atual para os traços especificados. Esse método salva os objetos de [**IContextNode**](icontextnode.md) folha de tinta que contêm os traços e todos os ancestrais desses nós de contexto. Esse método não salva nenhum dado de traço nem nós de dica de análise. É responsabilidade do seu aplicativo sincronizar os resultados da análise e os dados de traço correspondentes, se ele persistir.

Esse método retorna um código de erro quando um objeto [**IContextNode**](icontextnode.md) a ser salvo é parcialmente preenchido (consulte [**IContextNode:: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).

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

[**Método IInkAnalyzer:: loadresults**](iinkanalyzer-loadresults.md)
</dt> <dt>

[**Método IInkAnalyzer:: SaveResults**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**Método IInkAnalyzer:: SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

