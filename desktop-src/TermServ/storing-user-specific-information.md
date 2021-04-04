---
title: Armazenando informações específicas do usuário
description: Aplicativos devem armazenar informações específicas do usuário em locais específicos do usuário, separadamente de informações globais que se aplicam a todos os usuários.
ms.assetid: 32bd1d24-1d2e-4c0a-acdb-0cc67f275e6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c6236b7ba11a8b3149533e920b9b9413085d93
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007712"
---
# <a name="storing-user-specific-information"></a>Armazenando informações específicas do usuário

Em um ambiente Serviços de Área de Trabalho Remota, os aplicativos devem armazenar informações específicas do usuário em locais específicos do usuário, separadamente das informações globais que se aplicam a todos os usuários. Essa regra se aplica às informações armazenadas no registro, bem como às informações armazenadas em arquivos. Em geral, não presuma que um computador é equivalente a um usuário.

Armazene informações de registro específicas do usuário na chave de registro **HKEY \_ Current \_ User** . Serviços de Área de Trabalho Remota carrega o hive do registro pessoal do usuário atual em **HKEY \_ Current \_ User** quando o usuário faz logon. É claro que Serviços de Área de Trabalho Remota gerencia o registro para garantir que cada um dos clientes conectados detecte o hive do usuário correto em **HKEY \_ Current \_ User**. Para obter mais informações sobre chaves do registro, consulte [segurança da chave do registro e](/windows/desktop/SysInfo/registry-key-security-and-access-rights) [registros e hives do registro](/windows/desktop/SysInfo/registry-hives).

Por outro lado, todos os usuários compartilham o hive do **\_ \_ computador local hKey** . Use **o \_ \_ computador local hKey** para armazenar informações específicas do computador, não informações específicas do usuário.

Armazene arquivos de preferência de usuário ou outros arquivos específicos do usuário no diretório raiz do usuário ou em um diretório especificado pelo usuário. Essa consideração se aplica a arquivos temporários usados para armazenar informações provisórias (como dados armazenados em cache) ou para passar dados para outro aplicativo. Os arquivos temporários específicos do usuário também devem ser armazenados em uma base por usuário.

Você pode usar a função [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) com o sinalizador de CSIDL \_ pessoal para obter o local do diretório de arquivos pessoais do usuário. Você também pode usar a função [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para recuperar o caminho do diretório do Windows. Em um ambiente Serviços de Área de Trabalho Remota, é garantido que o diretório do Windows seja privado para cada usuário. Não armazene arquivos específicos do usuário no diretório do sistema, como o WINDOWS ou o diretório do programa, como arquivos de programas.

Para evitar conflitos entre as informações e as preferências dos usuários, os aplicativos devem armazenar informações temporárias por usuário em arquivos temporários específicos do usuário. Os arquivos temporários específicos do usuário também impedem falhas de aplicativo causadas por conflitos de bloqueio de arquivo. Para especificar o caminho para armazenar informações temporárias, use a função [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) .

 

 