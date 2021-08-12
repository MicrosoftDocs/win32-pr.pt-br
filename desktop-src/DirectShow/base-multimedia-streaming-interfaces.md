---
description: Interfaces base de streaming multimídia
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: Interfaces base de streaming multimídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5268855231169c6c0a7ffab02aa5145a7c1813511421b04b2420773e1588ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662916"
---
# <a name="base-multimedia-streaming-interfaces"></a>Interfaces base de streaming multimídia

> [!Note]  
> Essas APIs foram preterida. Os aplicativos devem usar [**o filtro Grabber**](sample-grabber-filter.md) de exemplo ou implementar um filtro personalizado para obter dados de um DirectShow de filtro.

 

As interfaces de streaming multimídia base fornecem uma maneira programática de acessar fluxos multimídia. No entanto, usar uma interface base para acessar um tipo específico de dados pode limitar a quantidade de controle que você tem sobre os dados, portanto, os desenvolvedores de mídia devem criar versões derivadas dessas interfaces que fornecem controle mais poderoso sobre os recursos exclusivos de seu tipo de mídia.



| Interface                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | Define como acessar o objeto de fluxo multimídia de nível mais alto; esse objeto contém e fornece acesso a outros objetos de fluxo. [**O IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) tem métodos que enumeram ou recuperam fluxos específicos, além de verificar a duração total do tempo do fluxo e a busca dentro do fluxo.                                                                                                       |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | Define um objeto de fluxo genérico. Use seus métodos para recuperar um ponteiro para o fluxo, obter informações sobre o fluxo e criar exemplos dos dados de fluxo. Você também pode criar exemplos de fluxo compartilhado, que vários fluxos podem acessar sem duplicar os dados do exemplo.                                                                                                                                                  |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | Controla o comportamento de um exemplo de fluxo específico. Você pode recuperar o fluxo que criou o exemplo, verificar os horários de início e término e o status de conclusão do exemplo e executar uma função definida pelo usuário no próprio exemplo (por meio do [**método Update).**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) Normalmente, o método Update processa os dados de exemplo de maneira apropriada, como renderizar dados de vídeo ou reprodução de dados de áudio. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lista de interfaces de streaming multimídia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



