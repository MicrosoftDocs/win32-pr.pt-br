---
title: Modificando configuração de partição de diretório de aplicativo
description: Uma partição de diretório de aplicativo pode ser modificada alterando determinados atributos do objeto crossRef que representa a partição de diretório de aplicativo.
ms.assetid: c4db5b3f-7d80-46a0-8a3a-9b1eb3c9f7b1
ms.tgt_platform: multiple
keywords:
- Modificando o AD de configuração de partição de diretório de aplicativo
- AD de partições de diretório de aplicativo, modificando configuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c976c297e8491dbb87a32cf2241446ca0403e7f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823651"
---
# <a name="modifying-application-directory-partition-configuration"></a>Modificando configuração de partição de diretório de aplicativo

Uma partição de diretório de aplicativo pode ser modificada alterando determinados atributos do objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa a partição de diretório de aplicativo. Para localizar o objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa uma partição de diretório de aplicativo específica, pesquise o contêiner partições em busca de um objeto **crossRef** que tenha um valor de atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) igual ao nome distinto da partição de diretório do aplicativo. O nome distinto do objeto **crossRef** pode ser usado para associar ao objeto **crossRef** .

A tabela a seguir lista os atributos do objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que podem ser modificados.

| Atributo                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**msDS-Replication-Notify-primeiro-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay)           | Especifica o atraso, em segundos, após a alteração de um objeto de origem antes que o primeiro parceiro de replicação seja notificado. Para obter mais informações, consulte [replicação de partição de diretório de aplicativo](application-directory-partition-replication.md).                                                                                                   |
| [**msDS-Replication-Notify-subseqüente-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) | Especifica o atraso, em segundos, entre as notificações subsequentes para o segundo, terceiro, e assim por diante de parceiros de replicação. Para obter mais informações, consulte [replicação de partição de diretório de aplicativo](application-directory-partition-replication.md).                                                                                                 |
| [**msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain)                                             | Identifica o domínio que o subsistema de segurança usa para interpretar referências de domínio local nos atributos [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) de objetos nessa partição de diretório de aplicativo. Para obter mais informações, consulte [segurança de partição de diretório de aplicativo](application-directory-partition-security.md). |
| [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)                                       | Contém o nome distinto do objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) para cada controlador de domínio que hospeda uma réplica da partição de diretório do aplicativo. Para obter mais informações, consulte [adicionando ou excluindo uma réplica de partição de diretório de aplicativo](adding-or-deleting-an-application-directory-partition-replica.md).            |



 

 

 