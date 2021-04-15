---
description: Uma chave mestra é o material de dados chave do qual outras chaves são derivadas.
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: Criando a chave mestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35a6aef52525bdce622355ede4ae9723f7cd8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501551"
---
# <a name="creating-the-master-key"></a>Criando a chave mestra

Uma [*chave mestra*](../secgloss/m-gly.md) é o material de dados chave do qual outras chaves são derivadas. Dependendo do protocolo e do conjunto de codificação usado, a chave mestra pode ter de 5 a 48 bytes de comprimento. Para o CSP do [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) , a chave mestra é criada pelo lado do cliente e transferida para o servidor em um envelope RSA. Para um CSP/Schannel [*Diffie-Hellman*](../secgloss/d-gly.md), a chave mestra é criada com a execução de um Diffie-Hellman troca de chaves.

O código para criar e trocar chaves mestras é demonstrado em:

-   [Código de cliente Diffie-Hellman para criar a chave mestra](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [Código de servidor Diffie-Hellman para criar a chave mestra](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [Código do cliente RSA para criar a chave mestra](rsa-client-code-for-creating-the-master-key.md)
-   [Código do servidor RSA para criar a chave mestra](rsa-server-code-for-creating-the-master-key.md)
-   [Especificando os algoritmos](specifying-the-algorithms.md)

 

 
