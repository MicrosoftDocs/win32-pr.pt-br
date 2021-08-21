---
description: Esta seção descreve o design geral de Microsoft Media Foundation. Para obter informações sobre como usar Media Foundation para tarefas de programação específicas, consulte Media Foundation De programação.
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: Arquitetura Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abcc95b1fdb39ad7d0e90e44b66df0dd7eb3c06418c16b4efc452abba4a9738d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974206"
---
# <a name="media-foundation-architecture"></a>Arquitetura Media Foundation

Esta seção descreve o design geral de Microsoft Media Foundation. Para obter informações sobre como usar Media Foundation para tarefas de programação específicas, [consulte Media Foundation Guia de Programação.](media-foundation-programming-guide.md)

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                         | Descrição                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Visão geral da arquitetura Media Foundation dados](overview-of-the-media-foundation-architecture.md)<br/> | Fornece uma visão geral de alto nível da Media Foundation arquitetura.<br/>                                                                                                                                                                                                               |
| [Media Foundation primitivos](media-foundation-primitives.md)<br/>                                     | Descreve algumas interfaces básicas que são usadas em todo o Media Foundation.<br/> Quase todos Media Foundation aplicativos usarão essas interfaces.<br/>                                                                                                                       |
| [Media Foundation Platform APIs](media-foundation-platform-apis.md)<br/>                               | Descreve as principais Media Foundation, como retornos de chamada assíncronos e filas de trabalho.<br/> Alguns aplicativos podem usar interfaces no nível da plataforma. Além disso, plug-ins personalizados, como fontes de mídia e MFTs, usam essas interfaces.<br/>                                       |
| [Media Foundation Pipeline](media-foundation-pipeline.md)<br/>                                         | A Media Foundation de pipeline consiste em fontes de mídia, MFTs e sinks de mídia. A maioria dos aplicativos não chama métodos diretamente na camada de pipeline. Em vez disso, os aplicativos usam uma das camadas mais altas, como a Sessão de Mídia ou o Leitor de Origem e o Sink Writer.<br/> |
| [Sessão de mídia](media-session.md)<br/>                                                                 | A Sessão de Mídia gerencia o fluxo de dados no Media Foundation pipeline.<br/>                                                                                                                                                                                                           |
| [Leitor de Origem](source-reader.md)<br/>                                                                 | O Leitor de Origem permite que um aplicativo receba dados de uma fonte de mídia, sem a necessidade de aplicação chamar as APIs de origem de mídia diretamente. O Leitor de Origem também pode executar a decodificação de fluxos compactados.<br/>                                                            |
| [Caminho de mídia protegida](protected-media-path.md)<br/>                                                   | O caminho de mídia protegido (PMP) fornece um ambiente protegido para reprodução de conteúdo de vídeo premium. Não é necessário usar o PMP ao escrever um Media Foundation aplicativo. <br/>                                                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Media Foundation: conceitos essenciais](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Media Foundation e COM](media-foundation-and-com.md)
</dt> <dt>

[Guia Media Foundation programação do Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 




