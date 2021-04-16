---
description: O modelo de segurança do Microsoft Windows permite que você controle o acesso a objetos de trabalho. Para obter mais informações sobre segurança, consulte modelo de Access-Control.
ms.assetid: 8d212292-f087-41e4-884e-cec4423dac49
title: Segurança do objeto de trabalho e direitos de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f5207e459bab2ae444282355844401e0b82e9c
ms.sourcegitcommit: 18023a15a4312c653a8dcc0feef23e3413a7f5dd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/25/2021
ms.locfileid: "105782298"
---
# <a name="job-object-security-and-access-rights"></a>Segurança do objeto de trabalho e direitos de acesso

O modelo de segurança do Microsoft Windows permite que você controle o acesso a objetos de trabalho. Para obter mais informações sobre segurança, consulte [modelo de controle de acesso](../secauthz/access-control-model.md).

Você pode especificar um [descritor de segurança](../secauthz/security-descriptors.md) para um objeto de trabalho ao chamar a função [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) . Se você especificar NULL, o objeto de trabalho obterá um descritor de segurança padrão. As ACLs no descritor de segurança padrão para um objeto de trabalho são provenientes do token principal ou de representação do criador.

Para obter ou definir o descritor de segurança para um objeto de trabalho, chame a função [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)ou [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) .

Os direitos de acesso válidos para objetos de trabalho incluem os [direitos de acesso padrão](../secauthz/standard-access-rights.md) e alguns direitos de acesso específicos ao trabalho. A tabela a seguir lista os direitos de acesso padrão usados por todos os objetos.

| Valor                           | Significado                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Excluir** (0x00010000L)        | Necessário para excluir o objeto.                                                                                                                                                                                                                                                           |
| **Ler \_ CONTROL** (0x00020000L) | Necessário para ler informações no descritor de segurança do objeto, não incluindo as informações na SACL. Para ler ou gravar a SACL, você deve solicitar o direito de acesso de **\_ \_ segurança do sistema de acesso** . Para obter mais informações, consulte [direitos de acesso à SACL](../secauthz/sacl-access-right.md). |
| **Sincronizar** (0x00100000L)   | O direito de usar o objeto para sincronização. Isso permite que um thread aguarde até que o objeto esteja no estado sinalizado.                                                                                                                                                                |
| **Gravar \_ DAC** (0x00040000L)    | Necessário para modificar a DACL no descritor de segurança do objeto.                                                                                                                                                                                                                   |
| **Gravar \_ PROPRIETÁRIO** (0x00080000L)  | Necessário para alterar o proprietário no descritor de segurança do objeto.                                                                                                                                                                                                                  |



 

A tabela a seguir lista os direitos de acesso específicos ao trabalho.



| Valor                                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Trabalho \_ do OBJETO \_ All \_ Access** (0x1F001F)             | Combina todos os direitos válidos de acesso ao objeto de trabalho.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Trabalho \_ do \_ \_ Processo de atribuição de objeto** (0x0001)           | Necessário para chamar a função [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) para atribuir processos ao objeto de trabalho.                                                                                                                                                                                                                                                                                                                                                                |
| **Trabalho \_ do \_Consulta de objeto** (0x0004)                     | Necessário para recuperar determinadas informações sobre um objeto de trabalho, como atributos e informações de contabilidade (consulte [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) e [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)).                                                                                                                                                                                                                                                                    |
| **Trabalho \_ do \_ \_ Atributos de conjunto de objetos** (0x0002)           | Necessário para chamar a função [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) para definir os atributos do objeto de trabalho.                                                                                                                                                                                                                                                                                                                                                                |
| **Trabalho \_ do \_Atributos de \_ segurança \_ do conjunto de objetos** (0x0010) | Não há suporte para esse sinalizador. Você deve definir as limitações de segurança individualmente para cada processo associado a um objeto de trabalho. **Windows Server 2003 e Windows XP:** Necessário para chamar a função [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) com a classe de informações **JobObjectSecurityLimitInformation** para definir as limitações de segurança para os processos associados ao objeto de trabalho. O suporte para esse sinalizador foi removido no Windows Vista e no Windows Server 2008. <br/> |
| **Trabalho \_ do \_Final do objeto** (0x0008)                 | Necessário para chamar a função [**TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject) para encerrar todos os processos no objeto de trabalho.                                                                                                                                                                                                                                                                                                                                                                     |



 

O identificador retornado por [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) tem o objeto de trabalho acesso de **\_ \_ \_ acesso** ao objeto de trabalho. Quando você chama a função [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta) , o sistema verifica os direitos de acesso solicitados no descritor de segurança do objeto. Se um objeto de trabalho estiver em uma hierarquia de [trabalhos aninhados](nested-jobs.md), um chamador com acesso ao objeto de trabalho implicitamente terá acesso a todos os seus trabalhos filho na hierarquia.

Você pode solicitar o direito de acesso de **\_ \_ segurança do sistema de acesso** a um objeto de trabalho se desejar ler ou gravar a SACL do objeto. Para obter mais informações, consulte [listas de controle de acesso (ACLs)](../secauthz/access-control-lists.md) e [direito de acesso SACL](../secauthz/sacl-access-right.md).

Você deve definir as limitações de segurança individualmente para cada processo associado a um objeto de trabalho, em vez de defini-los para o próprio objeto de trabalho. Para obter informações, consulte [segurança do processo e direitos de acesso](process-security-and-access-rights.md).

**Windows Server 2003 e Windows XP:** Você pode usar a função [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) para definir limitações de segurança para o objeto de trabalho. Esse recurso foi removido no Windows Vista e no Windows Server 2008.

 

 
