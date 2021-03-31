---
description: Os programas de exemplo nas seções a seguir executam operações que exigem a disponibilidade de pares de chaves pública/privada para criptografar e descriptografar arquivos, mensagens e assinaturas.
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: Contêineres de chave, chaves e certificados necessários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d1f01a59c83ea21437608608e033a2ee0f8fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663143"
---
# <a name="necessary-key-containers-keys-and-certificates"></a>Contêineres de chave, chaves e certificados necessários

Os programas de exemplo nas seções a seguir executam operações que exigem a disponibilidade de [*pares de chaves pública/privada*](../secgloss/p-gly.md) para criptografar e descriptografar arquivos, mensagens e assinaturas. Muitos desses programas serão compilados, vinculados e executados, mas falharão em tempo de execução sem a existência de [*contêineres de chave*](../secgloss/k-gly.md), chaves, [*repositórios de certificados*](../secgloss/c-gly.md)e certificados apropriados nesses armazenamentos.

Além disso, alguns dos certificados no meu repositório devem ter algumas das suas propriedades estendidas definidas.

A criação do contêiner de chave padrão necessário pode ser feita executando o programa no [programa C de exemplo: Criando um contêiner de chave e gerando chaves](example-c-program-creating-a-key-container-and-generating-keys.md). Observe que a criação de um contêiner de chave não gera automaticamente pares de chaves pública/privada. O programa de exemplo, no entanto, cria o contêiner de chave e gera os pares de chaves pública/privada.

Após os pares de chaves pública/privada terem sido gerados, os certificados de teste usando essas chaves podem ser obtidos de uma [*autoridade de certificação*](../secgloss/c-gly.md) (CA).

Vários dos programas pressupõem que os certificados com nomes de entidades específicos existam no repositório do meu sistema. Em particular, vários programas procuram certificados com os nomes de assunto "certificado de teste completo" e "Hortense". Os nomes de entidade para os certificados podem ser alterados no código para corresponder aos nomes de entidades de certificados existentes no repositório meu certificado.

Executando o programa de exemplo no [programa C de exemplo: listar os certificados em um repositório](example-c-program-listing-the-certificates-in-a-store.md) exibirá todos os certificados em um repositório e todas as propriedades estendidas definidas nesses certificados.

 

 
