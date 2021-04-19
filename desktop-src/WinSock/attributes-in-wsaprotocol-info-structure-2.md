---
description: XP1 \_ oferece suporte \_ a parâmetros de atributo MultiPoint, XP1 \_ MultiPoint \_ Control \_ e XP1 \_ MultiPoint \_ Data \_ plano na estrutura de informações do Winsock WSAPROTOCOL \_ .
ms.assetid: 62f5b8b0-a404-49d1-b163-026f79a46845
title: Atributos na estrutura WSAPROTOCOL_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39ea2905da3228860d4fe22f5a0f0d954ce0624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814434"
---
# <a name="attributes-in-wsaprotocol_info-structure"></a><span data-ttu-id="cdf46-103">Atributos na estrutura de informações de WSAPROTOCOL \_</span><span class="sxs-lookup"><span data-stu-id="cdf46-103">Attributes in WSAPROTOCOL\_INFO Structure</span></span>

<span data-ttu-id="cdf46-104">Para dar suporte à taxonomia descrita acima, três parâmetros de atributo na estrutura [**de \_ informações WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) são usados para distinguir os esquemas usados nos planos de controle e de dados, respectivamente:</span><span class="sxs-lookup"><span data-stu-id="cdf46-104">In support of the taxonomy described above, three attribute parameters in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure are used to distinguish the schemes used in the control and data planes respectively:</span></span>

-   <span data-ttu-id="cdf46-105">XP1 \_ suporte \_ a MultiPoint com um valor de 1 indica que essa entrada de protocolo dá suporte a comunicações do MultiPoint e que os dois parâmetros a seguir são significativos.</span><span class="sxs-lookup"><span data-stu-id="cdf46-105">XP1\_SUPPORT\_MULTIPOINT with a value of 1 indicates this protocol entry supports multipoint communications, and that the following two parameters are meaningful.</span></span>
-   <span data-ttu-id="cdf46-106">\_ \_ \_ O plano de controle do MultiPoint XP1 indica se o plano de controle tem raiz (valor = 1) ou não raiz (valor = 0).</span><span class="sxs-lookup"><span data-stu-id="cdf46-106">XP1\_MULTIPOINT\_CONTROL\_PLANE indicates whether the control plane is rooted (value = 1) or nonrooted (value = 0).</span></span>
-   <span data-ttu-id="cdf46-107">\_ \_ \_ O plano de dados do MultiPoint XP1 indica se o plano de dados tem raiz (valor = 1) ou não raiz (valor = 0).</span><span class="sxs-lookup"><span data-stu-id="cdf46-107">XP1\_MULTIPOINT\_DATA\_PLANE indicates whether the data plane is rooted (value = 1) or nonrooted (value = 0).</span></span>

<span data-ttu-id="cdf46-108">Observe que duas entradas de [**\_ informações WSAPROTOCOLs**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) estarão presentes se um protocolo multiponto tiver suporte para os planos de dados com e sem raiz, uma entrada para cada um.</span><span class="sxs-lookup"><span data-stu-id="cdf46-108">Note that two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entries would be present if a multipoint protocol supported both rooted and nonrooted data planes, one entry for each.</span></span>

<span data-ttu-id="cdf46-109">O aplicativo pode usar o [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) para descobrir se há suporte para comunicações do MultiPoint para um determinado protocolo e, em caso afirmativo, como há suporte em relação aos planos de controle e de dados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="cdf46-109">The application can use [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) to discover whether multipoint communications is supported for a given protocol and, if so, how it is supported with respect to the control and data planes, respectively.</span></span>

 

 
