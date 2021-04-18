---
description: O túnel automático com endereços compatíveis com IPv4 e o 6to4 funcionam por meio de uma rota para um prefixo que está no link para a interface \# 2. Os bits 32 após o prefixo são extraídos e usados como um endereço de destino IPv4 para o pacote encapsulado.
ms.assetid: 92261a1b-2b7f-4a76-b98a-2631dc303618
title: Túnel automático IPv6 e 6to4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede1179902a7ec3276058e078d56e069603e54a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787659"
---
# <a name="ipv6-automatic-tunneling-and-6to4"></a><span data-ttu-id="03e93-104">Túnel automático IPv6 e 6to4</span><span class="sxs-lookup"><span data-stu-id="03e93-104">IPv6 Automatic Tunneling and 6to4</span></span>

<span data-ttu-id="03e93-105">O túnel automático com endereços compatíveis com IPv4 e o 6to4 funcionam por meio de uma rota para um prefixo que está no link para a interface \# 2.</span><span class="sxs-lookup"><span data-stu-id="03e93-105">Automatic tunneling with IPv4-compatible addresses and 6to4 both work through a route for a prefix that is on-link to interface \#2.</span></span> <span data-ttu-id="03e93-106">Os bits 32 após o prefixo são extraídos e usados como um endereço de destino IPv4 para o pacote encapsulado.</span><span class="sxs-lookup"><span data-stu-id="03e93-106">The 32 bits following the prefix are extracted and used as an IPv4 destination address for the encapsulated packet.</span></span>

<span data-ttu-id="03e93-107">O túnel automático usa o prefixo::/96, que é habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="03e93-107">Automatic tunneling uses the ::/96 prefix, which is enabled by default.</span></span> <span data-ttu-id="03e93-108">Ele pode ser desabilitado removendo a rota para::/96.</span><span class="sxs-lookup"><span data-stu-id="03e93-108">It can be disabled by removing the route for ::/96.</span></span>

<span data-ttu-id="03e93-109">o 6to4 usa o prefixo 2002::/16, que não está habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="03e93-109">6to4 uses the 2002::/16 prefix, which is not enabled by default.</span></span>

 

 



