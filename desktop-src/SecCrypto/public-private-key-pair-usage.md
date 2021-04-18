---
description: Todas as operações normais do RSA/Schannel e do Diffie-Hellman/Schannel usam o \_ par de chaves públicas/privadas do keyexchange.
ms.assetid: e12afdbb-7ba8-444e-a43f-e262b481a353
title: Uso do par de chaves pública/privada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dba78c487c433875ed23ce3f2f3c87a86b07c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105800077"
---
# <a name="publicprivate-key-pair-usage"></a>Uso do par de chaves pública/privada

Todas as operações normais do [*RSA*](../secgloss/r-gly.md)/Schannel e do [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel usam o \_ par de [*chaves públicas/privadas*](../secgloss/p-gly.md)do keyexchange. Para fornecer [*autenticação*](../secgloss/a-gly.md)de servidor, o lado do servidor de operações Schannel deve ter acesso ao seu certificado [*X. 509*](../secgloss/x-gly.md) contendo sua chave pública e acesso à [*chave privada*](../secgloss/p-gly.md)correspondente. O lado do cliente do [*Schannel*](../secgloss/s-gly.md) precisa de seu certificado com sua chave pública e acesso à sua chave privada se a autenticação do cliente for implementada.

Como os mecanismos de protocolo Schannel nunca usam o \_ par de chaves pública/privada da assinatura, esse par de chaves não precisa ter suporte de um novo CSP com suporte somente para RSA/Schannel ou Diffie-Hellman/Schannel.

Se um mecanismo de protocolo usar um conjunto de codificação de exportação SSL 3,0 com um par de chaves AT- \_ Exchange com mais de 512 bits, o servidor deverá usar um par de chaves RSA adicional. Esse par de chaves adicional sempre é exatamente 512 bits e pode ser efêmero. O par é armazenado como um \_ elemento de keyexchange em um contêiner de chave de Propriedade do mecanismo de protocolo. Um identificador para esse contêiner de chave normalmente é adquirido na inicialização do mecanismo de protocolo.

Diffie-Hellman dá suporte apenas a [*\_ \_ EPHEM DH CALG*](../secgloss/c-gly.md) e usa chaves públicas RSA ou DSS normais.

 

 
