---
description: Programas de exemplo nas seções a seguir executam operações que exigem que pares de chaves públicas/privadas sejam disponibilizados para criptografar e descriptografar arquivos, mensagens e assinaturas.
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: Contêineres de chave, chaves e certificados necessários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee5f86f887050d0d7abe440c89cc9c9444dba26854645d5ad6d16279af91e1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992716"
---
# <a name="necessary-key-containers-keys-and-certificates"></a>Contêineres de chave, chaves e certificados necessários

Programas de exemplo nas seções a seguir executam operações que exigem que pares de chaves [*públicas/privadas*](../secgloss/p-gly.md) sejam disponibilizados para criptografar e descriptografar arquivos, mensagens e assinaturas. Muitos desses programas compilarão, vinculam e executarão, mas falharão em tempo de operação sem a existência de contêineres de chave [*adequados,*](../secgloss/k-gly.md)chaves, armazenamentos de [*certificados*](../secgloss/c-gly.md)e certificados nesses armazenamentos.

Além disso, alguns dos certificados no meu armazenamento devem ter algumas de suas propriedades estendidas definidas.

A criação do contêiner de chave padrão necessário pode ser feita executando o programa no Programa C de Exemplo: criando um contêiner de chaves e [gerando chaves](example-c-program-creating-a-key-container-and-generating-keys.md). Observe que a criação de um contêiner de chaves não gera automaticamente pares de chaves públicas/privadas. No entanto, o programa de exemplo cria o contêiner de chave e gera os pares de chaves pública/privada.

Depois que os pares de chaves públicas/privadas são gerados, os certificados de teste que usam essas chaves podem ser obtidos de uma AC (autoridade [*de*](../secgloss/c-gly.md) certificação).

Vários dos programas pressupom que os certificados com nomes de assunto específicos existam no armazenamento do sistema MY. Em particular, vários programas procurarão certificados com os nomes de assunto "Certificado de Teste Completo" e "Hortense". Os nomes de assunto para os certificados podem ser alterados no código para corresponder aos nomes de assunto dos certificados que existem no meu armazenamento de certificados.

Executar o programa de exemplo no Programa C de Exemplo: listar os [certificados](example-c-program-listing-the-certificates-in-a-store.md) em um armazenamento exibirá todos os certificados em um armazenamento e todas as propriedades estendidas definidas nesses certificados.

 

 
