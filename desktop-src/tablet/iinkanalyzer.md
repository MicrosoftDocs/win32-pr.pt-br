---
description: Fornece acesso à análise de layout, escrita e classificação de desenho e reconhecimento de manuscrito.
ms.assetid: 3a19db78-df14-43c2-9e3e-8cf674aa7b9c
title: Interface IInkAnalyzer (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b37e6d72b87ac31bda7e6c9b0d6f9bf3d35af524eea201e446b50905447404b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939846"
---
# <a name="iinkanalyzer-interface"></a>Interface IInkAnalyzer

Fornece acesso à análise de layout, escrita e classificação de desenho e reconhecimento de manuscrito.

## <a name="members"></a>Membros

A interface **IInkAnalyzer** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IInkAnalyzer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IInkAnalyzer** tem esses métodos.



| Método                                                                                                  | Descrição                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Anular**](iinkanalyzer-abort.md)                                                                     | Cancela a operação de análise atual.<br/>                                                                                                                                           |
| [**Addstroke**](iinkanalyzer-addstroke.md)                                                             | Adiciona dados de traço para um único traço para o **IInkAnalyzer** e atribui o identificador de cultura do thread de entrada ativo ao traço.<br/>                                              |
| [**AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)                                       | Adiciona dados de traço para um único traço para o **IInkAnalyzer** e atribui um identificador de cultura específico ao traço.<br/>                                                             |
| [**Addtraços**](iinkanalyzer-addstrokes.md)                                                           | Adiciona dados de traço para vários traços ao **IInkAnalyzer** e atribui o identificador de cultura do thread de entrada ativo aos traços.<br/>                                            |
| [**AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)                                     | Adiciona dados de traço para vários traços ao **IInkAnalyzer** e atribui o identificador de cultura especificado aos traços.<br/>                                                        |
| [**AddStrokesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)                       | Adiciona dados de traço para vários traços a um nó de reconhecedor personalizado.<br/>                                                                                                                |
| [**AddStrokeToCustomRecognizer**](iinkanalyzer-addstroketocustomrecognizer.md)                         | Adiciona dados de traço para um único traço para um nó de reconhecedor personalizado.<br/>                                                                                                                 |
| [**Analisar**](iinkanalyzer-analyze.md)                                                                 | Executa a análise de tinta síncrona.<br/>                                                                                                                                                |
| [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)                                             | Executa a análise de tinta assíncrona.<br/>                                                                                                                                               |
| [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md)                                                 | Limpa os dados de pacote de traço do **IInkAnalyzer**.<br/>                                                                                                                              |
| [**CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)                                           | Adiciona um novo nó de dica de análise com uma área infinita ao **IInkAnalyzer**.<br/>                                                                                                      |
| [**CreateContextNodes**](iinkanalyzer-createcontextnodes.md)                                           | Cria um objeto [**IContextNodes**](icontextnodes.md) .<br/>                                                                                                                         |
| [**CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)                                   | Cria um novo nó de reconhecedor personalizado para o **IInkAnalyzer**.<br/>                                                                                                                    |
| [**DeleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)                                           | Remove uma dica de análise do **IInkAnalyzer**.<br/>                                                                                                                               |
| [**FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)                                               | Recupera todos os nós folha de tinta.<br/>                                                                                                                                              |
| [**FindInkLeafNodesForStrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)                           | Recupera os nós folha de tinta que contêm os traços especificados.<br/>                                                                                                                  |
| [**FindLeafNodes**](iinkanalyzer-findleafnodes.md)                                                     | Recupera todos os nós folha.<br/>                                                                                                                                                  |
| [**FindNode**](iinkanalyzer-findnode.md)                                                               | Recupera o objeto [**IContextNode**](icontextnode.md) para um GUID (identificador global exclusivo) especificado.<br/>                                                                      |
| [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md)                                                 | Recupera todos os objetos [**IContextNode**](icontextnode.md) do tipo especificado.<br/>                                                                                          |
| [**FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)                             | Recupera todos os objetos [**IContextNode**](icontextnode.md) do tipo especificado que contêm os traços especificados.<br/>                                                       |
| [**FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)                               | Recupera todos os objetos [**IContextNode**](icontextnode.md) do tipo especificado que são descendentes do objeto **IContextNode** especificado.<br/>                            |
| [**FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)                                     | Recupera todos os objetos [**IContextNode**](icontextnode.md) que correspondem aos critérios especificados.<br/>                                                                              |
| [**FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)                   | Recupera todos os objetos [**IContextNode**](icontextnode.md) que correspondem aos critérios especificados e são descendentes do objeto **IContextNode** especificado.<br/>                 |
| [**Getalternativos**](iinkanalyzer-getalternates.md)                                                     | Recupera 10 alternativas de análise para toda a tinta associada ao **IInkAnalyzer**.<br/>                                                                                                |
| [**GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)                       | Recupera alternativas de análise para os nós em uma coleção [**IContextNodes**](icontextnodes.md) especificada.<br/>                                                                     |
| [**GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)                                 | Recupera as alternativas de análise para os traços com os identificadores de traço especificados.<br/>                                                                                              |
| [**GetAnalysisHints**](iinkanalyzer-getanalysishints.md)                                               | Recupera todos os objetos [**IContextNode**](icontextnode.md) da dica de análise que estão anexados ao **IInkAnalyzer**.<br/>                                                        |
| [**GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)                                   | Recupera todos os objetos [**IContextNode**](icontextnode.md) da dica de análise que estão anexados ao **IInkAnalyzer** e que têm o nome especificado.<br/>                       |
| [**GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)                                               | Recupera sinalizadores que controlam como o **IInkAnalyzer** executa a análise de tinta.<br/>                                                                                                      |
| [**GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)                                                   | Recupera a área que foi alterada desde a última operação de análise.<br/>                                                                                                            |
| [**GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)         | Recupera uma coleção ordenada de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .<br/>                                                                              |
| [**GetNodesFromTextRange**](iinkanalyzer-getnodesfromtextrange.md)                                     | Recupera uma coleção de objetos [**IContextNode**](icontextnode.md) que são relevantes para o intervalo de texto especificado para os nós de contexto especificados.<br/>                             |
| [**Reconhecívelstring**](iinkanalyzer-getrecognizedstring.md)                                         | Recupera a cadeia de caracteres de melhor resultado da operação de reconhecimento para toda a árvore de nós de contexto no **IInkAnalyzer**.<br/>                                                           |
| [**GetRootNode**](iinkanalyzer-getrootnode.md)                                                         | Recupera o [**IContextNode**](icontextnode.md) raiz da árvore de contexto do objeto **IInkAnalyzer** .<br/>                                                                            |
| [**GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md)                                         | Recupera o identificador de localidade do traço especificado.<br/>                                                                                                                          |
| [**Getstroketype**](iinkanalyzer-getstroketype.md)                                                     | Recupera o tipo do traço especificado.<br/>                                                                                                                                       |
| [**GetTextRangeFromNodes**](iinkanalyzer-gettextrangefromnodes.md)                                     | Localiza o intervalo de texto na cadeia de caracteres reconhecida que corresponde a uma coleção de objetos [**IContextNode**](icontextnode.md) .<br/>                                                   |
| [**Isanalisar**](iinkanalyzer-isanalyzing.md)                                                         | Recupera um valor que indica se o **IInkAnalyzer** está executando a análise de tinta.<br/>                                                                                             |
| [**Loadresults**](iinkanalyzer-loadresults.md)                                                         | Carrega os resultados da análise salva no **IInkAnalyzer**.<br/>                                                                                                                           |
| [**ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)                                           | Altera a alternativa superior atual para a alternativa especificada e limpa o tipo de confirmação para todos os objetos [**IContextNode**](icontextnode.md) associados à alternativa.<br/> |
| [**ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)           | Altera a alternativa superior atual para o [**IAnalysisAlternate**](ianalysisalternate.md)especificado.<br/>                                                                              |
| [**Reconcile**](iinkanalyzer-reconcile.md)                                                             | Determina quais partes dos resultados da análise foram alteradas durante a análise de tinta em segundo plano.<br/>                                                                                    |
| [**RemoveStroke**](iinkanalyzer-removestroke.md)                                                       | Remove o traço especificado do **IInkAnalyzer**.<br/>                                                                                                                           |
| [**RemoveStrokes**](iinkanalyzer-removestrokes.md)                                                     | Remove os traços especificados do **IInkAnalyzer**.<br/>                                                                                                                          |
| [**SaveResults**](iinkanalyzer-saveresults.md)                                                         | Salva todos os resultados da análise para **um IInkAnalyzer.**<br/>                                                                                                                               |
| [**SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)                                         | Salva os resultados da análise para uma coleção de nós de contexto específica associada a **um IInkAnalyzer.**<br/>                                                                                |
| [**SaveResultsForRogkes**](iinkanalyzer-saveresultsforstrokes.md)                                     | Salva os resultados da análise para os traços especificados associados a **um IInkAnalyzer.**<br/>                                                                                             |
| [**Search**](iinkanalyzer-search.md)                                                                   | Fornece uma pesquisa com base em frases difusas e sem reconhecimento de maiúsculas e minúsculas para traços de escrita analisados e traços de desenho analisados que têm tipos reconhecidos.<br/>                                      |
| [**SearchWithLanguageId**](iinkanalyzer-searchwithlanguageid.md)                                       | Fornece uma pesquisa com base em frases difusas e sem reconhecimento de maiúsculas e minúsculas para traços de escrita analisados e traços de desenho analisados que têm tipos reconhecidos.<br/>                                      |
| [**SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)                                               | Modifica sinalizadores que controlam como o **IInkAnalyzer** executa a análise de tinta.<br/>                                                                                                       |
| [**SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)                                                   | Modifica a área que foi alterada desde a última operação de análise.<br/>                                                                                                             |
| [**SetHighestPriorityInkAnalysisRecognizer**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) | Move o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) especificado para a primeira posição na lista de reconhecedores de tinta do objeto **IInkAnalyzer.**<br/>                      |
| [**SetEntrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md)                                         | Altera o identificador de localidade para o traço especificado.<br/>                                                                                                                           |
| [**SetEntrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md)                                       | Altera o identificador de localidade para os traços especificados.<br/>                                                                                                                          |
| [**SetStrokesType**](iinkanalyzer-setstrokestype.md)                                                   | Altera o tipo dos traços especificados.<br/>                                                                                                                                        |
| [**SetStrokeType**](iinkanalyzer-setstroketype.md)                                                     | Altera o tipo do traço especificado.<br/>                                                                                                                                         |
| [**UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md)                                             | Atualiza os dados do pacote para os traços especificados.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Comentários

**IInkAnalyzer** usa dados de pacote de traço para analisar tinta e não interage diretamente com objetos [**InkDisp Class**](inkdisp-class.md) ou [InkStrkes Collection.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))

Para adicionar ou remover traços ao **IInkAnalyzer** para análise, use um dos métodos a seguir.

-   [**Método IInkAnalyzer::AddStrke**](iinkanalyzer-addstroke.md)
-   [**Método IInkAnalyzer::AddStrkes**](iinkanalyzer-addstrokes.md)
-   [**Método IInkAnalyzer::RemoveStrke**](iinkanalyzer-removestroke.md)
-   [**Método IInkAnalyzer::RemoveStrkes**](iinkanalyzer-removestrokes.md)

Esses métodos atualizam a região suja (consulte [**Método IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)), que é a região para a qual os traços são analisados na próxima operação de análise.

Para analisar tinta, use o [**método IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md) ou o método [**IInkAnalyzer::BackgroundAnalyze.**](iinkanalyzer-backgroundanalyze.md) Durante a análise, **o IInkAnalyzer** executa análise de layout, classificação de traço e reconhecimento de manuscrito.

Para alterar as configurações de análise de layout e classificação de traço, use a [**propriedade Método IInkAnalyzer::SetAnalysisModes.**](iinkanalyzer-setanalysismodes.md)

Durante a análise, **o IInkAnalyzer** recebe vários eventos, incluindo eventos gerados durante a análise em segundo plano. [**\_ IAnalysisProxyEvents dá**](-ianalysisproxyevents.md) suporte aos recursos de proxy de dados do **IInkAnalyzer.** Para obter mais informações, consulte [Proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md). Para interromper o processo de análise de dentro de um manipulador de eventos, chame [**o Método IInkAnalyzer::Abort.**](iinkanalyzer-abort.md)

Para modificar a linguagem que o analisador de tinta usa para reconhecer manuscrito, use o Método [**IInkAnalyzer::SetRogkeLanguageId**](iinkanalyzer-setstrokelanguageid.md) ou o Método [**IInkAnalyzer::SetBonkesLanguageId**](iinkanalyzer-setstrokeslanguageid.md). Para modificar a forma como o analisador de tinta classifica traços específicos, use o Método [**IInkAnalyzer::SetStrokeType**](iinkanalyzer-setstroketype.md) ou o Método [**IInkAnalyzer::SetOsekesType**](iinkanalyzer-setstrokestype.md).

O **IInkAnalyzer** carrega informações para todos os reconhecedores de tinta instalados. O método [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) retorna uma coleção [**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md) que contém cada [**IInkAnalysisRecognizer disponível.**](iinkanalysisrecognizer.md) Se mais de um reconhecedor de tinta dá suporte a uma linguagem específica, use o Método [**IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) para definir qual reconhecedor de tinta lida com traços dessa linguagem.

O uso de dicas de análise pode melhorar a precisão do reconhecimento fornecendo contexto extra ao analisador de tinta. As informações de contexto adicionais podem ajudar o analisador de tinta a limitar o número de resultados de reconhecimento possíveis. Por exemplo, você pode restringir o escopo definindo factoids e palavras esperadas ou estruturando sua entrada em um guia de reconhecimento. Para obter mais informações sobre como fornecer contexto ao analisador de tinta, consulte:

-   [**Método IInkAnalyzer::CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)
-   [**Método IInkAnalyzer::D eleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)
-   [**Método IInkAnalyzer::GetAnalysisHints**](iinkanalyzer-getanalysishints.md)
-   [**Método IInkAnalyzer::GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)

O analisador de tinta representa os resultados da análise como uma cadeia de caracteres ou como uma árvore de [**objetos IContextNode.**](icontextnode.md) Para acessar a cadeia de caracteres reconhecida, use [**o Método IInkAnalyzer::GetRecognizedString**](iinkanalyzer-getrecognizedstring.md). Para acessar a raiz da árvore de nós de contexto, use [**o Método IInkAnalyzer::GetRootNode**](iinkanalyzer-getrootnode.md). O analisador de tinta tem os métodos a seguir para localizar nós de contexto ou texto específicos.

-   [**Método IInkAnalyzer::FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)
-   [**Método IInkAnalyzer::FindInkLeafNodesForStrkes**](iinkanalyzer-findinkleafnodesforstrokes.md)
-   [**Método IInkAnalyzer::FindLeafNodes**](iinkanalyzer-findleafnodes.md)
-   [**Método IInkAnalyzer::FindNode**](iinkanalyzer-findnode.md)
-   [**Método IInkAnalyzer::FindNodesOfType**](iinkanalyzer-findnodesoftype.md)
-   [**Método IInkAnalyzer::FindNodesOfTypeForRogkes**](iinkanalyzer-findnodesoftypeforstrokes.md)
-   [**Método IInkAnalyzer::FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)
-   [**Método IInkAnalyzer::FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
-   [**Método IInkAnalyzer::FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)

Para trabalhar com resultados de análise alternativos, use um dos métodos a seguir.

-   [**Método IInkAnalyzer::GetAlternates**](iinkanalyzer-getalternates.md)
-   [**Método IInkAnalyzer::GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)
-   [**Método IInkAnalyzer::GetAlternatesForRogkes**](iinkanalyzer-getalternatesforstrokes.md)
-   [**Método IInkAnalyzer::ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)
-   [**Método IInkAnalyzer::ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)

Para salvar os resultados da análise, use um dos métodos a seguir.

-   [**Método IInkAnalyzer::SaveResults**](iinkanalyzer-saveresults.md)
-   [**Método IInkAnalyzer::SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)
-   [**Método IInkAnalyzer::SaveResultsForRogkes**](iinkanalyzer-saveresultsforstrokes.md)

Para carregar os resultados salvos, use [**o Método IInkAnalyzer::LoadResults**](iinkanalyzer-loadresults.md).

Para obter mais informações sobre como usar **o IInkAnalyzer para** analisar tinta, consulte Visão [geral da análise de tinta.](ink-analysis-overview.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

