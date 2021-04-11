---
description: Contém uma coleção de objetos que implementam a interface IInkAnalysisRecognizer e que representam a capacidade de reconhecer manuscritos, objetos ou gestos.
ms.assetid: d9264c9f-bf75-493e-8e41-57ea69955e6b
title: Interface IInkAnalysisRecognizers (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ba9bbcd029803e613fb27d351de554c013c02616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296392"
---
# <a name="iinkanalysisrecognizers-interface"></a>Interface IInkAnalysisRecognizers

Contém uma coleção de objetos que implementam a interface [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) e que representam a capacidade de reconhecer manuscritos, objetos ou gestos.

## <a name="members"></a>Membros

A interface **IInkAnalysisRecognizers** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IInkAnalysisRecognizers** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IInkAnalysisRecognizers** tem esses métodos.



| Método                                                                               | Descrição                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iinkanalysisrecognizers-getcount.md)                                 | Recupera o número de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) nesta coleção.<br/> |
| [**GetInkAnalysisRecognizer**](iinkanalysisrecognizers-getinkanalysisrecognizer.md) | Recupera o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) no índice especificado.<br/>               |



 

## <a name="remarks"></a>Comentários

O método do [**método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) de [**IInkAnalyzer**](iinkanalyzer.md) retorna uma coleção **IInkAnalysisRecognizers** que contém os reconhecedores de tinta disponíveis no Tablet PC atual.

Para um reconhecedor de linguagem, o método [**IInkAnalysisRecognizer:: Getlinguations**](iinkanalysisrecognizer-getlanguages.md) retorna uma matriz não vazia. Para os reconhecedores de gestores e os reconhecedores de objetos, o método **IInkAnalysisRecognizer:: GetLanguages** retorna uma matriz vazia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

