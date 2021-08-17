---
title: O estado do pipe
description: No servidor, o compilador MIDL cria uma variável de estado que coordena os procedimentos de push, pull e Alloc.
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d12c5ef5549d89f3aee2833599f5930f2617478e66e16c3b78188eb63a40e7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924066"
---
# <a name="the-pipe-state"></a>O estado do pipe

No servidor, o compilador MIDL cria uma variável de *estado* que coordena os procedimentos de push, pull e Alloc. No lado do cliente, o desenvolvedor deve criar a variável de *estado* . Portanto, a variável de *estado* é local para ambos os lados — ou seja, o cliente e o servidor mantêm seu próprio estado de pipe. O código stub do servidor mantém a variável de estado no servidor. Você não deve tentar modificar seu conteúdo diretamente. O cliente deve inicializar os campos na estrutura de controle de pipe e manter sua variável de *estado* . Ele usa a variável de *estado* para identificar onde localizar ou colocar dados.

A variável de *estado* do cliente pode ser tão simples quanto um identificador de arquivo, se você estiver transferindo dados de um arquivo para outro. Ele também pode ser um inteiro que aponta para um elemento em uma matriz. Ou você pode definir uma estrutura de estado bastante complexa para executar tarefas adicionais, como coordenar as rotinas de push e pull em um \[ parâmetro [in](/windows/desktop/Midl/in)e [out](/windows/desktop/Midl/out-idl) \] .

 

 