---
title: Guia de programação para 64 bits Windows
description: A Microsoft lançou versões de 64 bits do Windows operacional.
ms.assetid: eb31408a-549d-427e-9f8e-9ae96bf6f854
keywords:
- Guia de programação Windows de 64 bits Windows 64 bits
- Guia de programação Windows de 64 bits Windows de 64 bits, home page
- guia de programação para programação Windows 64 bits Windows programação de 64 bits Consulte Guia de programação Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8af8c2cb6340bd7617dd7e712f89cb5d9485c65d3d56258850c1a885df1f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743463"
---
# <a name="programming-guide-for-64-bit-windows"></a>Guia de programação para 64 bits Windows

A Microsoft lançou versões de 64 bits do Windows operacional. Os Windows de 64 bits foram projetados com a compatibilidade em mente. Os desenvolvedores podem garantir que seus aplicativos de 32 bits existentes são executados bem em um Windows de 64 bits ou aproveitar os benefícios do Windows de 64 bits migrando seus aplicativos.

## <a name="benefits-of-64-bit-windows"></a>Benefícios de 64 bits Windows

Um sistema operacional de 64 bits dá suporte a muito mais memória física do que um sistema operacional de 32 bits. Por exemplo, a maioria dos sistemas Windows de 32 bits dá suporte a um máximo de 4 gigabytes de memória física, com até 3 gigabytes de espaço de endereço para cada processo, enquanto o Windows de 64 bits dá suporte a até 2 terabytes de memória física com 8 terabytes de espaço de endereço para cada processo. O aumento da memória física inclui os seguintes benefícios para aplicativos:

-   Cada aplicativo pode dar suporte a mais usuários. Todo ou parte de cada aplicativo deve ser replicado para cada usuário, o que requer memória adicional.
-   Cada aplicativo tem um melhor desempenho. O aumento da memória física permite que mais aplicativos executem simultaneamente e permaneçam completamente residentes na memória principal do sistema. Isso reduz ou elimina a penalidade de desempenho da troca de páginas de e para o disco.
-   Cada aplicativo tem mais memória para armazenamento e manipulação de dados. Os bancos de dados podem armazenar mais de seus dados na memória física do sistema. O acesso a dados é mais rápido porque as leituras de disco não são necessárias.
-   Os aplicativos podem manipular grandes quantidades de dados facilmente e de forma mais confiável. A composição de vídeo para o trabalho de imagens de movimento requer Windows de 64 bits por esse motivo. A modelagem para aplicativos científicos e financeiros se beneficia muito de estruturas de dados residentes na memória que não são possíveis em 32 bits Windows.

Também há benefícios importantes para as empresas:

-   Maior produtividade. Os trabalhadores de conhecimento podem gastar seu tempo pensando e produzindo, em vez de esperar que o software termine suas tarefas.
-   Menor custo de propriedade. Cada servidor pode dar suporte a um número maior de usuários e aplicativos, portanto, sua empresa exigirá menos servidores. Isso se traduz diretamente em menos sobrecarga de gerenciamento– um dos custos mais altos em qualquer ambiente de computação.
-   Novas oportunidades de aplicativo. Novos aplicativos podem ser projetados sem as barreiras impostas por 32 bits Windows. Novos aplicativos gráficos tornarão o trabalho mais fácil e mais agradável. Tarefas com uso intensivo de dados que são impossíveis hoje podem ser feitas com tarefas de 64 bits Windows.

## <a name="in-this-section"></a>Nesta seção

-   [Preparando-se para 64 bits Windows](getting-ready-for-64-bit-windows.md)
-   [Projetando interfaces compatíveis de 64 bits](designing-64-bit-compatible-interfaces.md)
-   [Executando aplicativos de 32 bits](running-32-bit-applications.md)
-   [Migração Dicas](migration-tips.md)

 

 




