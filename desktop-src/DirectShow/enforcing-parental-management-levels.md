---
description: Impondo níveis de gerenciamento de pais
ms.assetid: ad996a03-e94e-4743-90a2-aa390984a231
title: Impondo níveis de gerenciamento de pais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7548721613c36369aaa34e5b5a62b665100e9495
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456782"
---
# <a name="enforcing-parental-management-levels"></a>Impondo níveis de gerenciamento de pais

Qualquer título ou parte de um título em um disco DVD-Video pode ser atribuído a um nível de gerenciamento pai genérico (PML) de 1 a 8. Quando o navegador de DVD está lendo o conteúdo que tem um PML, ele é considerado em um *bloco pai*. Um bloco pai pode consistir em parte de um capítulo, vários capítulos ou vários títulos. Um aplicativo de DVD destinado a um mercado internacional não deve embutir em código um determinado sistema de classificação em sua lógica de gerenciamento de pais.

O DVD Navigator em si não impõe o PMLs; Ele simplesmente informa seu aplicativo quando encontra informações de PML no disco. Por padrão, ele ignora essas informações no disco e reproduz o conteúdo de nível mais alto. Para impor o PMLs, seu aplicativo deve implementar alguma forma de lógica de controle de senha que associa os usuários aos níveis, instruindo o navegador de DVD a enviar notificações de evento PML (chamando o método [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) na inicialização, com os parâmetros DVD \_ NotifyParentalLevelChange e **true**) e responder a esses eventos para permitir ou impedir o acesso conforme apropriado.

Um título de DVD pode ter um PML geral, mas os autores de disco podem dar a determinadas seções do título um PMLs mais restrito ou mais restritivo. Eles são chamados de comandos PML temporários; esses comandos sempre contêm duas instruções de ramificação: uma para seguir se o comando PML temporário for aceito pelo aplicativo de Player e o outro para seguir se o comando for rejeitado. A sequência de eventos é a seguinte: O navegador de DVD está lendo o conteúdo de vídeo (domínio de título de DVD) quando encontra um comando PML temporário no disco. Ele verifica seu sinalizador interno para ver se o aplicativo solicitou que seja notificado desse evento. Se o sinalizador não estiver definido, o DVD continuará a ser reproduzido, seguindo a ramificação "alteração de nível de pai rejeitada" especificada no disco. Se o sinalizador for definido, o DVD enviará um \_ evento de alteração de nível pai de DVD do EC \_ \_ \_ para o aplicativo e aguardará um estado de pausa até obter uma resposta. Quando seu aplicativo recebe o evento, ele usa sua própria lógica para determinar se o comando deve ser aceito. Em seguida, ele chama [**IDvdControl2:: AcceptParentalLevelChange**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-acceptparentallevelchange) com um argumento de **true** ou **false**. Se **for true**, o navegador de DVD retomará a reprodução, seguindo a ramificação "alteração de nível de pai aceita" especificada no disco. Caso contrário, ele retoma a reprodução e segue a ramificação "alteração de nível de pai rejeitada".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



