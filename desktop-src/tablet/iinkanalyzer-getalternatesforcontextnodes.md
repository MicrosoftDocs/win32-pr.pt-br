---
description: Recupera alternativas de análise para os nós em uma coleção IContextNodes especificada.
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: 'Método IInkAnalyzer:: GetAlternatesForContextNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 71c53e4a8e0989d836d63db5c5cae8c89d56fcf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090526"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a>Método IInkAnalyzer:: GetAlternatesForContextNodes

Recupera alternativas de análise para os nós em uma coleção [**IContextNodes**](icontextnodes.md) especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAlternatesForContextNodes(
  [in]  IContextNodes      *pContextNodes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pContextNodes* \[ no\]
</dt> <dd>

A coleção [**IContextNodes**](icontextnodes.md) para a qual as alternativas de análise são retornadas.

</dd> <dt>

*ulMaximumAlternates* \[ no\]
</dt> <dd>

O número máximo de alternativas a serem retornadas.

</dd> <dt>

*ppAlternates* \[ fora\]
</dt> <dd>

O objeto [**IAnalysisAlternates**](ianalysisalternates.md) que contém as alternativas de análise.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppAlternates* quando você não precisar mais usar o objeto.

 

O [**IAnalysisAlternate**](ianalysisalternate.md) superior é retornado como a primeira alternativa da coleção.

Os objetos [**IContextNode**](icontextnode.md) em *pContextNodes* não precisam representar áreas adjacentes do documento.

Para cada dica de análise em nós, o [**IInkAnalyzer**](iinkanalyzer.md) retorna apenas a alternativa superior.

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**Método IInkAnalyzer:: getalternations**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer:: ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**Método IInkAnalyzer:: ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

