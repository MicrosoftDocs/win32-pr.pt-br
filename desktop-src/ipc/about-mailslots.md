---
description: Um maillot é um pseudoarquivo que reside na memória e você usa funções de arquivo padrão para acessá-lo.
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: Sobre Emailslots
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d009b2e667e5feebedeb4b842fc3f6e1630b39069e717ce08f5d0441ebe25aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756514"
---
# <a name="about-mailslots"></a>Sobre Emailslots

Um maillot é um pseudoarquivo que reside na memória e você usa funções de arquivo padrão para acessá-lo. Os dados em uma mensagem maillot podem estar em qualquer formato, mas não podem ser maiores que 424 bytes quando enviados entre computadores. Ao contrário dos arquivos de disco, os emailslots são temporários. Quando todos os tratadores para um maillot são fechados, o maillot e todos os dados que ele contém são excluídos.

Um *servidor maillot* é um processo que cria e possui um maillot. Quando o servidor cria um maillot, ele recebe um alça de maillot. Esse handle deve ser usado quando um processo lê mensagens do maillot. Somente o processo que cria um maillot ou obteve o tratamento por algum outro mecanismo (como herança) pode ler do maillot. Todos os emailslots são locais para o processo que os cria. Um processo não pode criar um maillot remoto.

Um *cliente maillot* é um processo que grava uma mensagem em um maillot. Qualquer processo que tenha o nome de um maillot pode colocar uma mensagem lá. Novas mensagens seguem todas as mensagens existentes no maillot.

Os Emailslots podem transmitir mensagens dentro de um domínio. Se vários processos em um domínio criarem um maillot usando o mesmo nome, cada mensagem endereçada a esse maillot e enviada ao domínio será recebida pelos processos participantes. Como um processo pode controlar um handle maillot do servidor e o handle do cliente recuperado quando o maillot é aberto para uma operação de gravação, os aplicativos podem implementar facilmente um recurso simples de passagem de mensagens dentro de um domínio.

Para enviar mensagens maiores que 424 bytes entre computadores, use [pipes](named-pipes.md) [nomeados ou Windows soquetes.](/windows/desktop/WinSock/windows-sockets-start-page-2)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Nomes do Maillot](mailslot-names.md)
</dt> <dt>

[Operações do Maillot](mailslot-operations.md)
</dt> </dl>

 

 
