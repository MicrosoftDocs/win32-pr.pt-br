---
title: O modelo de RPC
description: A RPC (chamada de procedimento remoto) para as linguagens de programação C e C++ foi projetada para ajudar a atender às necessidades dos desenvolvedores que trabalham na próxima geração de software para sistemas operacionais Windows.
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- Chamada de procedimento remoto RPC, descrito, o modelo de RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e72048b12329133fcc8ce4ee82bce266ed29162
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641628"
---
# <a name="the-rpc-model"></a>O modelo de RPC

A RPC (chamada de procedimento remoto) para as linguagens de programação C e C++ foi projetada para ajudar a atender às necessidades dos desenvolvedores que trabalham na próxima geração de software para sistemas operacionais Windows.

O RPC é um mecanismo de IPC (comunicação entre processos) eficiente, robusto, eficiente e seguro que permite a troca de dados e a invocação de funcionalidades que residem em um processo diferente. Esse processo diferente pode estar no mesmo computador, na rede local ou na Internet. Esta seção explica o modelo de programação RPC e o modelo para sistemas distribuídos que podem ser implementados usando RPC.

O RPC dá suporte total ao Windows de 64 bits. Há três tipos de processos: processos nativos de 32 bits, processos nativos de 64 bits e processos de 32 bits em execução no emulador de processo de 32 bits em um sistema de 64 bits (geralmente conhecido como processos WOW64). Para obter mais informações sobre o WOW64, consulte [executando aplicativos de 32 bits](/windows/desktop/WinProg64/running-32-bit-applications). Usando o RPC, os desenvolvedores podem se comunicar de forma transparente entre diferentes tipos de processo; O RPC gerencia automaticamente as diferenças de processo nos bastidores.

O RPC foi inicialmente desenvolvido como uma extensão para uso RPC. Com exceção de alguns de seus recursos avançados, o RPC é interoperável com implementações de outros fornecedores de RPC uso.

Esta seção também fornece uma visão geral dos componentes RPC e sua operação. As informações são apresentadas nos seguintes tópicos:

-   [O modelo de programação](the-programming-model.md)
-   [O modelo para sistemas distribuídos](the-model-for-distributed-systems.md)
-   [Como funciona o RPC](how-rpc-works.md)
-   [Componentes RPC da Microsoft](microsoft-rpc-components.md)

 

 