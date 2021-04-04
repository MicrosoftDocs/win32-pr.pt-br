---
description: Interfaces de streaming de multimídia base
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: Interfaces de streaming de multimídia base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b715a68bd65a2fa3a3923edf10f0e2d1f6c22edb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930214"
---
# <a name="base-multimedia-streaming-interfaces"></a>Interfaces de streaming de multimídia base

> [!Note]  
> Essas APIs são preteridas. Os aplicativos devem usar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ou implementar um filtro personalizado para obter dados de um grafo de filtro do DirectShow.

 

As interfaces de streaming de multimídia base fornecem uma maneira programática de acessar fluxos de multimídia. No entanto, usar uma interface base para acessar um tipo específico de dados pode limitar a quantidade de controle que você tem sobre os dados; portanto, os desenvolvedores de mídia devem criar versões derivadas dessas interfaces que fornecem um controle mais poderoso sobre os recursos exclusivos de seu tipo de mídia.



| Interface                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | Define como acessar o objeto de fluxo multimídia de nível mais alto; Este objeto contém e fornece acesso a outros objetos de fluxo. [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) tem métodos que enumeram ou recuperam fluxos específicos, bem como verificam a duração total do fluxo e buscam dentro do fluxo.                                                                                                       |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | Define um objeto de fluxo genérico. Use seus métodos para recuperar um ponteiro para o fluxo, obter informações sobre o fluxo e criar exemplos a partir dos dados de fluxo. Você também pode criar amostras de fluxo compartilhado, que vários fluxos podem acessar sem duplicar os dados do exemplo.                                                                                                                                                  |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | Controla o comportamento de um exemplo de fluxo específico. Você pode recuperar o fluxo que criou o exemplo, verificar as horas de início e de término e o status de conclusão do exemplo e executar uma função definida pelo usuário no próprio exemplo (por meio do método [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) ). Normalmente, o método Update processa os dados de exemplo de maneira apropriada, como a renderização de dados de vídeo ou reprodução de dados de áudio. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lista de interfaces de streaming de multimídia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



