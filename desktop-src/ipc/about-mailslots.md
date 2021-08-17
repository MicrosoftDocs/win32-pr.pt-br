---
description: Um processador de processadores é um pseudofile que reside na memória e você usa funções de arquivo padrão para acessá-lo.
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: Sobre processadores de informações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d009b2e667e5feebedeb4b842fc3f6e1630b39069e717ce08f5d0441ebe25aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756514"
---
# <a name="about-mailslots"></a>Sobre processadores de informações

Um processador de processadores é um pseudofile que reside na memória e você usa funções de arquivo padrão para acessá-lo. Os dados em uma mensagem do processador de mensagens podem estar em qualquer formato, mas não podem ter mais de 424 bytes quando enviados entre computadores. Ao contrário dos arquivos de disco, os processadores são temporários. Quando todos os identificadores para um processador de processadores são fechados, o processador de processadores e todos os dados que ele contém são excluídos.

Um *servidor do processador de processadores* é um processo que cria e possui um processador de processadores. Quando o servidor cria um processador de processadores, ele recebe um identificador de processador de processadores. Esse identificador deve ser usado quando um processo lê mensagens do processador de mensagem. Somente o processo que cria um processador de processadores ou obteve o identificador por algum outro mecanismo (como a herança) pode ler do processador de itens. Todos os processadores são locais para o processo que os cria. Um processo não pode criar um processador de processadores remoto.

Um *cliente do processador* de mensagens é um processo que grava uma mensagem em um processador de mensagens. Qualquer processo que tenha o nome de um processador de mensagens pode colocar uma mensagem lá. Novas mensagens seguem qualquer mensagem existente no processador de mensagens.

Os processadores podem transmitir mensagens em um domínio. Se vários processos em um domínio criarem um processador de mensagens usando o mesmo nome, cada mensagem que é endereçada a esse processador e enviado ao domínio é recebida pelos processos participantes. Como um processo pode controlar tanto um identificador de processador de processadores quanto o identificador do cliente recuperado quando o processador de mensagens é aberto para uma operação de gravação, os aplicativos podem facilmente implementar uma facilidade de transmissão de mensagem simples em um domínio.

para enviar mensagens com mais de 424 bytes entre computadores, use [pipes nomeados](named-pipes.md) ou [soquetes de Windows](/windows/desktop/WinSock/windows-sockets-start-page-2) em vez disso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Nomes de processador de processadores](mailslot-names.md)
</dt> <dt>

[Operações de processador de processadores](mailslot-operations.md)
</dt> </dl>

 

 
