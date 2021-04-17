---
description: Ao criar um pacote de segurança do SSP (provedor de suporte de segurança), você não deve permitir que o cliente ingressado no domínio se autentique em um controlador de domínio usando um SPN (nome do provedor de serviços) de duas partes do formulário a seguir.
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: Usando nomes principais de três partes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8760ba740843c62c39a98e7e4683d25410a94ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754512"
---
# <a name="using-three-part-principal-names"></a><span data-ttu-id="46714-103">Usando nomes principais de três partes</span><span class="sxs-lookup"><span data-stu-id="46714-103">Using Three Part Principal Names</span></span>

<span data-ttu-id="46714-104">Ao criar um pacote de segurança do SSP (provedor de suporte de segurança), você não deve permitir que o cliente ingressado no domínio se autentique em um controlador de domínio usando um SPN (nome do provedor de serviços) de duas partes do formulário a seguir.</span><span class="sxs-lookup"><span data-stu-id="46714-104">When creating a security support provider (SSP) security package, you should not allow the domain joined client to authenticate to a domain controller by using a two part service provider name (SPN) of the following form.</span></span>

-   <span data-ttu-id="46714-105"><*protocolo* >/< do *nome do host*></span><span class="sxs-lookup"><span data-stu-id="46714-105"><*protocol*>/<*host name*></span></span>

<span data-ttu-id="46714-106">Um cliente sempre deve ser autenticado especificando o domínio.</span><span class="sxs-lookup"><span data-stu-id="46714-106">A client should always authenticate by specifying the domain.</span></span>

-   <span data-ttu-id="46714-107"><*protocolo* >/< do *nome* >/< do host *nome de domínio*></span><span class="sxs-lookup"><span data-stu-id="46714-107"><*protocol*>/<*host name*>/<*domain name*></span></span>

<span data-ttu-id="46714-108">Um cliente ingressado no domínio que faz logon com um SPN de duas partes pode ser capaz de representar o controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="46714-108">A domain joined client that logs on with a two part SPN may be able to impersonate the domain controller.</span></span> <span data-ttu-id="46714-109">Se você permitir dois SPNs de parte, deverá criar uma entrada de log que contenha informações suficientes para permitir que o administrador identifique o chamador.</span><span class="sxs-lookup"><span data-stu-id="46714-109">If you allow two part SPNs, you should create a log entry that contains enough information to enable the administrator to identify the caller.</span></span>

 

 



