---
description: A Microsoft fornece o pacote de autenticação MSV1 \_ 0 para logons de computador local que não exigem autenticação personalizada.
ms.assetid: 8b85588d-0a79-43af-b526-7a5fc8248f99
title: MSV1_0 de autenticação do MSV1_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12366ecf2ce213b1221fe310e77f9f019c859c038a47d332c8b702639662bc53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921742"
---
# <a name="msv1_0-authentication-package"></a>Pacote de Autenticação MSV1 \_ 0

A Microsoft fornece o pacote de autenticação MSV1 \_ 0 para logons de computador local que não exigem autenticação personalizada. [](../secgloss/a-gly.md) A LSA (Autoridade de Segurança [*Local)*](../secgloss/l-gly.md) chama o pacote de autenticação MSV1 0 para processar os dados de logon coletados peloLP para o processo de \_ logon do [*Winlogon.*](../secgloss/w-gly.md) [](../secgloss/g-gly.md) O pacote MSV1 0 verifica o banco de dados SAM (gerenciador de contas de segurança) local para determinar se os dados de logon pertencem a uma entidade de segurança válida e retorna o resultado da tentativa de logon para \_ o LSA. [](../secgloss/s-gly.md)

O MSV1 \_ 0 também dá suporte a logons de domínio. O MSV1 0 processa logons de domínio usando a autenticação de \_ passagem, conforme ilustrado no diagrama a seguir.

![Pacote de autenticação msv1 \- 0](images/lsaint4.png)

Na autenticação de passagem, a instância local do MSV1 0 usa o serviço Netlogon para chamar a instância \_ do MSV1 0 em execução no controlador \_ de domínio. A instância do controlador de domínio MSV1 0 verifica o banco de dados SAM do controlador de domínio e retorna o resultado do logon para a instância \_ do MSV1 0 no \_ computador local. A versão local do MSV1 0 encaminha o resultado do logon para a instância do \_ LSA no computador local.

Se o controlador de domínio não estiver disponível e o LSA contiver credenciais armazenadas em cache para o usuário, a instância local do MSV1 0 poderá autenticar o usuário usando os dados de logon [*armazenados*](../secgloss/c-gly.md) em \_ cache.

O pacote de autenticação MSV1 \_ 0 também dá suporte a [pacotes de subutenticação](subauthentication-packages.md). Um pacote de subutenticação é uma DLL que pode substituir parte dos critérios de autenticação e validação usados pelo pacote de autenticação MSV1 \_ 0.

O pacote de autenticação MSV1 0 define um par de valor de cadeia de \_ [*caracteres/chave*](../secgloss/p-gly.md) de credenciais primárias. A cadeia de caracteres de credenciais primárias contém as credenciais derivadas dos dados fornecidos no momento do logon. Ele inclui o nome de usuário e as formas que não fazem maiúsculas de minúsculas e maiúsculas de minúsculas da senha do usuário.

 

 
