---
description: Representa as correspondências de palavras de reconhecimento de manuscrito possíveis para objetos IContextNode.
ms.assetid: a497c140-6166-4309-af0f-851af09015c6
title: Interface IAnalysisAlternate (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8f65b97ca3811212b73c6bdb12e9b889636dd6ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164560"
---
# <a name="ianalysisalternate-interface"></a>Interface IAnalysisAlternate

Representa as correspondências de palavras de reconhecimento de manuscrito possíveis para objetos [**IContextNode**](icontextnode.md) .

## <a name="members"></a>Membros

A interface **IAnalysisAlternate** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisAlternate** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAnalysisAlternate** tem esses métodos.



| Método                                                                          | Descrição                                                                                                                                                          |
|:--------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAlternateNodes**](ianalysisalternate-getalternatenodes.md)               | Recupera os objetos [**IContextNode**](icontextnode.md) que estão associados a essa alternativa.<br/>                                                       |
| [**GetRecognitionConfidence**](ianalysisalternate-getrecognitionconfidence.md) | Recupera um valor que indica o nível de confiança que o [**IInkAnalyzer**](iinkanalyzer.md) tem na precisão do **IAnalysisAlternate**.<br/> |
| [**Reconhecívelstring**](ianalysisalternate-getrecognizedstring.md)           | Recupera o valor de cadeia de caracteres reconhecido do objeto **IAnalysisAlternate** .<br/>                                                                               |
| [**GetStrokeIds**](ianalysisalternate-getstrokeids.md)                         | Recupera os identificadores de traço associados a este **IAnalysisAlternate**.<br/>                                                                    |



 

## <a name="remarks"></a>Comentários

Há muitas variações no manuscrito dos usuários. Por esse motivo, os reconhecedores de manuscrito podem, às vezes, converter manuscrito em texto diferente do que o usuário pretendia. Quando um [**IInkAnalyzer**](iinkanalyzer.md) executa uma análise em uma coleção de traços, o **IInkAnalyzer** encontra o conjunto de palavras mais provável que o manuscrito representa. Além disso, o **IInkAnalyzer** também localiza conjuntos de correspondências de reconhecimento alternativas, que são armazenados em uma coleção [**IAnalysisAlternates**](ianalysisalternates.md) . Para que um usuário aproveite as alternativas de reconhecimento, você deve criar uma interface do usuário que permita ao usuário selecionar o **IAnalysisAlternate** correto.

Os objetos **IAnalysisAlternate** geralmente são obtidos por meio do [**método IInkAnalyzer:: getalternativos**](iinkanalyzer-getalternates.md). O primeiro objeto **IAnalysisAlternate** na coleção é o que o [**IInkAnalyzer**](iinkanalyzer.md) considera como a alternativa mais provável.

Essa interface é equivalente a [System. Windows. Ink. AnalysisCore. AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) na .NET Framework.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer:: getalternations**](iinkanalyzer-getalternates.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

