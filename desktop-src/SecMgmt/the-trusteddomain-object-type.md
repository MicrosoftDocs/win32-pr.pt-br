---
description: Os sistemas baseados no Windows podem ter várias instâncias do tipo de objeto TrustedDomain.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: O tipo de objeto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0a4e6eca0790d877a9a23e4d83725d4e80798
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646989"
---
# <a name="the-trusteddomain-object-type"></a>O tipo de objeto TrustedDomain

Os sistemas baseados no Windows podem ter várias instâncias do tipo de objeto [**TrustedDomain**](trusteddomain-object.md) . Os objetos **TrustedDomain** têm dois campos que devem ser exclusivos entre todos os objetos **TrustedDomain** :

-   O nome do [ **TrustedDomain**](trusteddomain-object.md)
-   O Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) do [**TrustedDomain**](trusteddomain-object.md).

Uma tentativa de criar um novo objeto **TrustedDomain** com um nome ou um SID que já está sendo usado por outro objeto **TrustedDomain** será rejeitada.

 

 
