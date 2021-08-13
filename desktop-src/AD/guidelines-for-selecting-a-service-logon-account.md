---
title: Diretrizes para selecionar uma conta de logon de serviço
description: Um serviço baseado no Win32 pode ser executado no contexto de segurança de uma conta de usuário local, uma conta de usuário de domínio ou a conta LocalSystem.
ms.assetid: aa2b93c7-335f-4e03-9198-fe2b396e296e
ms.tgt_platform: multiple
keywords:
- Diretrizes para selecionar um anúncio de conta de logon de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a976927130a3585be2e6130dbb71b37fa0c69660b6ae953e28909fad3db570f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188670"
---
# <a name="guidelines-for-selecting-a-service-logon-account"></a>Diretrizes para selecionar uma conta de logon de serviço

Um serviço baseado no Win32 pode ser executado no contexto de segurança de uma conta de usuário local, uma conta de usuário de domínio ou a conta LocalSystem. Para decidir qual conta usar, um administrador deve instalar o serviço com o conjunto mínimo de permissões necessárias para executar as operações de serviço. Em um serviço típico habilitado para diretório, isso significa que o instalador do serviço deve criar uma conta de usuário de domínio para o serviço e conceder a essa conta os direitos de acesso e privilégios específicos exigidos pelo serviço em tempo de execução. Um serviço deve ser executado somente na conta LocalSystem se o serviço exigir privilégios administrativos ou deve atuar como parte do sistema operacional no computador local.

Lembre-se de que o instalador do serviço deve, por padrão, configurar o serviço para ser executado em uma conta de usuário de domínio. Para executar o serviço na conta LocalSystem, o instalador do serviço deve consultar o administrador para obter permissão para fazer isso.

Para obter mais informações sobre descrições, vantagens e desvantagens de cada tipo de conta, consulte:

-   [Contas de usuário local](local-user-accounts.md).
-   [Contas de usuário de domínio](domain-user-accounts.md).
-   [A conta LocalSystem](the-localsystem-account.md).

 

 




