---
title: Armazenar informações específicas do usuário
description: Aplicativos devem armazenar informações específicas do usuário em locais específicos do usuário, separadamente de informações globais que se aplicam a todos os usuários.
ms.assetid: 32bd1d24-1d2e-4c0a-acdb-0cc67f275e6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aa8e60ec89c3f9d161941d01e1aa241f0bb0245d0f5b57b1cc362dd836bdb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000426"
---
# <a name="storing-user-specific-information"></a>Armazenar informações específicas do usuário

Em um Serviços de Área de Trabalho Remota, os aplicativos devem armazenar informações específicas do usuário em locais específicos do usuário, separadamente das informações globais que se aplica a todos os usuários. Essa regra se aplica a informações armazenadas no Registro, bem como informações armazenadas em arquivos. Em geral, não suponha que um computador seja equivalente a um usuário.

Armazene informações do Registro específicas do usuário na **chave do registro HKEY CURRENT \_ \_ USER.** Serviços de Área de Trabalho Remota carrega o hive do registro pessoal do usuário atual no **HKEY \_ CURRENT \_ USER** quando o usuário faz o login. É claro que Serviços de Área de Trabalho Remota gerencia o Registro para garantir que cada um dos clientes conectados detecte o hive de usuário correto em **HKEY \_ CURRENT \_ USER**. Para obter mais informações sobre chaves do Registro, consulte [Direitos de](/windows/desktop/SysInfo/registry-key-security-and-access-rights) Acesso e Segurança da Chave do Registro e [Hives do Registro.](/windows/desktop/SysInfo/registry-hives)

Por outro lado, todos os usuários compartilham o hive **HKEY \_ LOCAL \_ MACHINE.** Use **HKEY \_ LOCAL \_ MACHINE** para armazenar informações específicas do computador, não informações específicas do usuário.

Armazene arquivos de preferência do usuário ou outros arquivos específicos do usuário no diretório raiz do usuário ou em um diretório especificado pelo usuário. Essa consideração se aplica a arquivos temporários usados para armazenar informações provisórios (como dados armazenados em cache) ou para passar dados para outro aplicativo. Arquivos temporários específicos do usuário também devem ser armazenados por usuário.

Você pode usar a [**função SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) com o sinalizador CSIDL PERSONAL para obter o local do diretório de arquivos \_ pessoais do usuário. Você também pode usar a [**função GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) para recuperar o caminho do Windows diretório. Em um ambiente Serviços de Área de Trabalho Remota, o Windows diretório tem a garantia de ser privado para cada usuário. Não armazene arquivos específicos do usuário no diretório do sistema, como WINDOWS ou diretório do programa, como Arquivos de Programas.

Para evitar conflitos entre as informações e as preferências dos usuários, os aplicativos devem armazenar informações temporárias por usuário em arquivos temporários específicos do usuário. Arquivos temporários específicos do usuário também impedem falhas de aplicativo causadas por conflitos de bloqueio de arquivo. Para especificar o caminho para armazenar informações temporárias, use a [**função GetTempPath.**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha)

 

 