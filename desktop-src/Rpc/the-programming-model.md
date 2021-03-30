---
title: O modelo de programação
description: Nos primórdios da programação do computador, cada programa foi escrito como uma grande parte monolítica, preenchida com instruções GoTo.
ms.assetid: b64d5338-a06a-4a27-bedb-c9011fa5a5a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcc0fd51404290b3d673982001cb3ee91bf1747
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636033"
---
# <a name="the-programming-model"></a>O modelo de programação

Nos primórdios da programação do computador, cada programa foi escrito como uma grande parte monolítica, preenchida com instruções **goto** . Cada programa tinha que gerenciar sua própria entrada e saída para diferentes dispositivos de hardware. À medida que a disciplina de programação amadureceu, esse código monolítico foi organizado em procedimentos, com os procedimentos mais usados empacotados em bibliotecas para compartilhamento e reutilização.

![instruções GoTo monolíticos versus procedimentos empacotados em bibliotecas compartilhadas](images/prog-a06.png)

A linguagem de programação C dá suporte à programação orientada por procedimento. Em C, o procedimento principal está relacionado a todos os outros procedimentos como caixas pretas. Por exemplo, o procedimento principal não consegue descobrir como os procedimentos A, B e X fazem seu trabalho. O procedimento principal só chama outro procedimento; Ele não tem informações sobre como esse procedimento é implementado.

![isolamento de atividades executadas em procedimentos externos](images/prog-a08.png)

Linguagens de programação orientadas a procedimento fornecem mecanismos simples para especificar e escrever procedimentos. Por exemplo, o protótipo de função C-padrão ANSI é um constructo usado para especificar o nome de um procedimento, o tipo do resultado que ele retorna (se houver) e o número, a sequência e o tipo de seus parâmetros. Usar o protótipo de função é uma maneira formal de especificar uma interface entre procedimentos.

O Microsoft RPC se baseia nesse modelo de programação, permitindo que os procedimentos, agrupados em interfaces, residam em processos diferentes do chamador. O Microsoft RPC também adiciona uma abordagem mais formal à definição de procedimento que permite que o chamador e a rotina chamada adotem um contrato para a troca remota de dados e a invocação de funcionalidade. No modelo de programação RPC da Microsoft, as chamadas de função tradicionais são complementadas com dois elementos adicionais.

-   O primeiro elemento é um arquivo. idl/. ACF que descreve precisamente a troca de dados e o mecanismo de passagem de parâmetros entre o chamador e o procedimento chamado.
-   O segundo elemento é um conjunto de APIs de tempo de execução que fornece aos desenvolvedores um controle granular da chamada de procedimento remoto, incluindo aspectos de segurança, gerenciamento de estado no servidor, especificando quais clientes podem se comunicar com o servidor e assim por diante.

 

 




