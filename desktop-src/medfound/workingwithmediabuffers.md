---
description: Trabalhando com buffers de mídia DMO
ms.assetid: 6d0c51b8-0d79-4f04-8e90-0cea4f3b1427
title: Trabalhando com buffers de mídia DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c870b3a4a035c71a4dcadf9a38b4c2a150097e7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105784572"
---
# <a name="working-with-dmo-media-buffers"></a>Trabalhando com buffers de mídia DMO

Os dados de entrada são passados para o codec DMOs usando buffers de mídia. Um buffer de mídia é um objeto que implementa a interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) . Você pode implementar uma classe para essa finalidade ou, se você estiver usando o Windows Media Format SDK em seu aplicativo, poderá usar os objetos de buffer que são definidos nesse SDK.

Se você implementar sua própria classe de buffer, tenha cuidado com a forma como a memória de buffer é manipulada. Quando você passa um exemplo de entrada, o DMO mantém uma referência ao buffer até que ele seja concluído com o exemplo. Você pode liberar imediatamente sua referência para a interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) , mas não tem como saber quando o codec não precisa mais de sua referência. Para ter certeza de que a memória é liberada quando o objeto se exclui, você deve implementar sua classe para que ela aloque e libere a memória para o buffer internamente.

Como o DMOs mantém referências a buffers por um período de tempo desconhecido, não é uma questão comum usar um pool limitado de buffers. A solução mais simples é alocar um novo buffer para cada exemplo, embora fazer isso não seja eficiente.

Uma solução melhor é implementar um objeto para gerenciar um pool de buffers. Para fazer isso, escreva o código no método **Release** da sua implementação [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) que chama um método de seu Gerenciador de buffer (em vez de excluir a si mesmo) quando a contagem de referência cai para zero. O Gerenciador de buffer pode manter uma lista de ponteiros para objetos de buffer alocados. Crie um método no Gerenciador de buffer para verificar a lista de buffers livres e retornar um ponteiro para que seu aplicativo possa acessar os buffers quando necessário. Esse método deve criar novos buffers conforme necessário e adicioná-los à lista.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
