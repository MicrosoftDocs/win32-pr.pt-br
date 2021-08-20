---
title: Partições de diretório de aplicativos
description: no Windows Server 2003, Active Directory Domain Services suporte a partições de diretório de aplicativos.
ms.assetid: 55c47803-c1ee-4888-bb19-103374ec9719
ms.tgt_platform: multiple
keywords:
- AD de partições do diretório de aplicativos
- AD de partições de diretório de aplicativo, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d90532c813dde406fae3104b56ab2e68065145cf893b145f6148f39e6c1007e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024247"
---
# <a name="application-directory-partitions"></a>Partições de diretório de aplicativos

no Windows Server 2003, Active Directory Domain Services suporte a partições de diretório de aplicativos. Uma partição de diretório de aplicativo pode conter uma hierarquia de qualquer tipo de objeto, exceto entidades de segurança, e pode ser configurada para replicar para qualquer conjunto de controladores de domínio na floresta. Ao contrário de uma partição de domínio, uma partição de diretório de aplicativo não precisa ser replicada para todos os controladores de domínio em um domínio e a partição pode ser replicada para controladores de domínio em domínios diferentes da floresta. Para obter mais informações sobre partições de diretório de aplicativos, consulte [sobre partições de diretório de aplicativo](about-application-directory-partitions.md).

Uma partição de diretório de aplicativo pode ser criada. modificado e excluído usando as operações padrão ADSI, LDAP e [System. DirectoryServices](/dotnet/api/system.directoryservices) . O contexto de segurança necessário para criar e modificar uma partição de diretório de aplicativo é o mesmo que para criar uma partição de domínio.

Os tópicos a seguir descrevem como trabalhar com partições de diretório de aplicativo:

-   [Replicação de partição de diretório de aplicativo](application-directory-partition-replication.md)
-   [Segurança de partição de diretório de aplicativo](application-directory-partition-security.md)
-   [Criando uma partição de diretório de aplicativo](creating-an-application-directory-partition.md)
-   [Excluindo uma partição de diretório de aplicativo](deleting-an-application-directory-partition.md)
-   [Enumerando partições de diretório de aplicativo em uma floresta](enumerating-application-directory-partitions-in-a-forest.md)
-   [Localizando um servidor de host de partição de diretório de aplicativo](locating-an-application-directory-partition-host-server.md)
-   [Adicionando ou excluindo uma réplica de partição de diretório de aplicativo](adding-or-deleting-an-application-directory-partition-replica.md)
-   [Enumerando réplicas de uma partição de diretório de aplicativo](enumerating-replicas-of-an-application-directory-partition.md)
-   [Modificando configuração de partição de diretório de aplicativo](modifying-application-directory-partition-configuration.md)

 

 