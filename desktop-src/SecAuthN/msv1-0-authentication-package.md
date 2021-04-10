---
description: A Microsoft fornece o \_ pacote de autenticação MSV1 0 para logons do computador local que não exigem autenticação personalizada.
ms.assetid: 8b85588d-0a79-43af-b526-7a5fc8248f99
title: MSV1_0 pacote de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 662ae65f60bec61c30b12271a34dc9d3c2883d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170811"
---
# <a name="msv1_0-authentication-package"></a>Pacote de autenticação do MSV1 \_ 0

A Microsoft fornece o \_ [*pacote de autenticação*](../secgloss/a-gly.md) MSV1 0 para logons do computador local que não exigem autenticação personalizada. A [*autoridade de segurança local*](../secgloss/l-gly.md) (LSA) chama o \_ pacote de autenticação MSV1 0 para processar os dados de logon coletados pela [*Gina*](../secgloss/g-gly.md) para o processo de logon do [*Winlogon*](../secgloss/w-gly.md) . O \_ pacote MSV1 0 verifica o banco de dados do Sam (Gerenciador de contas de segurança) local para determinar se o logon pertence a uma [*entidade de segurança*](../secgloss/s-gly.md) válida e, em seguida, retorna o resultado da tentativa de logon para o LSA.

O MSV1 \_ 0 também dá suporte a logons de domínio. MSV1 \_ 0 processa logons de domínio usando a autenticação de passagem, conforme ilustrado no diagrama a seguir.

![pacote de autenticação do msv1 \- 0](images/lsaint4.png)

Na autenticação de passagem, a instância local do MSV1 \_ 0 usa o serviço Netlogon para chamar a instância do MSV1 \_ 0 em execução no controlador de domínio. A instância do controlador de domínio de MSV1 \_ 0 verifica o banco de dados Sam do controlador de domínio e retorna o resultado do logon à instância do MSV1 \_ 0 no computador local. A versão local do MSV1 \_ 0 encaminha o resultado do logon para a instância do LSA no computador local.

Se o controlador de domínio não estiver disponível e a LSA contiver [*credenciais*](../secgloss/c-gly.md) armazenadas em cache para o usuário, a instância local do MSV1 \_ 0 poderá autenticar o usuário usando os dados de logon armazenados em cache.

O \_ pacote de autenticação MSV1 0 também dá suporte a [pacotes de subautenticação](subauthentication-packages.md). Um pacote de subautenticação é uma DLL que pode substituir parte dos critérios de autenticação e validação usados pelo \_ pacote de autenticação MSV1 0.

O \_ pacote de autenticação MSV1 0 define um par de chaves/valor de cadeia de caracteres de [*credenciais primários*](../secgloss/p-gly.md) . A cadeia de credenciais primária contém as credenciais derivadas dos dados fornecidos no momento do logon. Ele inclui o nome de usuário e as formas de diferenciação de maiúsculas e minúsculas da senha do usuário.

 

 
