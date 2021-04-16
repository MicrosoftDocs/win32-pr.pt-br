---
description: Os certificados podem ser solicitados e distribuídos por meio de qualquer mecanismo de transporte.
ms.assetid: 2cbd0cdb-eefa-4434-893d-20e8b34f4cfe
title: Independência de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8d68b8f6312495c242f6b2bd2ea75301f802c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752334"
---
# <a name="transport-independence"></a><span data-ttu-id="e7843-103">Independência de transporte</span><span class="sxs-lookup"><span data-stu-id="e7843-103">Transport Independence</span></span>

<span data-ttu-id="e7843-104">Os certificados podem ser solicitados e distribuídos por meio de qualquer mecanismo de transporte.</span><span class="sxs-lookup"><span data-stu-id="e7843-104">Certificates can be requested and distributed through any transport mechanism.</span></span> <span data-ttu-id="e7843-105">Os serviços de certificados aceitam [*solicitações de certificado*](../secgloss/c-gly.md) de um candidato por meio de http, DCOM, RPC, arquivo de disco ou transporte personalizado.</span><span class="sxs-lookup"><span data-stu-id="e7843-105">Certificate Services accepts [*certificate requests*](../secgloss/c-gly.md) from an applicant through HTTP, DCOM, RPC, disk file, or by custom transport.</span></span> <span data-ttu-id="e7843-106">Os serviços de certificados enviam certificados para o candidato por meio de HTTP, DCOM, RPC, arquivo de disco ou transporte personalizado.</span><span class="sxs-lookup"><span data-stu-id="e7843-106">Certificate Services posts certificates to the applicant through HTTP, DCOM, RPC, disk file, or custom transport.</span></span>

<span data-ttu-id="e7843-107">Os transportes são suportados por aplicativos intermediários e DLLs de módulo de saída, geralmente escritos em C/C++.</span><span class="sxs-lookup"><span data-stu-id="e7843-107">Transports are supported by intermediary applications and exit module DLLs, usually written in C/C++.</span></span> <span data-ttu-id="e7843-108">Os aplicativos intermediários e os módulos de saída isolam as funções dos serviços de certificados de se comunicar com qualquer transporte específico.</span><span class="sxs-lookup"><span data-stu-id="e7843-108">The intermediary applications and exit modules isolate Certificate Services functions from communicating with any specific transport.</span></span>

 

 
