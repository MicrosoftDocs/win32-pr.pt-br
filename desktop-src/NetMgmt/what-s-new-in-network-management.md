---
title: O que há de novo no gerenciamento de rede
description: O que há de novo no gerenciamento de rede
ms.assetid: f805b662-1807-4703-b27e-4721895fe450
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e688d340b8282015b99ccb3d7fa6404dfa332748
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104366898"
---
# <a name="whats-new-in-network-management"></a>O que há de novo no gerenciamento de rede

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 e Windows Server 2012

O Microsoft Windows 8 apresenta novos recursos de programação de gerenciamento de rede. Esses novos elementos estendem a funcionalidade do gerenciamento de rede para criar pacotes de provisionamento para operações de ingresso no domínio offline ao provisionar computadores com o Windows 8.

A seguir estão as novas funções de gerenciamento de rede:

-   [**NetCreateProvisioningPackage**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [**NetRequestProvisioningPackageInstall**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall)

A seguir estão as novas estruturas de gerenciamento de rede:

-   [**parâmetros de provisionamento do Netsetup \_ \_**](/windows/desktop/api/Lmjoin/ns-lmjoin-netsetup_provisioning_params)
-   [**Informações do usuário \_ \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24)

A função [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) foi aprimorada no Windows 8 para dar suporte a um novo nível de informações e retornar uma estrutura de informações de [**usuário \_ \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) com informações de conta de usuário para uma conta conectada a uma identidade de Internet.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

O Microsoft Windows 7 apresenta novos recursos de programação de gerenciamento de rede. Esses elementos estendem a capacidade do gerenciamento de rede para permitir operações de ingresso no domínio offline ao provisionar computadores com o Windows 7.

A seguir estão as novas funções de gerenciamento de rede:

-   [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [**NetRequestOfflineDomainJoin**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)

As seguintes funções de gerenciamento de rede existentes foram aprimoradas para dar suporte a opções adicionais:

-   [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)

## <a name="windows-server-2003"></a>Windows Server 2003

O Microsoft Windows Server 2003 apresenta novos recursos de programação de gerenciamento de rede. Esses elementos estendem o recurso de operações de gerenciamento de rede no Windows Server 2003 e posterior.

## <a name="windows-xp"></a>Windows XP

O Microsoft Windows XP apresenta novos recursos de programação de gerenciamento de rede. Esses elementos estendem o recurso de operações de gerenciamento de rede no Windows XP e versões posteriores.

A seguir estão as novas funções de gerenciamento de rede:

-   [**NetAddAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)
-   [**NetEnumerateComputerNames**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)
-   [**NetRemoveAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)
-   [**NetSetPrimaryComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)
-   [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation)

 

 




