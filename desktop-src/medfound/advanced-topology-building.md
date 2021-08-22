---
description: Criação de topologia avançada
ms.assetid: 66aa07d8-6756-4d5b-9f0a-24b902da6fa2
title: Criação de topologia avançada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d7f2bba412a698d688bc9d88e9935ed0988cc909931634633a0d75b88c2fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664866"
---
# <a name="advanced-topology-building"></a>Criação de topologia avançada

Esta seção descreve algumas técnicas avançadas para a criação de topologias. Você pode usar essas técnicas se quiser mais controle sobre as topologias que você envia para a sessão de mídia.

Como essas técnicas se destinam a cenários que vão além da funcionalidade fornecida pelo carregador de topologia padrão, muitos dos detalhes dependerão dos requisitos específicos do seu aplicativo. Portanto, esta seção está organizada de forma flexível em relação a subtarefas menores, em vez de cenários completos de ponta a ponta.

O aplicativo de reprodução típico segue estas etapas:

1.  O aplicativo cria uma topologia parcial e a enfileira na sessão de mídia.
2.  A sessão de mídia invoca o carregador de topologia para resolver a topologia.

Se você quiser ir além dos recursos do carregador de topologia, há três abordagens gerais:

-   Crie uma topologia completa. Ao enfileirar a topologia na sessão de mídia, chame [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) com o \_ sinalizador resolution do settopologia do MFSESSION \_ . Esse sinalizador impede que a sessão de mídia tente resolver a topologia.

-   Invoque diretamente o carregador de topologia para resolver a topologia. Em seguida, você pode modificar a topologia completa antes de enfileirar a fila na sessão de mídia.

-   Implemente um carregador de topologia personalizado. Com essa abordagem, você coloca em fila uma topologia parcial, mas a sessão de mídia chama seu carregador personalizado em vez da implementação de Media Foundation padrão. Uma vantagem dessa abordagem é que você pode executar a criação de topologia personalizada dentro do ambiente protegido. (Nesse caso, no entanto, o carregador de topologia deve ser um componente confiável. Para obter mais informações, consulte [proteção de caminho de mídia](protected-media-path.md).)

Esta seção contém os seguintes tópicos.



| Tópico                                                                          | Descrição                                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Carregadores de topologia personalizados](custom-topology-loaders.md)                         | Como fornecer uma implementação personalizada do [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) para a sessão de mídia.          |
| [Associando nós de saída a coletores de mídia](binding-output-nodes-to-media-sinks.md) | Como preparar os nós de saída em uma topologia se você estiver usando o carregador de topologia fora da sessão de mídia. |
| [Adicionando um decodificador a uma topologia](adding-a-decoder-to-a-topology.md)           | Como selecionar um decodificador manualmente e adicioná-lo a uma topologia.                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Topologias](topologies.md)
</dt> </dl>

 

 



