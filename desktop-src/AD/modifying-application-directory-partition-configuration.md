---
title: Modificando a configuração de partição do diretório do aplicativo
description: Uma partição de diretório do aplicativo pode ser modificada alterando determinados atributos do objeto crossRef que representa a partição de diretório do aplicativo.
ms.assetid: c4db5b3f-7d80-46a0-8a3a-9b1eb3c9f7b1
ms.tgt_platform: multiple
keywords:
- Modificando o AD de Configuração da Partição do Diretório do Aplicativo
- Application Directory Partitions AD , Modificando a configuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc378536a552bb7612877fc09913fdbad9daf507adbb34b5f53f8946c946e8ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186311"
---
# <a name="modifying-application-directory-partition-configuration"></a>Modificando a configuração de partição do diretório do aplicativo

Uma partição de diretório do aplicativo pode ser modificada alterando determinados atributos do [**objeto crossRef**](/windows/desktop/ADSchema/c-crossref) que representa a partição de diretório do aplicativo. Para localizar o objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa uma partição de diretório de aplicativo específica, pesquise no contêiner Partições um objeto **crossRef** que tenha um valor de atributo [**nCName**](/windows/desktop/ADSchema/a-ncname) que seja igual ao nome diferenciado da partição de diretório do aplicativo. O nome diferenciado do objeto **crossRef** pode ser usado para se vincular ao **objeto crossRef.**

A tabela a seguir lista atributos do [**objeto crossRef**](/windows/desktop/ADSchema/c-crossref) que podem ser modificados.

| Atributo                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**msDS-Replication-Notify-First-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay)           | Especifica o atraso, em segundos, após uma alteração de objeto de origem antes que o primeiro parceiro de replicação seja notificado. Para obter mais informações, consulte Application [Directory Partition Replication](application-directory-partition-replication.md).                                                                                                   |
| [**msDS-Replication-Notify-Subsequent-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) | Especifica o atraso, em segundos, entre as notificações subsequentes para o segundo, o terceiro e assim por diante nos parceiros de replicação. Para obter mais informações, consulte Application [Directory Partition Replication](application-directory-partition-replication.md).                                                                                                 |
| [**msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain)                                             | Identifica o domínio que o subsistema de segurança usa para interpretar referências de domínio local nos atributos [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) de objetos nessa partição de diretório do aplicativo. Para obter mais informações, consulte [Segurança de partição do Diretório do Aplicativo](application-directory-partition-security.md). |
| [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)                                       | Contém o nome diferenciado do objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) para cada controlador de domínio que hospeda uma réplica da partição de diretório do aplicativo. Para obter mais informações, consulte [Adicionando ou excluindo uma réplica de partição do diretório do aplicativo.](adding-or-deleting-an-application-directory-partition-replica.md)            |



 

 

 