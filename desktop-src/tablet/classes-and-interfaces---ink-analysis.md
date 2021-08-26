---
description: Esta seção contém informações sobre as interfaces e classes usadas na análise de tinta. As classes e interfaces de análise de tinta não são compatíveis com a automação.
ms.assetid: 712908e1-2d1d-4e42-8c80-71354b03d318
title: Classes e interfaces de análise de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48335b0e7bf6e29ee90cf1dbf8fb3e96fd761c4b8c0194daaa9d7365fe89d5c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937016"
---
# <a name="ink-analysis-classes-and-interfaces"></a>Classes e interfaces de análise de tinta

Esta seção contém informações sobre as interfaces e classes usadas na análise de tinta. As classes e interfaces de análise de tinta não são compatíveis com a automação.

## <a name="classes"></a>Classes



| Classe                                    | Descrição                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------|
| [**AnalysisRegion**](analysisregion.md) | Implementa a interface [**IAnalysisRegion**](ianalysisregion.md) .<br/> |
| [**InkAnalyzer**](inkanalyzer.md)       | Implementa a interface [**IInkAnalyzer**](iinkanalyzer.md) .<br/>       |



 

## <a name="interfaces"></a>Interfaces



| Interface                                                    | Descrição                                                                                                                                                                                                      |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAnalysisAlternate**](ianalysisalternate.md)             | Representa as correspondências de palavras de reconhecimento de manuscrito possíveis para objetos [**IContextNode**](icontextnode.md) .<br/>                                                                                        |
| [**IAnalysisAlternates**](ianalysisalternates.md)           | Contém uma coleção de objetos que implementam a interface [**IAnalysisAlternate**](ianalysisalternate.md) e que são o resultado da análise de tinta.<br/>                                               |
| [**IAnalysisRegion**](ianalysisregion.md)                   | Expõe métodos e propriedades para uma região que representa uma área de um documento.<br/>                                                                                                                    |
| [**IAnalysisStatus**](ianalysisstatus.md)                   | Representa o status da operação de análise de tinta descrevendo se a análise foi concluída com êxito e se ocorreu algum aviso.<br/>                                                  |
| [**IAnalysisWarning**](ianalysiswarning.md)                 | Representa um aviso ou erro que ocorre durante uma operação de análise de tinta.<br/>                                                                                                                           |
| [**IAnalysisWarnings**](ianalysiswarnings.md)               | Contém uma coleção de objetos que implementam a interface [**IAnalysisWarning**](ianalysiswarning.md) e que são o resultado de uma operação de análise de tinta.<br/>                                      |
| [**IContextLink**](icontextlink.md)                         | Representa uma relação entre dois objetos [**IContextNode**](icontextnode.md) .<br/>                                                                                                                   |
| [**IContextLinks**](icontextlinks.md)                       | Contém uma coleção de objetos que implementam a interface [**IContextLink**](icontextlink.md) .<br/>                                                                                                   |
| [**IContextNode**](icontextnode.md)                         | Representa um nó em uma árvore de objetos que são criados como parte da análise de tinta.<br/>                                                                                                                      |
| [**IContextNodes**](icontextnodes.md)                       | Contém uma coleção de objetos que implementam a interface [**IContextNode**](icontextnode.md) e que são o resultado de uma operação de análise de tinta.<br/>                                              |
| [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)     | Fornece acesso a reconhecedores de manuscrito para uso com a análise de tinta.<br/>                                                                                                                                 |
| [**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)   | Contém uma coleção de objetos que implementam a interface [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) e que representam a capacidade de reconhecer manuscritos, objetos ou gestos.<br/> |
| [**IInkAnalyzer**](iinkanalyzer.md)                         | Fornece acesso à análise de layout, escrita e classificação de desenho e reconhecimento de manuscrito.<br/>                                                                                                  |
| [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) | Expõe um método para avaliar se um objeto [**IContextNode**](icontextnode.md) atende ou falha em um critério especificado.<br/>                                                                              |



 

## <a name="return-values"></a>Valores de retorno

Os métodos na biblioteca COM do Tablet PC retornam valores de **HRESULT**. Salvo indicação em contrário, os significados dos valores **HRESULT** são descritos nesta tabela.



| Valor HRESULT                                   | Descrição                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| S \_ OK<br/>                                | Êxito.<br/>                                                                      |
| \_ponteiro E<br/>                           | Pelo menos um ponteiro (para um parâmetro de entrada ou de saída) é inválido.<br/> |
| E \_ INVALIDARG<br/>                        | O membro tentou passar um argumento inválido.<br/>                              |
| \_exceção de tinta E \_<br/>                    | Exceção ocorreu.<br/>                                                           |
| E \_ OUTOFMEMORY<br/>                       | O sistema não pode alocar memória para concluir a operação.<br/>                      |
| E \_ falha<br/>                              | Ocorreu uma falha não especificada.<br/>                                                 |
| E \_ INVALIDOPERATION<br/>                  | O membro tentou usar uma operação inválida.<br/>                                 |
| modo do TPC \_ E \_ inválido \_<br/>                | O membro tentou usar um modo inválido.<br/>                                      |
| configuração de TPC \_ E \_ inválido \_<br/>       | O membro tentou usar uma configuração inválida.<br/>                             |
| \_Descrição do pacote TPC E \_ inválido \_ \_<br/> | O membro tentou usar uma descrição de pacote inválida.<br/>                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




