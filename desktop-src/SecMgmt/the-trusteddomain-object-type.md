---
description: sistemas baseados em Windows podem ter várias instâncias do tipo de objeto TrustedDomain.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: O tipo de objeto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab860f9192e48433242251578a20a45bf294164c0bffff8b6f00562a1442e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004834"
---
# <a name="the-trusteddomain-object-type"></a>O tipo de objeto TrustedDomain

sistemas baseados em Windows podem ter várias instâncias do tipo de objeto [**TrustedDomain**](trusteddomain-object.md) . Os objetos **TrustedDomain** têm dois campos que devem ser exclusivos entre todos os objetos **TrustedDomain** :

-   O nome do [ **TrustedDomain**](trusteddomain-object.md)
-   O Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) do [**TrustedDomain**](trusteddomain-object.md).

Uma tentativa de criar um novo objeto **TrustedDomain** com um nome ou um SID que já está sendo usado por outro objeto **TrustedDomain** será rejeitada.

 

 
