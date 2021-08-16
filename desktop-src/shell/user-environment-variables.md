---
description: Variáveis de ambiente especificam caminhos de pesquisa para arquivos, diretórios para arquivos temporários, opções específicas de aplicativo e outras informações semelhantes.
ms.assetid: 6180e54e-4bd9-4692-83fd-f3f7f1d8f8d7
title: Variáveis de ambiente do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bbe37cdbe7dd82268b2166ed625a9baf1d2502df4c26208bca51a89cd782df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857038"
---
# <a name="user-environment-variables"></a>Variáveis de ambiente do usuário

Variáveis de ambiente especificam caminhos de pesquisa para arquivos, diretórios para arquivos temporários, opções específicas de aplicativo e outras informações semelhantes. O sistema mantém um bloco de ambiente para cada usuário e um para o computador. O bloco de ambiente do sistema representa variáveis de ambiente para todos os usuários do computador específico. O bloco de ambiente de um usuário representa as variáveis de ambiente que o sistema mantém para esse usuário específico, incluindo o conjunto de variáveis de ambiente do sistema.

Por padrão, cada processo recebe uma cópia do bloco de ambiente para seu processo pai. Normalmente, esse é o bloco de ambiente para o usuário que fez logon. Um processo pode especificar diferentes blocos de ambiente para seus processos filho usando a função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) ou [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .

Para adicionar ou modificar variáveis de ambiente, o usuário seleciona **sistema** no **painel de controle** e seleciona a guia **ambiente** . O usuário também pode adicionar ou modificar variáveis de ambiente em um prompt de comando usando o comando **set** . As variáveis de ambiente criadas com o comando **set** aplicam-se somente à janela de comando na qual elas são definidas e a seus processos filho. Para obter mais informações, digite **set/?** em um prompt de comando.

Para recuperar uma cópia do bloco de ambiente para um determinado usuário, use a função [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) . Para liberar um bloco de ambiente criado pelo **CreateEnvironmentBlock**, use a função [**DestroyEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock) . Essas funções fazem referência a um ponteiro para um bloco de ambiente. O bloco de ambiente é uma matriz de cadeias de caracteres Unicode terminadas em nulo. A lista termina com dois valores nulos ( \\ 0 \\ 0).

Para expandir uma cadeia de caracteres que contém variáveis de ambiente usando o bloco de ambiente para um usuário especificado, use a função [**ExpandEnvironmentStringsForUser**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) .

 

 
