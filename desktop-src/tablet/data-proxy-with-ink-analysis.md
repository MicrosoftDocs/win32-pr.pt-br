---
description: Conforme mencionado em Visão geral da análise de tinta, a tecnologia de análise de tinta mantém internamente um modelo de documento baseado em árvore para conter resultados e relações de análise.
ms.assetid: 33ba9292-3bc7-41ba-a602-e2fc94cd3a57
title: Proxy de dados com análise de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad79a37a3220351adad56c0a131392e96964714114ba1e0a982833b07bc85077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092775"
---
# <a name="data-proxy-with-ink-analysis"></a>Proxy de dados com análise de tinta

Conforme mencionado em [Visão geral da análise de](ink-analysis-overview.md)tinta, a tecnologia de análise de tinta mantém internamente um modelo de documento baseado em árvore para conter resultados e relações de análise. Se seu aplicativo já tiver um armazenamento de documentos estabelecido diferente, você precisará usar os recursos de análise de tinta projetados para proxy de dados entre modelos de documentos diferentes.

## <a name="types-of-data-proxy"></a>Tipos de proxy de dados

Os recursos de proxy de dados permitem que seu aplicativo:

-   Integrar dados de resultados de análise de volta a um modelo de documento existente.
-   Comunique os resultados anteriores (ou o estado) de volta [**para o InkAnalyzer.**](inkanalyzer.md)
-   Comunique o estado sem tinta no [**InkAnalyzer.**](inkanalyzer.md)
-   Comunique apenas o conjunto mínimo de dados (estado anterior e não tinta) necessário para concluir a operação de análise.
-   Atualize facilmente o modelo de documento de aplicativo interno com resultados de análise.

Há duas abordagens básicas para o proxy de dados de análise de tinta. As diferenças estão nos detalhes de quando e como ocorre a sincronização entre os modelos de documento. A primeira abordagem, atualização síncrona, requer a modificação do modelo de documento de análise de tinta conforme as alterações ocorrem no documento do aplicativo. A segunda abordagem, atualização sob demanda, requer que apenas os dados afetados pelas alterações no modelo de documento do aplicativo sejam passados para o [**InkAnalyzer.**](inkanalyzer.md) Ou seja, somente os dados das partes do modelo de documento análise de tinta que estão na mesma área que as modificações no documento do aplicativo precisam ser passados para o **InkAnalyzer** conforme necessário.

### <a name="synchronous-update"></a>Atualização síncrona

A abordagem de atualização síncrona requer a modificação (criação e exclusão) de nós na coleção de objetos [**ContextNode**](icontextnode.md) do objeto [**InkAnalyzer**](inkanalyzer.md) conforme eles ocorrem no documento do aplicativo. Por exemplo, sempre que uma palavra de texto é adicionada ao aplicativo, um **ContextNode** com estilo **TextWord** correspondente é criado **no InkAnalyzer.** Se o local da palavra de texto na página mudar, o local do **ContextNode** correspondente será atualizado ao mesmo tempo. Esse método é menos eficiente em termos de recursos de computação do que o método sob demanda porque cada alteração de documento envolve uma atualização para **o InkAnalyzer,** mesmo que a alteração não afete a tinta que está sendo analisada.

O exemplo a seguir serve para mostrar como funciona a atualização síncrona. Imagine um aplicativo que tem um modelo de documento existente. Quando o usuário final faz uma alteração no documento, como adicionar novo texto, a alteração é processada da seguinte forma:

1.  O usuário final cria os novos dados.
2.  O aplicativo determina como processar os dados, armazená-los e renderiza-os.
3.  Para fins práticos, as etapas a seguir ocorrem simultaneamente.
    1.  O aplicativo coloca os dados em seu modelo de documento.
    2.  O aplicativo cria um [**InkAnalyzer**](inkanalyzer.md) e atualiza-o. Fazer isso simultaneamente garante que o **InkAnalyzer** sempre tenha as informações mais recentes.
    3.  O aplicativo chama [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) no [**InkAnalyzer para**](inkanalyzer.md) iniciar a análise.
4.  Uma série de eventos será acionada se a alteração envolver tinta e [**o InkAnalyzer**](inkanalyzer.md) determinar novos resultados. Um evento é acionado para cada alteração feita na coleção de [**objetos ContextNode**](icontextnode.md) no **InkAnalyzer.** Esses eventos [**incluem ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**ContextNodeDeleting,**](-ianalysisproxyevents-contextnodedeleting.md) [**ContextNodeMovingToPosition,**](-ianalysisproxyevents-contextnodemovingtoposition.md) [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md), [**ContextNodeLinkAdding,**](-ianalysisproxyevents-contextnodelinkadding.md) [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)e [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md). O aplicativo lida com esses eventos para proxy dos resultados da operação de análise de volta para o modelo de documento, conforme apropriado.
5.  O aplicativo atualiza o layout do documento, exondo os novos dados do modelo de documento.
6.  Os novos dados são renderizados de volta para o usuário final.

### <a name="on-demand-update"></a>Atualização sob demanda

A abordagem sob demanda requer apenas que os dados sejam passados para os [**objetos ContextNode**](icontextnode.md) que estão nas áreas que estão sendo analisadas. Os objetos **ContextNode** necessários são extraídos do modelo de documento do aplicativo logo após a operação de análise ser invocada e, novamente, logo antes de reconciliar os resultados. Embora seja mais complicado implementar do que atualizações síncronas, essa abordagem produz melhores resultados de desempenho.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da análise de tinta](ink-analysis-overview.md)
</dt> <dt>

[**Classe InkAnalyzer (C++)**](inkanalyzer.md)
</dt> <dt>

[**Microsoft.Ink.InkAnalyzer**](/previous-versions/ms583671(v=vs.100))
</dt> <dt>

[**Microsoft.Ink.ContextNode**](/previous-versions/ms551996(v=vs.100))
</dt> </dl>

 

 
