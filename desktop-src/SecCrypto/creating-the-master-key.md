---
description: Uma chave mestra é o material de dados de chave do qual outras chaves são derivadas.
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: Criando a chave mestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea47c64348f89563340a4e25d411ed3174ee9d18ba1705d9707eab6b39633b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876526"
---
# <a name="creating-the-master-key"></a>Criando a chave mestra

Uma [*chave mestra*](../secgloss/m-gly.md) é o material de dados de chave do qual outras chaves são derivadas. Dependendo do protocolo e do pacote de criptografia usado, a chave mestra pode ter de 5 a 48 bytes de comprimento. Para o [*CSP rsa*](../secgloss/r-gly.md) / [*schannel,*](../secgloss/s-gly.md) a chave mestra é criada pelo lado do cliente e transferida para o servidor em um envelope RSA. Para um [*CSP Diffie-Hellman*](../secgloss/d-gly.md)/Schannel, a chave mestra é criada executando uma troca Diffie-Hellman chave.

O código para criar e trocar chaves mestras é demonstrado em:

-   [Código do cliente Diffie-Hellman para criar a chave mestra](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [Código do servidor Diffie-Hellman para criar a chave mestra](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [Código do cliente RSA para criar a chave mestra](rsa-client-code-for-creating-the-master-key.md)
-   [Código do servidor RSA para criar a chave mestra](rsa-server-code-for-creating-the-master-key.md)
-   [Especificando os algoritmos](specifying-the-algorithms.md)

 

 
