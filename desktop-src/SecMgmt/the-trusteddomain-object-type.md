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
# <a name="the-trusteddomain-object-type"></a><span data-ttu-id="b07ce-103">O tipo de objeto TrustedDomain</span><span class="sxs-lookup"><span data-stu-id="b07ce-103">The TrustedDomain Object Type</span></span>

<span data-ttu-id="b07ce-104">Os sistemas baseados no Windows podem ter várias instâncias do tipo de objeto [**TrustedDomain**](trusteddomain-object.md) .</span><span class="sxs-lookup"><span data-stu-id="b07ce-104">Windows-based systems can have multiple instances of the [**TrustedDomain**](trusteddomain-object.md) object type.</span></span> <span data-ttu-id="b07ce-105">Os objetos **TrustedDomain** têm dois campos que devem ser exclusivos entre todos os objetos **TrustedDomain** :</span><span class="sxs-lookup"><span data-stu-id="b07ce-105">**TrustedDomain** objects have two fields that must be unique among all **TrustedDomain** objects:</span></span>

-   <span data-ttu-id="b07ce-106">O nome do [ **TrustedDomain**](trusteddomain-object.md)</span><span class="sxs-lookup"><span data-stu-id="b07ce-106">The name of the [**TrustedDomain**](trusteddomain-object.md)</span></span>
-   <span data-ttu-id="b07ce-107">O Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) do [**TrustedDomain**](trusteddomain-object.md).</span><span class="sxs-lookup"><span data-stu-id="b07ce-107">The [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the [**TrustedDomain**](trusteddomain-object.md).</span></span>

<span data-ttu-id="b07ce-108">Uma tentativa de criar um novo objeto **TrustedDomain** com um nome ou um SID que já está sendo usado por outro objeto **TrustedDomain** será rejeitada.</span><span class="sxs-lookup"><span data-stu-id="b07ce-108">An attempt to create a new **TrustedDomain** object with either a name or SID that is already in use by another **TrustedDomain** object will be rejected.</span></span>

 

 
