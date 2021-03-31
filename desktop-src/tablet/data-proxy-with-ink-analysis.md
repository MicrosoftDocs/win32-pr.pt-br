---
description: Conforme mencionado na visão geral da análise de tinta, a tecnologia de análise de tinta mantém internamente um modelo de documento baseado em árvore para conter resultados e relações de análise.
ms.assetid: 33ba9292-3bc7-41ba-a602-e2fc94cd3a57
title: Proxy de dados com análise de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52717b955625e67f50c20703dd0e84449aa1037f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837029"
---
# <a name="data-proxy-with-ink-analysis"></a>Proxy de dados com análise de tinta

Conforme mencionado na [visão geral da análise de tinta](ink-analysis-overview.md), a tecnologia de análise de tinta mantém internamente um modelo de documento baseado em árvore para conter resultados e relações de análise. Se seu aplicativo já tiver um repositório de documentos estabelecido que seja diferente, você precisará usar os recursos de análise de tinta projetados para dados de proxy entre modelos de documentos diferentes.

## <a name="types-of-data-proxy"></a>Tipos de proxy de dados

Os recursos do proxy de dados permitem que seu aplicativo:

-   Integre dados de resultados de análise de volta a um modelo de documento existente.
-   Comunicar resultados anteriores (ou estado) de volta para o [**InkAnalyzer**](inkanalyzer.md).
-   Comunique o estado de não-tinta no [**InkAnalyzer**](inkanalyzer.md).
-   Comunique somente o conjunto mínimo de dados (estado anterior e não-à tinta) necessário para concluir a operação de análise.
-   Atualize facilmente o modelo de documento do aplicativo interno com os resultados da análise.

Há duas abordagens básicas para o proxy de dados de análise de tinta. As diferenças são formatadas nos detalhes de quando e como ocorre a sincronização entre os modelos de documento. A primeira abordagem, atualização síncrona, requer a modificação do modelo de documento de análise de tinta, pois ocorrem alterações no documento do aplicativo. A segunda abordagem, atualização sob demanda, requer apenas os dados afetados por alterações no modelo de documento do aplicativo a serem passadas para o [**InkAnalyzer**](inkanalyzer.md). Ou seja, somente os dados para as partes do modelo de documento de análise de tinta que estão na mesma área que as modificações no documento de aplicativo precisam ser passados para o **InkAnalyzer** conforme necessário.

### <a name="synchronous-update"></a>Atualização síncrona

A abordagem de atualização síncrona requer a modificação (criação e exclusão) de nós na coleção do objeto [**InkAnalyzer**](inkanalyzer.md) de objetos [**ContextNode**](icontextnode.md) conforme eles ocorrem no documento do aplicativo. Por exemplo, sempre que uma palavra de texto é adicionada ao aplicativo, um **ContextNode** com estilo **textword** correspondente é criado no **InkAnalyzer**. Se o local da palavra de texto na página for alterado, o local do **ContextNode** correspondente será atualizado ao mesmo tempo. Esse método é menos eficiente em termos de recursos de computação do que o método sob demanda, pois cada alteração de documento envolve uma atualização para o **InkAnalyzer**, mesmo que a alteração não afete a tinta que está sendo analisada.

O exemplo a seguir destina-se a mostrar como a atualização síncrona funciona. Imagine um aplicativo que tenha um modelo de documento existente. Quando o usuário final faz uma alteração no documento, como adicionar um novo texto, a alteração é processada da seguinte maneira:

1.  O usuário final cria os novos dados.
2.  O aplicativo determina como processar os dados, os armazena e os renderiza.
3.  Para fins práticos, ocorrem as etapas a seguir simultaneamente.
    1.  O aplicativo coloca os dados em seu modelo de documento.
    2.  O aplicativo cria um [**InkAnalyzer**](inkanalyzer.md) e o atualiza. Fazer isso simultaneamente garante que o **InkAnalyzer** sempre tenha as informações mais recentes.
    3.  O aplicativo chama [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) no [**InkAnalyzer**](inkanalyzer.md) para iniciar a análise.
4.  Uma série de eventos será acionada se a alteração envolver tinta e o [**InkAnalyzer**](inkanalyzer.md) determinar novos resultados. Um evento é acionado para cada alteração feita na coleção de objetos [**ContextNode**](icontextnode.md) no **InkAnalyzer**. Esses eventos incluem [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md), [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md), [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md), [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md), [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)e [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md). O aplicativo manipula esses eventos para fazer o proxy dos resultados da operação de análise de volta para o modelo de documento, conforme apropriado.
5.  O aplicativo atualiza o layout do documento, extraindo os novos dados do modelo de documento.
6.  Os novos dados são processados de volta para o usuário final.

### <a name="on-demand-update"></a>Atualização sob demanda

A abordagem sob demanda requer apenas que os dados sejam passados para os objetos [**ContextNode**](icontextnode.md) que estão nas áreas que estão sendo analisadas. Os objetos **ContextNode** necessários são extraídos do modelo de documento do aplicativo logo após a operação de análise ser invocada e novamente antes de reconciliar os resultados. Embora seja mais complicado implementar do que as atualizações síncronas, essa abordagem gera melhores resultados de desempenho.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da análise de tinta](ink-analysis-overview.md)
</dt> <dt>

[**Classe InkAnalyzer (C++)**](inkanalyzer.md)
</dt> <dt>

[**Microsoft. Ink. InkAnalyzer**](/previous-versions/ms583671(v=vs.100))
</dt> <dt>

[**Microsoft. Ink. ContextNode**](/previous-versions/ms551996(v=vs.100))
</dt> </dl>

 

 
