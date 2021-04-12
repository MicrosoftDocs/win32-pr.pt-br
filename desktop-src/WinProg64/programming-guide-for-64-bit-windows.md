---
title: Guia de programação para o Windows de 64 bits
description: A Microsoft lançou versões de 64 bits do sistema operacional Windows.
ms.assetid: eb31408a-549d-427e-9f8e-9ae96bf6f854
keywords:
- Guia de programação do Windows de 64 bits programação de Windows de 64 bits
- Guia de programação do Windows de 64 bits programação de Windows de 64 bits, home page
- Guia de programação para programação de 64 bits do Windows de 64 bits, consulte Guia de programação do Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb1fa906510d3d9909c5cf888b562deaccb3496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364097"
---
# <a name="programming-guide-for-64-bit-windows"></a>Guia de programação para o Windows de 64 bits

A Microsoft lançou versões de 64 bits do sistema operacional Windows. o Windows de 64 bits foi projetado tendo em mente a compatibilidade. Os desenvolvedores podem garantir que seus aplicativos de 32 bits existentes sejam executados bem em janelas de 64 bits ou aproveitem os benefícios das janelas de 64 bits migrando seus aplicativos.

## <a name="benefits-of-64-bit-windows"></a>Benefícios do Windows de 64 bits

Um sistema operacional de 64 bits dá suporte a muito mais memória física do que um sistema operacional de 32 bits. Por exemplo, a maioria dos sistemas Windows de 32 bits dá suporte a um máximo de 4 gigabytes de memória física, com até 3 gigabytes de espaço de endereço para cada processo, enquanto o Windows de 64 bits dá suporte a até 2 terabytes de memória física com 8 terabytes de espaço de endereço para cada processo. A memória física aumentada inclui os seguintes benefícios para aplicativos:

-   Cada aplicativo pode dar suporte a mais usuários. Todo ou parte de cada aplicativo deve ser replicado para cada usuário, o que requer memória adicional.
-   Cada aplicativo tem um desempenho melhor. A memória física aumentada permite que mais aplicativos sejam executados simultaneamente e permaneçam completamente residentes na memória principal do sistema. Isso reduz ou elimina a penalidade de desempenho de troca de páginas de e para o disco.
-   Cada aplicativo tem mais memória para o armazenamento e a manipulação de dados. Os bancos de dados do podem armazenar mais de seu dado na memória física do sistema. O acesso a dados é mais rápido porque as leituras de disco não são necessárias.
-   Os aplicativos podem manipular grandes quantidades de dados com facilidade e confiança. A composição de vídeo para a imagem de movimento funcionam requer o Windows de 64 bits por esse motivo. A modelagem para aplicativos científicos e financeiros beneficia-se muito das estruturas de dados residentes na memória que não são possíveis em janelas de 32 bits.

Também há benefícios importantes para as empresas:

-   Maior produtividade. Os funcionários de conhecimento podem gastar seu tempo pensando e produzindo, em vez de esperar que o software conclua suas tarefas.
-   Menor custo de propriedade. Cada servidor pode dar suporte a um número maior de usuários e aplicativos, de modo que sua empresa exigirá menos servidores. Isso se traduz diretamente em menos sobrecarga de gerenciamento — um dos custos mais altos em qualquer ambiente computacional.
-   Novas oportunidades de aplicativos. Novos aplicativos podem ser criados sem as barreiras impostas por janelas de 32 bits. Novos aplicativos gráficos tornarão o trabalho mais fácil e agradável. Tarefas de uso intensivo de dados que são impossíveis hoje podem ser feitas com o Windows de 64 bits.

## <a name="in-this-section"></a>Nesta seção

-   [Preparando-se para o Windows de 64 bits](getting-ready-for-64-bit-windows.md)
-   [Criando interfaces compatíveis com 64 bits](designing-64-bit-compatible-interfaces.md)
-   [Executando aplicativos de 32 bits](running-32-bit-applications.md)
-   [Dicas de migração](migration-tips.md)

 

 




