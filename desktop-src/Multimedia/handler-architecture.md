---
title: Arquitetura do manipulador
description: Arquitetura do manipulador
ms.assetid: 93839b82-09cb-41af-ac0e-a8e9448bf04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c0da7846f31c94202d8d50ac0566c87ef5db085a0b9efb3f9250468346512db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141089"
---
# <a name="handler-architecture"></a>Arquitetura do manipulador

A função interna de um manipulador de arquivo ou fluxo é definida pelo próprio manipulador. Para um aplicativo, um manipulador de arquivos normalmente aparece como um módulo para ler e gravar arquivos AVI. Da mesma forma, um manipulador de fluxo aparece como um módulo para ler e gravar um tipo específico de fluxo de dados. A interface de fluxo consistente torna a origem e o destino do fluxo sem importância para o aplicativo que usa o manipulador.

Um manipulador de arquivos fornece acesso a uma fonte de dados que consiste em um ou mais fluxos de dados. Os manipuladores de arquivos normalmente fornecem acesso a arquivos de disco que contêm um ou mais fluxos de dados e as funções internas do manipulador de arquivos leem e escrevem os dados multimídia. No entanto, os manipuladores de arquivos podem trabalhar com qualquer fonte de dados, como um canal de transmissão digital que contém vários fluxos de dados intermenuados.

Por outro lado, um manipulador de fluxo processa um tipo de dados e aparece como um fluxo de dados para um aplicativo. Um manipulador de fluxo pode fornecer dados que fabrica ou pode recuperar dados de um arquivo ou de uma fonte externa. Ele fornece seus dados em um formato que seu aplicativo pode usar.

 

 




