---
description: O modelo de segurança do Windows permite controlar o acesso aos objetos de mapeamento de arquivos. Para obter mais informações, consulte modelo de Access-Control.
ms.assetid: 8bbf7c98-ff83-4ed9-8b82-f08dcd31295c
title: Segurança de mapeamento de arquivo e direitos de acesso
ms.topic: article
ms.date: 10/06/2018
ms.openlocfilehash: 65d520e12d1b555e7c633f0d1e0ba5142c330ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779478"
---
# <a name="file-mapping-security-and-access-rights"></a>Segurança de mapeamento de arquivo e direitos de acesso

O modelo de segurança do Windows permite controlar o acesso aos objetos de mapeamento de arquivos. Para obter mais informações, consulte [modelo de controle de acesso](../secauthz/access-control-model.md).

Você pode especificar um [descritor de segurança](../secauthz/security-descriptors.md) para um objeto de mapeamento de arquivo ao chamar a função [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) . Se você especificar **NULL**, o objeto obterá um descritor de segurança padrão. As ACLs no descritor de segurança padrão para um objeto de mapeamento de arquivo são provenientes do token principal ou de representação do criador.

Para recuperar o descritor de segurança de um objeto de mapeamento de arquivo, chame a função [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa) ou [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo) . Para definir o descritor de segurança de um objeto de mapeamento de arquivo, chame a função [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa) ou [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) .

Os direitos de acesso válidos para objetos de mapeamento de arquivos incluem os [direitos de acesso padrão](../secauthz/standard-access-rights.md)de **excluir**, **\_ controle de leitura**, **gravação de \_ DAC** e **gravar \_ proprietário** . Os objetos de mapeamento de arquivo não dão suporte ao direito de **sincronização** de acesso padrão. A tabela a seguir lista os direitos de acesso específicos aos objetos de mapeamento de arquivos.

| Direito de acesso | Significado |
|-|-|
| **\_todo o \_ \_ acesso ao mapa de arquivos** | Inclui todos os direitos de acesso a um objeto de mapeamento de arquivo, exceto a **\_ \_ execução do mapa de arquivo**. As funções [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) e [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) tratam dessa mesma maneira de especificar a **\_ \_ gravação do mapa de arquivos**. |
| **\_execução do mapa de arquivos \_** | Permite o mapeamento de exibições executáveis do objeto de mapeamento de arquivo. O objeto deve ter sido criado com a proteção de página que permite o acesso de execução, como **\_ executar \_ leitura de página**, **\_ executar \_ WRITECOPY** ou página **executar proteção \_ \_ ReadWrite** .  |
| **\_leitura do mapa de arquivos \_** | Permite o mapeamento de exibições somente leitura ou de cópia em gravação do objeto de mapeamento de arquivo.  |
| **\_gravação de mapa de arquivo \_** | Permite o mapeamento de exibições somente leitura, cópia em gravação ou leitura/gravação de um objeto de mapeamento de arquivo. O objeto deve ter sido criado com proteção de página que permita acesso de gravação, como a **página \_ ReadWrite** ou a proteção de página **\_ executar \_ ReadWrite** . |

O mapeamento de uma exibição de copiar na gravação de um objeto de mapeamento de arquivo requer o mesmo acesso que o mapeamento de uma exibição somente leitura. O sinalizador de **\_ \_ cópia do mapa de arquivos** não é um direito de acesso e não deve ser especificado como parte de uma DACL em um descritor de segurança. Esse valor pode ser usado somente com funções que mapeiam uma exibição de um objeto de mapeamento de arquivo, como as funções [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) e [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) , ou com a função [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) , que trata a **cópia do \_ mapa \_ de arquivos** da mesma forma que trata a **leitura do \_ mapa \_ de arquivos**.

Você pode solicitar o direito de acesso de **\_ \_ segurança do sistema de acesso** a um objeto de mapeamento de arquivo se quiser ler ou gravar a SACL do objeto. Para obter mais informações, consulte [listas de controle de acesso (ACLs)](../secauthz/access-control-lists.md) e [direito de acesso SACL](../secauthz/sacl-access-right.md).
