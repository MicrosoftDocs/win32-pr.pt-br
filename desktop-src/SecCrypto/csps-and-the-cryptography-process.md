---
description: As funções de CryptoAPI usam CSPs (provedores de serviços de criptografia) para executar criptografia e descriptografia e para fornecer segurança e armazenamento de chave.
ms.assetid: 7977e59b-7ce1-4bb4-aae4-d67b7d646493
title: CSPs e o processo de criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5404fc3641a9a2c753158f5acb84850f3f0f29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010428"
---
# <a name="csps-and-the-cryptography-process"></a>CSPs e o processo de criptografia

As funções de [*CryptoAPI*](../secgloss/c-gly.md) usam CSPs ( [*provedores de serviços de criptografia*](../secgloss/c-gly.md) ) para executar criptografia e descriptografia e para fornecer segurança e armazenamento de chave. Esses CSPs são módulos independentes. O ideal é que os CSPs sejam escritos para serem independentes de um aplicativo específico, para que qualquer aplicativo seja executado com uma variedade de CSPs. Na realidade, no entanto, alguns aplicativos têm requisitos específicos que exigem um CSP personalizado. Isso se compara ao modelo [*GDI*](../secgloss/g-gly.md) do Windows. Os CSPs são análogos aos drivers de dispositivo de gráficos.

A qualidade de proteção para chaves no sistema é um parâmetro de design do CSP e não do sistema como um todo. Isso permite que um aplicativo seja executado em uma variedade de contextos de segurança sem modificação.

Os aplicativos do Access que têm a criptografia interna são cuidadosamente restritos. Isso facilita o desenvolvimento de aplicativos seguros e portáteis.

As três regras de design a seguir se aplicam:

-   Os aplicativos não podem acessar diretamente o material de chave. Como todo material de chave é gerado dentro do CSP e usado pelo aplicativo por meio de identificadores opacos, não há risco de um aplicativo ou de suas DLLs associadas divulgar material de chave ou escolher material de chaveamento de fontes de má qualidade.
-   Os aplicativos não podem especificar os detalhes das operações de criptografia. A interface do CSP permite que um aplicativo escolha um algoritmo de criptografia ou assinatura, mas a implementação de cada operação de criptografia é feita pelo CSP.
-   Os aplicativos não tratam [*as credenciais*](../secgloss/c-gly.md) do usuário ou outros dados de autenticação do usuário. A autenticação do usuário é feita pelo CSP; Portanto, os CSPs futuros com recursos de autenticação avançada, como entradas biométricas, funcionarão sem a necessidade de alterar o modelo de autenticação do aplicativo.

No mínimo, um CSP consiste em uma DLL (biblioteca de vínculo dinâmico) e um [*arquivo de assinatura*](../secgloss/s-gly.md). O arquivo de assinatura é necessário para garantir que o [*CryptoAPI*](../secgloss/c-gly.md) reconheça o CSP. O CryptoAPI valida essa assinatura periodicamente para garantir que qualquer violação no CSP seja detectada.

Alguns CSPs podem implementar uma fração de sua funcionalidade em um serviço separado por endereço chamado por meio de RPC local ou em hardware chamado por meio de um driver de dispositivo de sistema. Isolar as operações globais de estado de chave e criptografia central em um serviço separado por endereço ou em hardware mantém as chaves e as operações seguras contra violação em um espaço de dados de aplicativo.

Não é recomendável que os aplicativos tirem proveito dos atributos específicos de um CSP específico. Por exemplo, o provedor criptográfico base da Microsoft (fornecido com o CryptoAPI) dá suporte a chaves de sessão de 40 bits e chaves públicas de 512 bits. Os aplicativos que manipulam essas chaves devem evitar suposições sobre a quantidade de memória necessária para armazenar essas chaves porque o aplicativo provavelmente falhará se um CSP diferente for usado. Aplicativos bem escritos devem funcionar com uma variedade de CSPs.

Para obter detalhes sobre os tipos de provedor criptográfico e os CSPs predefinidos que podem ser usados com o CryptoAPI, consulte [tipos de provedor criptográfico](cryptographic-provider-types.md) e [provedores de serviços de criptografia da Microsoft](microsoft-cryptographic-service-providers.md).

 

 
