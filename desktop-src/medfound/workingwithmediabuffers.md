---
description: Trabalhando com buffers DMO mídia
ms.assetid: 6d0c51b8-0d79-4f04-8e90-0cea4f3b1427
title: Trabalhando com buffers DMO mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 311778898fbfa669a602cd189fb5518f7a2814089a87ed33fba7e303c4327cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236952"
---
# <a name="working-with-dmo-media-buffers"></a>Trabalhando com buffers DMO mídia

Os dados de entrada são passados para os DMOs codec usando buffers de mídia. Um buffer de mídia é um objeto que implementa a interface [**IMediaBuffer.**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) Você pode implementar uma classe para essa finalidade ou, se estiver usando o SDK de Formato de Mídia Windows em seu aplicativo, poderá usar os objetos de buffer definidos nesse SDK.

Se você implementar sua própria classe de buffer, tenha cuidado sobre como a memória do buffer é tratada. Quando você passa um exemplo de entrada, o DMO mantém uma referência ao buffer até que ele seja concluído com o exemplo. Você pode liberar imediatamente sua referência para a interface [**IMediaBuffer,**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) mas não tem como saber quando o codec não precisa mais de sua referência. Para ter certeza de que a memória é liberada quando o objeto se exclui, você deve implementar sua classe para que ela aloce e libera a memória para o buffer internamente.

Como os DMOs mantêm referências a buffers por um período desconhecido, não é uma questão trivial usar um pool limitado de buffers. A solução mais simples é alocar um novo buffer para cada exemplo, embora isso seja ineficiente.

Uma solução melhor é implementar um objeto para gerenciar um pool de buffers. Para fazer isso, escreva o código no método **Release** da implementação [**de IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) que chama um método do gerenciador de buffers (em vez de excluir a si mesmo) quando a contagem de referência cair para zero. O gerenciador de buffers pode manter uma lista de ponteiros para objetos de buffer alocados. Crie um método no gerenciador de buffers para verificar a lista de buffers gratuitos e retornar um ponteiro para que seu aplicativo possa acessar buffers quando necessário. Esse método deve criar novos buffers conforme necessário e adicioná-los à lista.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com DMOs codec](workingwithcodecdmos.md)
</dt> </dl>

 

 
