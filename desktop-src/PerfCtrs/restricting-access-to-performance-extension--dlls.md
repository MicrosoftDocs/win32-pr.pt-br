---
description: A partir do Windows Server 2003, o grupo de usuários do monitor de desempenho e o grupo de usuários de log de desempenho foram disponibilizados para desenvolvedores e usuários de DLLs de desempenho e para as funções de API de PDH (auxiliar de dados de desempenho).
ms.assetid: 423359be-9d41-4a5f-91cd-f6d7a6a91d9d
title: Restringindo o acesso a DLLs de extensão de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd433cad68ec3e50f6b17994da98164e2ae9f237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828376"
---
# <a name="restricting-access-to-performance-extension-dlls"></a>Restringindo o acesso a DLLs de extensão de desempenho

A partir do Windows Server 2003, o grupo de usuários do monitor de desempenho e o grupo de usuários de log de desempenho foram disponibilizados para desenvolvedores e usuários de DLLs de desempenho e para as funções de API de PDH (auxiliar de dados de desempenho). Esses grupos de segurança de desempenho destinam-se ao uso por administradores de sistema ao restringir o acesso às informações expostas por DLLs de desempenho para uma lista específica de usuários.

O grupo de usuários do monitor de desempenho destina-se a incluir usuários que exibem dados do contador e não registram dados do contador usando o serviço de Logs e Alertas de Desempenho. O grupo de usuários de log de desempenho deve incluir os usuários que têm permissão para usar os logs de desempenho e o serviço de alerta para registrar em log os contadores no servidor local ou remoto. Os privilégios desse grupo também incluem a criação de arquivos de log em sistemas locais ou remotos, usando o serviço de alertas e executando programas como parte do serviço.

Observe que esses grupos de segurança de desempenho não são por si próprios um mecanismo de restrição de acesso. Você deve usar esses grupos com o modelo de controle de acesso a objetos do Windows para fazer isso.

A maioria dos aplicativos se comunica com a DLL de desempenho por meio de um mecanismo IPC, normalmente a memória compartilhada. Portanto, você pode adicionar os membros de um grupo de segurança de desempenho ao descritor de segurança do objeto de memória compartilhada para restringir o acesso à DLL para os membros do grupo de segurança. Ao fazer isso, você também deve adicionar os membros do grupo ao descritor de segurança dos objetos do sistema que a DLL de desempenho acessa para fornecer dados do contador, por exemplo, arquivos de log e pastas. Para obter informações mais detalhadas sobre como adicionar ACLs aos descritores de segurança do objeto, consulte [modificando a ACL de um objeto](/windows/desktop/SecAuthZ/modifying-the-acls-of-an-object-in-c--).

Outro método que você pode usar para modificar as informações de ACL do descritor de segurança de um objeto de sistema IPC é especificar os membros da lista de grupos de segurança de desempenho com SDDL (Security Descriptor Definition Language) e chamar [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) para criar o descritor de segurança. Esse descritor de segurança é então anexado ao objeto do sistema IPC. O seguinte mostra uma cadeia de caracteres SDDL que inclui o grupo de usuários do monitor de desempenho, MU e o grupo de usuários de log de desempenho, LU.

``` syntax
D:(A;OICI;GA;;;SY)(A;OICI;GA;;;BA)(A;OICI;FRFWFXSDRC;;;NS)(A;OICI;FRFWFXSDRC;;;LU)(A;OICI;FRFX;;;MU) 
```

 

 
