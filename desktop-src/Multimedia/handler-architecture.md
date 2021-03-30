---
title: Arquitetura do manipulador
description: Arquitetura do manipulador
ms.assetid: 93839b82-09cb-41af-ac0e-a8e9448bf04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b02d0184d364ce438dc28f8219beea01c4868
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005620"
---
# <a name="handler-architecture"></a>Arquitetura do manipulador

A função interna de um manipulador de arquivo ou fluxo é definida pelo próprio manipulador. Para um aplicativo, um manipulador de arquivos normalmente aparece como um módulo para ler e gravar arquivos AVI. Da mesma forma, um manipulador de fluxo aparece como um módulo para ler e gravar um tipo específico de fluxo de dados. A interface de fluxo consistente torna a origem e o destino do fluxo não importantes para o aplicativo que usa o manipulador.

Um manipulador de arquivos fornece acesso a uma fonte de dados que consiste em um ou mais fluxos de dados. Os manipuladores de arquivos normalmente fornecem acesso a arquivos de disco que contêm um ou mais fluxos de dados, e as funções internas do manipulador de arquivos lêem e gravam os dados de multimídia. No entanto, os manipuladores de arquivos podem trabalhar com qualquer fonte de dados, como um canal de transmissão digital contendo vários fluxos de dados intermisturados.

Por outro lado, um manipulador de fluxo processa um tipo de dados e aparece como um fluxo de dados para um aplicativo. Um manipulador de fluxo pode fornecer dados que ele fabrica, ou pode recuperar dados de um arquivo ou de uma fonte externa. Ele fornece seus dados em um formato que seu aplicativo pode usar.

 

 




