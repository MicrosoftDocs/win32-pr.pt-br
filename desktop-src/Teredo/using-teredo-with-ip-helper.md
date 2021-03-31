---
title: Usando Teredo com auxiliar de IP
description: A API do auxiliar de protocolo de Internet (IP Helper) é utilizada por um aplicativo para coletar e fornecer informações importantes sobre a configuração de rede do computador local.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5936ce9987262fe24cfd6cf718a426b6123b89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641394"
---
# <a name="using-teredo-with-ip-helper"></a><span data-ttu-id="4bb5d-103">Usando Teredo com auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="4bb5d-103">Using Teredo with IP Helper</span></span>

<span data-ttu-id="4bb5d-104">A API do auxiliar de [protocolo de Internet](/windows/desktop/IpHlp/about-ip-helper) (IP Helper) é utilizada por um aplicativo para coletar e fornecer informações importantes sobre a configuração de rede do computador local.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-104">The [Internet Protocol Helper](/windows/desktop/IpHlp/about-ip-helper) (IP Helper) API is utilized by an application to gather and provide important information regarding the networking configuration of the local machine.</span></span> <span data-ttu-id="4bb5d-105">Ao operar na plataforma Windows Vista, essas informações incluem a porta UDP dinâmica atribuída à interface Teredo e as alterações que podem ocorrer na porta designada.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-105">When operating on the Windows Vista platform, this information includes the dynamic UDP port assigned to the Teredo interface and changes that may occur to the designated port.</span></span>

<span data-ttu-id="4bb5d-106">As funções a seguir são utilizadas pela API do auxiliar de IP para facilitar o uso da interface Teredo:</span><span class="sxs-lookup"><span data-stu-id="4bb5d-106">The following functions are utilized by the IP Helper API to facilitate the use of the Teredo interface:</span></span>

-   [<span data-ttu-id="4bb5d-107">**GetTeredoPort**</span><span class="sxs-lookup"><span data-stu-id="4bb5d-107">**GetTeredoPort**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="4bb5d-108">**NotifyTeredoPortChange**</span><span class="sxs-lookup"><span data-stu-id="4bb5d-108">**NotifyTeredoPortChange**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="4bb5d-109">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="4bb5d-109">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 