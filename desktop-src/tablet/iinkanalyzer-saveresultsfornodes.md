---
description: Salva os resultados da análise de uma coleção de nós de contexto específica associada a um IInkAnalyzer.
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: 'Método IInkAnalyzer:: SaveResultsForNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eb628fafb9bf479e6a011137105005e541180aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090518"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a>Método IInkAnalyzer:: SaveResultsForNodes

Salva os resultados da análise de uma coleção de nós de contexto específica associada a um [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SaveResultsForNodes(
  [in]      IContextNodes *pContextNodes,
  [in, out] ULONG         *pulSerializedDataSize,
  [out]     BYTE          **ppbSerializedData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pContextNodes* \[ no\]
</dt> <dd>

A coleção [**IContextNode**](icontextnode.md) para a qual salvar os resultados da análise.

</dd> <dt>

*pulSerializedDataSize* \[ entrada, saída\]
</dt> <dd>

O número de bytes em *ppbSerializedData*.

</dd> <dt>

*ppbSerializedData* \[ fora\]
</dt> <dd>

Ponteiro para os dados de análise serializados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) no \* *ppbSerializedData* quando você não precisar mais das informações.

 

Esse método salva os resultados da análise atual para os objetos [**IContextNode**](icontextnode.md) no *pContextNodes* e todos os seus nós de contexto ancestral e descendente. Esse método não salva nenhum dado de traço. É responsabilidade do seu aplicativo sincronizar os resultados da análise e os dados de traço correspondentes, se ele persistir.

Se o objeto [**IContextNode**](icontextnode.md) a ser salvo for apenas parcialmente preenchido, esse método retornará um código de erro (consulte [**IContextNode:: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).

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

[**Método IInkAnalyzer:: SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

