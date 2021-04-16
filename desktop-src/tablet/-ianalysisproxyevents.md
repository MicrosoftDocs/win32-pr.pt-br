---
description: Especifica os eventos associados às etapas de proxy de dados de um objeto IInkAnalyzer.
ms.assetid: 57fee525-02e2-4721-b6e5-28112d53db2a
title: Interface _IAnalysisProxyEvents (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b83019cafb6053b9f803c815289d9f9f64d32a5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105754231"
---
# <a name="_ianalysisproxyevents-interface"></a>\_Interface IAnalysisProxyEvents

Especifica os eventos associados às etapas de proxy de dados de um objeto [**IInkAnalyzer**](iinkanalyzer.md) .

-   [Eventos](/windows)

### <a name="events"></a>Eventos

A interface **\_ IAnalysisProxyEvents** tem esses eventos.



| Evento                                                                                      | Descrição                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md)                     | Ocorre depois que o [**IInkAnalyzer**](iinkanalyzer.md) cria um objeto [**IContextNode**](icontextnode.md) .<br/>                                                                  |
| [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md)                   | Ocorre antes de [**IInkAnalyzer**](iinkanalyzer.md) excluir um objeto [**IContextNode**](icontextnode.md) .<br/>                                                                 |
| [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)               | Ocorre antes de o [**IInkAnalyzer**](iinkanalyzer.md) adicionar um objeto [**IContextLink**](icontextlink.md) entre dois objetos [**IContextNode**](icontextnode.md) .<br/>           |
| [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)           | Ocorre antes de [**IInkAnalyzer**](iinkanalyzer.md) excluir um objeto [**IContextLink**](icontextlink.md) entre dois objetos [**IContextNode**](icontextnode.md) .<br/>         |
| [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)   | Ocorre antes de o [**IInkAnalyzer**](iinkanalyzer.md) mover um objeto [**IContextNode**](icontextnode.md) para uma nova posição dentro de sua coleção de subnós do nó pai.<br/> |
| [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) | Ocorre depois que o [**IInkAnalyzer**](iinkanalyzer.md) atualiza uma ou mais propriedades de um objeto [**IContextNode**](icontextnode.md) .<br/>                                        |
| [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)             | Ocorre antes de o [**IInkAnalyzer**](iinkanalyzer.md) mover um objeto [**IContextNode**](icontextnode.md) alterando seu nó pai.<br/>                                       |
| [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md)         | Ocorre antes de o [**IInkAnalyzer**](iinkanalyzer.md) reconciliar os resultados da análise para que um aplicativo possa sincronizar dados com o **IInkAnalyzer**.<br/>                      |
| [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md)                   | Ocorre antes de o [**IInkAnalyzer**](iinkanalyzer.md) executar a análise dentro da região de um objeto [**IContextNode**](icontextnode.md) parcialmente populado.<br/>               |
| [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)                         | Ocorre quando o [**IInkAnalyzer**](iinkanalyzer.md) move um traço de um objeto [**IContextNode**](icontextnode.md) para outro.<br/>                                           |



 

## <a name="remarks"></a>Comentários

Use esses eventos quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md). Para obter mais informações sobre como sincronizar os dados do aplicativo com o **IInkAnalyzer**, consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).

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

[**Método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[\_IAnalysisEvents](-ianalysisevents.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

