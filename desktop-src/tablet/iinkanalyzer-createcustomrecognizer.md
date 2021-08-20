---
description: Cria um novo nó de reconhecedor personalizado para o IInkAnalyzer.
ms.assetid: bc1dbe88-8f81-48b6-9dd3-8f00e2b6c01c
title: Método IInkAnalyzer::CreateCustomRecognizer (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d30a829107710e1349917ced0a9068108bccd4c120faf3aa96ceed375c350449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043944"
---
# <a name="iinkanalyzercreatecustomrecognizer-method"></a>Método IInkAnalyzer::CreateCustomRecognizer

Cria um novo nó de reconhecedor personalizado para [**o IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateCustomRecognizer(
  [in]  const GUID         *pInkAnalysisRecognizerId,
  [out]       IContextNode **ppContextNode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInkAnalysisRecognizerId* \[ Em\]
</dt> <dd>

O GUID (identificador global exclusivo) do [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) para o qual criar um nó.

</dd> <dt>

*ppContextNode* \[ out\]
</dt> <dd>

Um ponteiro para o [**objeto IContextNode que**](icontextnode.md) representa o novo nó de reconhecedor personalizado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, chame [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em ppContextNode quando você não precisar mais usar o objeto .

 

Esse método cria um [**novo IContextNode com**](icontextnode.md) um tipo de CustomRecognizer (consulte [**IContextNode::GetType**](icontextnode-gettype.md)). Em seguida, ele adiciona o novo nó de reconhecedor personalizado à coleção de subnodos do nó raiz do objeto [**IInkAnalyzer**](iinkanalyzer.md) (consulte [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) e [**Método IInkAnalyzer::GetRootNode**](iinkanalyzer-getrootnode.md)).

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**Método IInkAnalyzer::GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

