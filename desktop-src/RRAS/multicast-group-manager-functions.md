---
title: Funções do Gerenciador de Grupos multicast
description: As funções a seguir são usadas para se registrar no gerenciador de grupos multicast
ms.assetid: d4374ced-06ea-49dd-8f52-0d06612aa4c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d32ecaa5bc30aa9563ac15383cf17d9308c6c17b416b31a6c2b03b8b55d0710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790380"
---
# <a name="multicast-group-manager-functions"></a>Funções do Gerenciador de Grupos multicast

As seguintes funções são usadas para se registrar no gerenciador de grupos multicast:

[**MgmRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmregistermprotocol)

[**MgmDeRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol)

As seguintes funções são usadas para gerenciar a propriedade da interface:

[**MgmGetProtocolOnInterface**](/windows/desktop/api/Mgm/nf-mgm-mgmgetprotocoloninterface)

[**MgmTakeInterfaceOwnership**](/windows/desktop/api/Mgm/nf-mgm-mgmtakeinterfaceownership)

[**MgmReleaseInterfaceOwnership**](/windows/desktop/api/Mgm/nf-mgm-mgmreleaseinterfaceownership)

As seguintes funções são usadas para gerenciar a associação de grupo:

[**MgmAddGroupMembershipEntry**](/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry)

[**MgmDeleteGroupMembershipEntry**](/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry)

As seguintes funções são usadas para obter MFEs (entradas de encaminhamento multicast) e estatísticas MFE:

[**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe)

[**MgmGetNextMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe)

[**MgmGetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe)

[**MgmGetFirstMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats)

[**MgmGetNextMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats)

[**MgmGetMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats)

A função a seguir é usada para modificar MFEs:

[**MgmSetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe)

As funções a seguir são usadas para obter uma lista de grupos que foram ingressados:

[**MgmGroupEnumerationStart**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart)

[**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext)

[**MgmGroupEnumerationEnd**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend)

 

 




