---
description: Recupera todos os objetos IContextNode da dica de análise que estão anexados ao IInkAnalyzer e que têm o nome especificado.
ms.assetid: 15269ee0-055c-424e-be49-945f47e8a77e
title: 'Método IInkAnalyzer:: GetAnalysisHintsByName (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHintsByName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 24c69cd1dd321b5f142fe07b7463941fc0944a2206f1f8d6baf0ebbe8459b6ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719188"
---
# <a name="iinkanalyzergetanalysishintsbyname-method"></a>Método IInkAnalyzer:: GetAnalysisHintsByName

Recupera todos os objetos [**IContextNode**](icontextnode.md) da dica de análise que estão anexados ao [**IInkAnalyzer**](iinkanalyzer.md) e que têm o nome especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAnalysisHintsByName(
  [in]  BSTR          hintName,
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dicaname* \[ no\]
</dt> <dd>

O nome da dica para pesquisa.

</dd> <dt>

*ppAnalysisHints* \[ fora\]
</dt> <dd>

A dica de análise [**IContextNode**](icontextnode.md) objetos no [**IInkAnalyzer**](iinkanalyzer.md) que têm o nome especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md) os valores de retorno.

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppAnalysisHints* quando você não precisar mais usar o objeto.

 

Esse método retornará uma coleção vazia se nenhum nó de dica de análise for anexado ao [**IInkAnalyzer**](iinkanalyzer.md).

Um nó de dica de análise é um [**IContextNode**](icontextnode.md) com um tipo de nó de contexto AnalysisHint (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [tipos de nó de contexto](context-node-types.md)).

Para adicionar informações de contexto à dica, use [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) com o parâmetro *pPropertyDataId* definido como um dos identificadores GLOBALmente exclusivos (GUIDs) nas constantes de [Propriedades da dica de análise](analysis-hint-properties.md) .

Para descobrir quais valores de propriedade são definidos em um nó de contexto, use [**IContextNode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md). Para localizar o valor de uma propriedade, use [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Método IInkAnalyzer:: CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer: método eleteAnalysisHint de:D**](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetAnalysisHints**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

