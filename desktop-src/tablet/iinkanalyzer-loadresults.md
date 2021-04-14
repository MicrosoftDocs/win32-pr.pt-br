---
description: Carrega os resultados da análise salva no IInkAnalyzer.
ms.assetid: 7634dbe2-1857-497c-81b5-76b92fed862d
title: 'Método IInkAnalyzer:: loadresults (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.LoadResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 76c7fed63b38f1b4fc058fbe7676a727c2d47f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461148"
---
# <a name="iinkanalyzerloadresults-method"></a>Método IInkAnalyzer:: loadresults

Carrega os resultados da análise salva no [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LoadResults(
  [in]          ULONG        ulDataSize,
  [in]          BYTE         *pbSerializedResults,
  [in]          ULONG        ulStrokeIdsCount,
  [in]          LONG         *plOriginalStrokeIds,
  [in]          LONG         *plNewStrokeIds,
  [out, retval] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulDataSize* \[ no\]
</dt> <dd>

O número de bytes em *pbSerializedResults*.

</dd> <dt>

*pbSerializedResults* \[ no\]
</dt> <dd>

Os resultados da análise serializada.

</dd> <dt>

*ulStrokeIdsCount* \[ no\]
</dt> <dd>

O número de identificadores de traço.

</dd> <dt>

*plOriginalStrokeIds* \[ no\]
</dt> <dd>

A matriz de identificadores de traço originais.

</dd> <dt>

*plNewStrokeIds* \[ no\]
</dt> <dd>

A matriz de novos identificadores de traço.

</dd> <dt>

*pfSuccessful* \[ out, retval\]
</dt> <dd>

**Variante \_ TRUE** se o carregamento tiver sido bem-sucedido; caso contrário, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Quando o [**IInkAnalyzer**](iinkanalyzer.md) adiciona um [**IContextNode**](icontextnode.md) dos resultados salvos, ele atribui um novo GUID (identificador global exclusivo) para o **IContextNode** (consulte [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md) e propriedades de nó de [contexto](context-node-properties.md)).

Esse método adiciona os resultados da análise salva à árvore [**IContextNode**](icontextnode.md) existente. Para garantir que os resultados combinados sejam ordenados corretamente, adicione a área que contém os nós de contexto carregados à região suja do objeto [**IInkAnalyzer**](iinkanalyzer.md) (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) e reanalise a tinta.

O método [**IInkAnalyzer:: SaveResults**](iinkanalyzer-saveresults.md), o método [**IInkAnalyzer:: SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)e os métodos do [**método IInkAnalyzer:: SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md) não salvam os dados do pacote junto com os resultados da análise.

Cada identificador em *plOriginalStrokeIds* é o identificador de traço para o traço nos resultados da análise salva. Cada identificador em *plNewStrokeIds* é o novo identificador com o qual substituir o identificador original nos resultados da análise carregada.

Se uma dica de análise salva entrar em conflito com uma dica de análise existente, o [**IInkAnalyzer**](iinkanalyzer.md) não carregará a dica salva, mas carregará o restante dos resultados salvos. No entanto, se o **IInkAnalyzer** carrega resultados para um traço que está dentro da área de uma dica de análise salva que o **IInkAnalyzer** não carrega, o **IInkAnalyzer** adiciona a caixa delimitadora do traço à região suja do objeto **IInkAnalyzer** . Além disso, se o **IInkAnalyzer** carregar resultados para um traço que esteja dentro de uma área de dica de análise existente, o **IInkAnalyzer** também adicionará a caixa delimitadora do traço à região suja do objeto **IInkAnalyzer** . Para obter mais informações sobre dicas de análise, consulte [Propriedades de dica de análise](analysis-hint-properties.md).

Esse método pode gerar os eventos [**\_ IAnalysisProxyEvents:: ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_ IAnalysisProxyEvents:: ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)e [**\_ IAnalysisProxyEvents:: ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) à medida que ele carrega os resultados salvos.

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Método IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**Método IInkAnalyzer:: SaveResults**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**Método IInkAnalyzer:: SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**Método IInkAnalyzer:: SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




