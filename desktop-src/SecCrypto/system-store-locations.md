---
description: Um armazenamento do sistema é uma coleção que consiste em um ou mais armazenamentos irmãos físicos.
ms.assetid: 41fe9366-4c17-43bb-91d6-934c7aa87a2d
title: Locais de armazenamento do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d793d94bcb1c58bcc0d8c046b038df7e699d287b9ede3f14d6e2cb3c94ab781e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897428"
---
# <a name="system-store-locations"></a>Locais de armazenamento do sistema

Um armazenamento do sistema é uma coleção que consiste em um ou mais armazenamentos irmãos físicos. Para cada armazenamento do sistema, há armazenamentos irmãos físicos predefinidos. Depois de abrir um repositório do sistema, como MY em CERT SYSTEM STORE CURRENT USER, o provedor de repositório chama \_ \_ \_ \_ [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) para abrir cada um dos repositórios físicos na coleção de repositórios do sistema. No processo aberto, cada um desses repositórios físicos é adicionado à coleção de repositórios do sistema usando [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection). Todos os certificados nesses armazenamentos físicos estão disponíveis por meio da coleção de armazenamento do sistema lógico.

Para cada local de armazenamento do sistema, os armazenamentos de sistemas predefinidos são:

-   MY
-   Root
-   Confiança
-   CA

No USUÁRIO \_ ATUAL DO CERT SYSTEM \_ \_ \_ STORE, também há um armazenamento UserDS predefinido. Um armazenamento de cartão inteligente está planejado para esse local.

Aqui estão os armazenamentos do sistema seguidos por mais comentários:

-   [USUÁRIO \_ ATUAL DO CERT SYSTEM \_ \_ \_ STORE](#cert_system_store_current_user)
-   [COMPUTADOR LOCAL \_ DO ARMAZENAMENTO DO SISTEMA DE \_ \_ \_ CERTIFICADOS](#cert_system_store_local_machine)
-   [SERVIÇO ATUAL \_ DO ARMAZENAMENTO DO SISTEMA DE \_ \_ \_ CERTIFICADOS](#cert_system_store_current_service)
-   [SERVIÇOS DE \_ ARMAZENAMENTO DO SISTEMA DE \_ \_ CERTIFICADOS](#cert_system_store_services)
-   [USUÁRIOS \_ DO CERT SYSTEM \_ STORE \_](#cert_system_store_users)
-   [POLÍTICA DE \_ GRUPO DE USUÁRIOS ATUAL DO SISTEMA DE \_ \_ \_ \_ CERTIFICADOS](#cert_system_current_user_group_policy)
-   [POLÍTICA DE \_ GRUPO DE MÁQUINAS LOCAIS DO SISTEMA DE \_ \_ \_ \_ CERTIFICADOS](#cert_system_local_machine_group_policy)
-   [CERT \_ SYSTEM \_ STORE \_ LOCAL \_ MACHINE \_ ENTERPRISE](#cert_system_store_local_machine_enterprise)
-   [Comentários](#remarks)

### <a name="cert_system_store_current_user"></a>USUÁRIO \_ ATUAL DO CERT SYSTEM \_ \_ \_ STORE

Os armazenamentos do sistema DE USUÁRIO ATUAL DO CERT \_ SYSTEM STORE estão no seguinte local do \_ \_ \_ Registro:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         SystemCertificates
```

Os armazenamentos físicos predefinidos associados a esses armazenamentos do sistema são os itens a seguir.



| Armazenamento do sistema | Armazenamento físico                                           |
|--------------|----------------------------------------------------------|
| MY           | . Padrão                                                 |
| Root         | . Default.LocalMachine<br/> . Smartcard<br/>   |
| Confiança        | . Default.GroupPolicy<br/> . Localmachine<br/> |
| CA           | . Default.GroupPolicy<br/> . Localmachine<br/> |
| UserDS       | . UserCertificate                                         |



 

### <a name="cert_system_store_local_machine"></a>COMPUTADOR LOCAL \_ DO ARMAZENAMENTO DO SISTEMA DE \_ \_ \_ CERTIFICADOS

Os armazenamentos do sistema DE MÁQUINA LOCAL DO CERT \_ SYSTEM STORE estão no seguinte local do \_ \_ \_ Registro:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         SystemCertificates
```

Os armazenamentos físicos predefinidos são associados a esses armazenamentos do sistema da seguinte forma.



| Armazenamento do sistema | Armazenamento físico                                                                                    |
|--------------|---------------------------------------------------------------------------------------------------|
| MY           | . Padrão                                                                                          |
| Root         | . Default.AuthRoot<br/> . Grouppolicy<br/> . Enterprise<br/> . Smartcard<br/> |
| Confiança        | . Default.GroupPolicy<br/> . Enterprise<br/>                                            |
| CA           | . Default.GroupPolicy<br/> . Enterprise <br/>                                           |



 

### <a name="cert_system_store_current_service"></a>SERVIÇO ATUAL \_ DO ARMAZENAMENTO DO SISTEMA DE \_ \_ \_ CERTIFICADOS

Os armazenamentos do sistema DE SERVIÇO ATUAL DO CERT \_ SYSTEM STORE estão no seguinte local do \_ \_ \_ Registro:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

Os armazenamentos físicos predefinidos associados a esses armazenamentos do sistema são os itens a seguir.



| Armazenamento do sistema | Armazenamento físico                   |
|--------------|----------------------------------|
| MY           | . Padrão                         |
| Root         | . Default.LocalMachine<br/> |
| Confiança        | . Default.LocalMachine<br/> |
| CA           | . Default.LocalMachine<br/> |



 

### <a name="cert_system_store_services"></a>SERVIÇOS DE \_ ARMAZENAMENTO DO SISTEMA DE \_ \_ CERTIFICADOS

Os armazenamentos do sistema CERT \_ SYSTEM STORE SERVICES estão no seguinte local do \_ \_ Registro:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

Os armazenamentos físicos predefinidos associados a esses armazenamentos do sistema são os itens a seguir.



| Armazenamento do sistema       | Armazenamento físico                   |
|--------------------|----------------------------------|
| ServiceName \\ MY    | . Padrão                         |
| Raiz \\ servicename  | . Default.LocalMachine<br/> |
| Confiança \\ de ServiceName | . Default.LocalMachine<br/> |
| ServiceName \\ CA    | . Default.LocalMachine<br/> |



 

### <a name="cert_system_store_users"></a>USUÁRIOS \_ DO CERT SYSTEM \_ STORE \_

Os armazenamentos do sistema DE USUÁRIOS DO CERT \_ SYSTEM STORE estão no seguinte local do \_ \_ Registro:

```
HKEY_USERS
   UserName
      Software
         Microsoft
            SystemCertificates
```

Os armazenamentos físicos predefinidos associados a esses armazenamentos do sistema são os itens a seguir.



| Armazenamento do sistema  | Armazenamento físico                   |
|---------------|----------------------------------|
| userid \\ MY    | . Default.LocalMachine<br/> |
| raiz \\ userid  | . Default.LocalMachine<br/> |
| confiança \\ userid | . Default.LocalMachine<br/> |
| AC \\ userid    | . Default.LocalMachine<br/> |



 

### <a name="cert_system_current_user_group_policy"></a>POLÍTICA DE \_ GRUPO DE USUÁRIOS ATUAL DO SISTEMA DE \_ \_ \_ \_ CERTIFICADOS

Os armazenamentos do sistema DE POLÍTICA DE GRUPO DE USUÁRIO ATUAL DO SISTEMA DE CERTIFICADO estão no seguinte local \_ \_ do \_ \_ \_ Registro:

```
HKEY_CURRENT_USER
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_local_machine_group_policy"></a>POLÍTICA DE \_ GRUPO DE MÁQUINAS LOCAIS DO SISTEMA DE \_ \_ \_ \_ CERTIFICADOS

Os armazenamentos do sistema DE POLÍTICA DE GRUPO DE MÁQUINAS LOCAIS DO SISTEMA \_ DE CERTIFICADO estão no seguinte local do \_ \_ \_ \_ Registro:

```
HKEY_LOCAL_MACHINE
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_store_local_machine_enterprise"></a>CERT \_ SYSTEM \_ STORE \_ LOCAL \_ MACHINE \_ ENTERPRISE

CERT SYSTEM STORE LOCAL MACHINE ENTERPRISE contém certificados compartilhados entre domínios na \_ empresa \_ e \_ \_ \_ baixados do diretório empresarial global. Para sincronizar o armazenamento empresarial do cliente, o diretório empresarial é sondado a cada oito horas e os certificados são baixados automaticamente em segundo plano.

Os armazenamentos físicos predefinidos associados a esses armazenamentos do sistema são os itens a seguir.



| Armazenamento do sistema | Armazenamento físico |
|--------------|----------------|
| MY           | . Padrão       |
| Root         | . Padrão       |
| Confiança        | . Padrão       |
| CA           | . Padrão       |



 

### <a name="remarks"></a>Comentários

Repositórios físicos adicionais podem ser associados a um repositório do sistema usando [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).

Os armazenamentos DE USUÁRIOS DO CERT SYSTEM STORE SERVICE e CERT SYSTEM STORE são abertos prefixando o nome do armazenamento na cadeia de caracteres passada para \_ \_ \_ \_ \_ \_ *pvPara*  \\  com **o serviço ou o nome de usuário, como ServiceName Trust ou . Padrão** \\ **MY.** O local DE USUÁRIOS DO CERT SYSTEM STORE SERVICES ou CERT SYSTEM STORE pode abrir o mesmo armazenamento no SERVIÇO ATUAL DO SISTEMA DE CERTIFICADO ou NO USUÁRIO ATUAL DO CERT SYSTEM STORE usando o SID (identificador de segurança \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ textual) [](../secgloss/s-gly.md) do serviço ou usuário atual.

Os armazenamentos na POLÍTICA DE GRUPO DE USUÁRIOS DO CERT SYSTEM STORE e NA POLÍTICA DE GRUPO DO COMPUTADOR LOCAL DO SISTEMA DE CERTIFICADOs em uma configuração de rede são baixados no computador cliente \_ \_ do \_ \_ \_ \_ \_ \_ \_ \_ GPT (modelo de Política de Grupo) durante a inicialização do computador ou logon do usuário. Esses armazenamentos podem ser atualizados no computador cliente após a inicialização ou logon quando o GPT é alterado no servidor de domínio por um administrador. A [**função CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) permite que um aplicativo seja notificado quando os repositórios em qualquer um desses locais foram alterados.

Os seguintes locais de armazenamento do sistema podem ser abertos remotamente:

-   COMPUTADOR LOCAL \_ DO ARMAZENAMENTO DO SISTEMA DE \_ \_ \_ CERTIFICADOS
-   POLÍTICA \_ DE GRUPO DE MÁQUINAS LOCAIS DO ARMAZENAMENTO DO SISTEMA DE \_ \_ \_ \_ \_ CERTIFICADOS
-   SERVIÇOS DE \_ ARMAZENAMENTO DO SISTEMA DE \_ \_ CERTIFICADOS
-   USUÁRIOS \_ DO CERT SYSTEM \_ STORE \_

Os locais do armazenamento do sistema são abertos remotamente prefixando o nome do armazenamento na cadeia de caracteres passada para *pvPara* com o nome do computador. Exemplos de nomes de armazenamento do sistema remoto são:

-   *ComputerName* \\ **AC**
-   \\\\*ComputerName* \\ **AC**
-   *ComputerName* \\ *ServiceName* \\ **Confiança**
-   \\\\*ComputerName* \\ *ServiceName* \\ **Confiança**

 

 
