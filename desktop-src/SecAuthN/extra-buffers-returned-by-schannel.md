---
description: O Schannel tem um conjunto bem definido de comportamentos para informações incompletas ou em excesso incluídas nos buffers de entrada para essas funções.
ms.assetid: 5fad1e76-6520-4ff7-b2b0-2cc2061062a1
title: Buffers extras retornados pelo Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c9ce7a468b1b04389ad19f91785b64fb50e74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752230"
---
# <a name="extra-buffers-returned-by-schannel"></a>Buffers extras retornados pelo Schannel

As informações devem ser enviadas entre o cliente e o servidor enquanto um [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) está sendo estabelecido e posteriormente, pois as mensagens seguras são trocadas usando os recursos de criptografia e descriptografia fornecidos pelo Schannel. As funções a seguir são usadas para realizar essas tarefas:

-   [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
-   [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
-   [**DecryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)

O Schannel tem um conjunto bem definido de comportamentos para informações incompletas ou em excesso incluídas nos buffers de entrada para essas funções. As informações são trocadas entre o cliente e o servidor da seguinte maneira:

1.  A parte local interage com o Schannel chamando uma função SSPI e transmitindo informações. Normalmente, as informações foram recebidas da parte remota.
2.  A função retorna um código de status e buffers de saída que contêm informações.
3.  Dependendo do código de status, os buffers de saída são enviados para a parte remota por meio de um mecanismo de comunicação.
4.  A parte remota lê as informações enviadas pela parte local.
5.  O loop se repete, com as partes locais e remotas trocadas. (A parte remota chama uma função SSPI e passa as informações lidas na etapa anterior.)

Tudo funciona conforme o esperado quando o buffer de entrada para a função SSPI contém exatamente as informações necessárias. No entanto, devido à natureza orientada a fluxo de alguns protocolos de comunicação, isso pode não ser o caso; um bloco de informações recebido de uma parte remota pode conter menos dados do que o necessário ou mais dados do que podem ser processados pelo Schannel em uma única chamada de função.

Se o buffer de entrada contiver poucas informações, as funções retornarão s \_ E a \_ mensagem incompleta \_ . O chamador deve obter dados adicionais da parte remota e chamar a função novamente.

Quando os buffers de entrada contiverem muitas informações, o Schannel não tratará isso como um erro. A função processa a maior parte da entrada possível e retorna o código de status para essa atividade de processamento. Além disso, o Schannel indica a presença de informações não processadas nos buffers de entrada, retornando um buffer de saída do tipo SECBUFFER \_ extra. Testar os buffers de saída para esse tipo de buffer é a única maneira de detectar essa situação. O campo **cbBuffer** da estrutura de buffer extra indica quantos bytes de entrada não foram processados.

> [!Note]  
> O campo **pvBuffer** do buffer extra não contém uma cópia dos dados em excesso.

 

Se você receber um buffer extra de uma função SSPI, deverá remover as informações já processadas do buffer de entrada e chamar a função novamente. O Schannel pode, e muitas vezes, retorna apenas o buffer extra e nada mais nos buffers de saída.

 

 
