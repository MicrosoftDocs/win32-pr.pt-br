---
description: Recupera alternativas de análise para os nós em uma coleção IContextNodes especificada.
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: Método IInkAnalyzer::GetAlternatesForContextNodes (IACom.h)
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
ms.openlocfilehash: bc282906bae70a28f612a8c1fd0a5a67ea1343c73f5ededf0d6c85a8bfd60aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939852"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a>Método IInkAnalyzer::GetAlternatesForContextNodes

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

*pContextNodes* \[ Em\]
</dt> <dd>

A [**coleção IContextNodes**](icontextnodes.md) para a qual as alternativas de análise são retornadas.

</dd> <dt>

*ulMaximumAlternates* \[ Em\]
</dt> <dd>

O número máximo de alternativas a retornar.

</dd> <dt>

*ppAlternates* \[ out\]
</dt> <dd>

O [**objeto IAnalysisAlternates**](ianalysisalternates.md) que contém as alternativas de análise.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, chame [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppAlternates* quando você não precisar mais usar o objeto .

 

O [**IAnalysisAlternate superior**](ianalysisalternate.md) é retornado como a primeira alternativa da coleção.

Os [**objetos IContextNode**](icontextnode.md) *em pContextNodes* não têm que representar áreas adjacentes do documento.

Para cada dica de análise em nós, [**o IInkAnalyzer**](iinkanalyzer.md) retorna apenas a principal alternativa.

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**Método IInkAnalyzer::GetAlternates**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**Método IInkAnalyzer::GetAlternatesForRogkes**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer::ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**Método IInkAnalyzer::ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

