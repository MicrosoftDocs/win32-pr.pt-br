---
description: Esta seção descreve o design geral do Microsoft Media Foundation. Para obter informações sobre como usar Media Foundation para tarefas de programação específicas, consulte Media Foundation Guia de programação.
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: Arquitetura Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0914b0f4c43966edcdc6d30efa7c9dbdbbd4e8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105791086"
---
# <a name="media-foundation-architecture"></a>Arquitetura Media Foundation

Esta seção descreve o design geral do Microsoft Media Foundation. Para obter informações sobre como usar Media Foundation para tarefas de programação específicas, consulte [Media Foundation Guia de programação](media-foundation-programming-guide.md).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                         | Descrição                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Visão geral da arquitetura de Media Foundation](overview-of-the-media-foundation-architecture.md)<br/> | Fornece uma visão geral de alto nível da arquitetura de Media Foundation.<br/>                                                                                                                                                                                                               |
| [Primitivos de Media Foundation](media-foundation-primitives.md)<br/>                                     | Descreve algumas interfaces básicas que são usadas em todo o Media Foundation.<br/> Quase todos os Media Foundation aplicativos usarão essas interfaces.<br/>                                                                                                                       |
| [APIs da plataforma Media Foundation](media-foundation-platform-apis.md)<br/>                               | Descreve as funções de Media Foundation básicas, como retornos de chamada assíncronos e filas de trabalho.<br/> Alguns aplicativos podem usar interfaces de nível de plataforma. Além disso, plug-ins personalizados, como fontes de mídia e MFTs, usam essas interfaces.<br/>                                       |
| [Pipeline de Media Foundation](media-foundation-pipeline.md)<br/>                                         | A camada de pipeline Media Foundation consiste em fontes de mídia, MFTs e coletores de mídia. A maioria dos aplicativos não chama métodos diretamente na camada de pipeline. Em vez disso, os aplicativos usam uma das camadas mais altas, como a sessão de mídia ou o leitor de origem e o gravador de coletor.<br/> |
| [Sessão de mídia](media-session.md)<br/>                                                                 | A sessão de mídia gerencia o fluxo de dados no pipeline de Media Foundation.<br/>                                                                                                                                                                                                           |
| [Leitor de origem](source-reader.md)<br/>                                                                 | O leitor de origem permite que um aplicativo obtenha dados de uma fonte de mídia, sem que o applicating precise chamar as APIs de origem de mídia diretamente. O leitor de origem também pode executar a decodificação de fluxos compactados.<br/>                                                            |
| [Caminho de mídia protegido](protected-media-path.md)<br/>                                                   | O caminho de mídia protegido (PMP) fornece um ambiente protegido para a reprodução de conteúdo de vídeo Premium. Não é necessário usar o PMP ao escrever um aplicativo Media Foundation. <br/>                                                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Media Foundation: conceitos essenciais](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Media Foundation e COM](media-foundation-and-com.md)
</dt> <dt>

[Guia de programação Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 




