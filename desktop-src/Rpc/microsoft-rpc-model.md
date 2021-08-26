---
title: O modelo RPC
description: A RPC (Chamada de Procedimento Remoto) para as linguagens de programação C e C++ foi projetada para ajudar a atender às necessidades dos desenvolvedores que trabalham na próxima geração de software para Windows sistemas operacionais.
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- RPC de Chamada de Procedimento Remoto , descrito, o modelo RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4c21a9fbbff24f4aafe9bad67186b65f4e3411b507d07953e29f806c6ff73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019706"
---
# <a name="the-rpc-model"></a>O modelo RPC

A RPC (Chamada de Procedimento Remoto) para as linguagens de programação C e C++ foi projetada para ajudar a atender às necessidades dos desenvolvedores que trabalham na próxima geração de software para Windows sistemas operacionais.

O RPC é um mecanismo de IPC (comunicação entre processos) eficiente, eficiente e segura que permite a troca de dados e a invocação de funcionalidades que residem em um processo diferente. Esse processo diferente pode estar no mesmo computador, na rede local ou na Internet. Esta seção explica o modelo de programação RPC e o modelo para sistemas distribuídos que podem ser implementados usando RPC.

O RPC dá suporte total a 64 bits Windows. Há três tipos de processos: processos nativos de 32 bits, processos nativos de 64 bits e processos de 32 bits em execução no emulador de processo de 32 bits em um sistema de 64 bits (geralmente chamado de processos WOW64). Para obter mais informações sobre WOW64, consulte [Executando aplicativos de 32 bits.](/windows/desktop/WinProg64/running-32-bit-applications) Usando RPC, os desenvolvedores podem se comunicar de forma transparente entre diferentes tipos de processo; O RPC gerencia automaticamente as diferenças de processo nos bastidores.

O RPC foi inicialmente desenvolvido como uma extensão para rpc osf. Com exceção de alguns de seus recursos avançados, o RPC é interoperável com implementações de RPC de OSF de outros fornecedores.

Esta seção também fornece uma visão geral dos componentes RPC e sua operação. As informações são apresentadas nos tópicos a seguir:

-   [O modelo de programação](the-programming-model.md)
-   [O modelo para sistemas distribuídos](the-model-for-distributed-systems.md)
-   [Como funciona o RPC](how-rpc-works.md)
-   [Componentes do Microsoft RPC](microsoft-rpc-components.md)

 

 