---
description: Um repositório do sistema é uma coleção que consiste em um ou mais armazenamentos irmãos físicos.
ms.assetid: 41fe9366-4c17-43bb-91d6-934c7aa87a2d
title: Locais de armazenamento do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0863ffde8be5db67459908b1ec26ec73da029744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921848"
---
# <a name="system-store-locations"></a>Locais de armazenamento do sistema

Um repositório do sistema é uma coleção que consiste em um ou mais armazenamentos irmãos físicos. Para cada repositório do sistema, há repositórios irmãos físicos predefinidos. Depois de abrir um repositório do sistema, como meu no \_ sistema CERT \_ \_ \_ do usuário atual, o provedor da loja chama [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) para abrir cada um dos repositórios físicos na coleção de armazenamento do sistema. No processo aberto, cada um desses repositórios físicos é adicionado à coleção de armazenamento do sistema usando [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection). Todos os certificados nesses repositórios físicos estão disponíveis por meio da coleção de armazenamento do sistema lógico.

Para cada local de repositório do sistema, os armazenamentos de sistemas predefinidos são:

-   MY
-   Root
-   Confiar
-   AC

No \_ usuário atual do repositório do sistema de certificados \_ \_ \_ , há também um repositório UserDS predefinido. Um repositório de cartão inteligente está planejado para esse local.

Aqui estão as lojas de sistema seguidas por comentários adicionais:

-   [\_ \_ usuário atual do repositório do sistema de \_ certificados \_](#cert_system_store_current_user)
-   [\_ \_ máquina local do repositório do sistema de \_ certificados \_](#cert_system_store_local_machine)
-   [\_ \_ serviço atual do repositório do sistema de \_ CERT. \_](#cert_system_store_current_service)
-   [\_serviços de \_ loja do sistema CERT \_](#cert_system_store_services)
-   [\_usuários do \_ repositório do sistema CERT \_](#cert_system_store_users)
-   [\_política de \_ \_ grupo de usuário atual do sistema \_ de certificado \_](#cert_system_current_user_group_policy)
-   [\_política de \_ \_ grupo do computador local do sistema \_ de CERT \_](#cert_system_local_machine_group_policy)
-   [\_máquina local do repositório do sistema de certificados \_ \_ \_ \_ Enterprise](#cert_system_store_local_machine_enterprise)
-   [Comentários](#remarks)

### <a name="cert_system_store_current_user"></a>\_ \_ usuário atual do repositório do sistema de \_ certificados \_

Os armazenamentos \_ \_ do sistema do usuário atual do repositório do sistema \_ de certificados \_ estão no seguinte local do registro:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         SystemCertificates
```

Os repositórios físicos predefinidos associados a esses armazenamentos do sistema são os seguintes.



| Armazenamento do sistema | Repositório físico                                           |
|--------------|----------------------------------------------------------|
| MY           | . Os                                                 |
| Root         | . Default. LocalMachine<br/> . Smart<br/>   |
| Confiar        | . Padrão. GroupPolicy<br/> . LocalMachine<br/> |
| AC           | . Padrão. GroupPolicy<br/> . LocalMachine<br/> |
| UserDS       | . UserCertificate                                         |



 

### <a name="cert_system_store_local_machine"></a>\_ \_ máquina local do repositório do sistema de \_ certificados \_

Os armazenamentos do sistema \_ \_ do computador local do repositório do sistema \_ de certificados \_ estão no seguinte local do registro:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         SystemCertificates
```

Os repositórios físicos predefinidos são associados a esses repositórios de sistema são os seguintes.



| Armazenamento do sistema | Repositório físico                                                                                    |
|--------------|---------------------------------------------------------------------------------------------------|
| MY           | . Os                                                                                          |
| Root         | . Padrão. AuthRoot<br/> . GroupPolicy<br/> . Porte<br/> . Smart<br/> |
| Confiar        | . Padrão. GroupPolicy<br/> . Porte<br/>                                            |
| AC           | . Padrão. GroupPolicy<br/> . Porte <br/>                                           |



 

### <a name="cert_system_store_current_service"></a>\_ \_ serviço atual do repositório do sistema de \_ CERT. \_

\_ \_ \_ \_ Os armazenamentos do sistema de serviço atual do repositório do sistema de certificados estão no seguinte local do registro:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

Os repositórios físicos predefinidos associados a esses armazenamentos do sistema são os seguintes.



| Armazenamento do sistema | Repositório físico                   |
|--------------|----------------------------------|
| MY           | . Os                         |
| Root         | . Default. LocalMachine<br/> |
| Confiar        | . Default. LocalMachine<br/> |
| AC           | . Default. LocalMachine<br/> |



 

### <a name="cert_system_store_services"></a>\_serviços de \_ loja do sistema CERT \_

\_ \_ \_ Os serviços de repositório do sistema de certificados são armazenados no seguinte local do registro:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

Os repositórios físicos predefinidos associados a esses armazenamentos do sistema são os seguintes.



| Armazenamento do sistema       | Repositório físico                   |
|--------------------|----------------------------------|
| Nome do \\ meu    | . Os                         |
| Raiz do ServiceName \\  | . Default. LocalMachine<br/> |
| Confiança do ServiceName \\ | . Default. LocalMachine<br/> |
| AC do ServiceName \\    | . Default. LocalMachine<br/> |



 

### <a name="cert_system_store_users"></a>\_usuários do \_ repositório do sistema CERT \_

\_ \_ Os usuários do repositório do sistema de certificados \_ armazenam o sistema no seguinte local do registro:

```
HKEY_USERS
   UserName
      Software
         Microsoft
            SystemCertificates
```

Os repositórios físicos predefinidos associados a esses armazenamentos do sistema são os seguintes.



| Armazenamento do sistema  | Repositório físico                   |
|---------------|----------------------------------|
| userid \\ My    | . Default. LocalMachine<br/> |
| raiz da userid \\  | . Default. LocalMachine<br/> |
| confiança de userid \\ | . Default. LocalMachine<br/> |
| \\AC da userid    | . Default. LocalMachine<br/> |



 

### <a name="cert_system_current_user_group_policy"></a>\_política de \_ \_ grupo de usuário atual do sistema \_ de certificado \_

\_ \_ \_ A política de grupo do usuário atual do sistema de certificados \_ \_ armazena o sistema no seguinte local do registro:

```
HKEY_CURRENT_USER
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_local_machine_group_policy"></a>\_política de \_ \_ grupo do computador local do sistema \_ de CERT \_

\_ \_ \_ A política de grupo do computador local do sistema de CERT \_ \_ repositórios do sistema está no seguinte local do registro:

```
HKEY_LOCAL_MACHINE
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_store_local_machine_enterprise"></a>\_máquina local do repositório do sistema de certificados \_ \_ \_ \_ Enterprise

O \_ computador local do repositório do sistema de certificados \_ \_ \_ \_ Enterprise contém certificados compartilhados entre domínios na empresa e baixados do diretório empresarial global. Para sincronizar a Enterprise Store do cliente, o diretório da empresa é sondado a cada oito horas e os certificados são baixados automaticamente em segundo plano.

Os repositórios físicos predefinidos associados a esses repositórios do sistema são os seguintes.



| Armazenamento do sistema | Repositório físico |
|--------------|----------------|
| MY           | . Os       |
| Root         | . Os       |
| Confiar        | . Os       |
| AC           | . Os       |



 

### <a name="remarks"></a>Comentários

Repositórios físicos adicionais podem ser associados a um repositório do sistema usando o [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).

O \_ \_ serviço de repositório do sistema CERT \_ e \_ os usuários do repositório do sistema de certificados \_ \_ são abertos por meio da prefixação do nome do repositório na cadeia de caracteres passada para  *pvPara* com o serviço ou nome de usuário, como ServiceName \\ **Trust** ou **.** \\ **My** padrão. O local dos usuários do repositório do sistema CERT \_ \_ ou do \_ CERT System Store \_ \_ \_ podem abrir o mesmo armazenamento no \_ serviço atual do sistema de CERT ou no \_ \_ \_ usuário atual do repositório do sistema de certificados \_ \_ \_ usando o Sid ( [*identificador de segurança*](../secgloss/s-gly.md) textual) do serviço ou usuário atual.

Os repositórios na política de \_ grupo do usuário da loja sistema de certificados \_ \_ \_ \_ e \_ \_ \_ na política de grupo do computador local do sistema de certificados \_ \_ em uma configuração de rede são baixados para o computador cliente do modelo de política de grupo (GPT) durante a inicialização do computador ou logon do usuário. Esses armazenamentos podem ser atualizados no computador cliente após a inicialização ou o logon quando o GPT é alterado no servidor de domínio por um administrador. A função [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) permite que um aplicativo seja notificado quando as lojas em qualquer um desses locais forem alteradas.

Os seguintes locais de armazenamento do sistema podem ser abertos remotamente:

-   \_ \_ máquina local do repositório do sistema de \_ certificados \_
-   \_política de \_ \_ grupo do \_ computador local do \_ repositório \_ do sistema de certificados
-   \_serviços de \_ loja do sistema CERT \_
-   \_usuários do \_ repositório do sistema CERT \_

Os locais da loja do sistema são abertos remotamente por meio da prefixação do nome do repositório na cadeia de caracteres passada para *pvPara* com o nome do computador. Exemplos de nomes de repositório do sistema remoto:

-   *ComputerName* \\ **AC**
-   \\\\*ComputerName* \\ **AC**
-   *ComputerName* \\ *ServiceName* \\ **Confiar**
-   \\\\*ComputerName* \\ *ServiceName* \\ **Confiar**

 

 
