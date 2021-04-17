---
description: O ATM é aplicável a ambientes de LAN e WAN.
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Anexo ATM do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ec056cc2b84c9449ed466a60a15683df29744b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811727"
---
# <a name="winsock-atm-annex"></a><span data-ttu-id="56f79-103">Anexo ATM do Winsock</span><span class="sxs-lookup"><span data-stu-id="56f79-103">Winsock ATM Annex</span></span>

<span data-ttu-id="56f79-104">O ATM é aplicável a ambientes de LAN e WAN.</span><span class="sxs-lookup"><span data-stu-id="56f79-104">ATM is applicable to both LAN and WAN environments.</span></span> <span data-ttu-id="56f79-105">Uma rede ATM transporta simultaneamente uma ampla variedade de tráfego de rede: voz, dados, imagem e vídeo.</span><span class="sxs-lookup"><span data-stu-id="56f79-105">An ATM network simultaneously transports a wide variety of network traffic — voice, data, image, and video.</span></span> <span data-ttu-id="56f79-106">Ele fornece aos usuários uma qualidade de serviço garantida em uma base de VC (por canal virtual).</span><span class="sxs-lookup"><span data-stu-id="56f79-106">It provides users with a guaranteed quality of service on a per-virtual channel (VC) basis.</span></span>



| <span data-ttu-id="56f79-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="56f79-107">Element</span></span>          | <span data-ttu-id="56f79-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="56f79-108">Description</span></span>                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56f79-109">Nome (s) de protocolo</span><span class="sxs-lookup"><span data-stu-id="56f79-109">Protocol name(s)</span></span> | <span data-ttu-id="56f79-110">ATMPROTO \_ AAL5, ATMPROTO \_ AALUSER</span><span class="sxs-lookup"><span data-stu-id="56f79-110">ATMPROTO\_AAL5, ATMPROTO\_AALUSER</span></span>                                                                                                                           |
| <span data-ttu-id="56f79-111">Description</span><span class="sxs-lookup"><span data-stu-id="56f79-111">Description</span></span>      | <span data-ttu-id="56f79-112">O ATM AAL5 fornece um serviço de transporte orientado por conexão, limite de mensagens preservado e QOS garantido.</span><span class="sxs-lookup"><span data-stu-id="56f79-112">ATM AAL5 provides a transport service that is connection oriented, message-boundary preserved, and QOS guaranteed.</span></span> <span data-ttu-id="56f79-113">ATMPROTO \_ AALUSER é uma AAL definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="56f79-113">ATMPROTO\_AALUSER is a user-defined AAL.</span></span> |
| <span data-ttu-id="56f79-114">Família de endereços</span><span class="sxs-lookup"><span data-stu-id="56f79-114">Address family</span></span>   | <span data-ttu-id="56f79-115">\_ATM AF</span><span class="sxs-lookup"><span data-stu-id="56f79-115">AF\_ATM</span></span>                                                                                                                                                     |
| <span data-ttu-id="56f79-116">Arquivo de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="56f79-116">Header file</span></span>      | <span data-ttu-id="56f79-117">Ws2atm. h</span><span class="sxs-lookup"><span data-stu-id="56f79-117">Ws2atm.h</span></span>                                                                                                                                                    |



 

<span data-ttu-id="56f79-118">Esta seção descreve as extensões específicas do modo de transferência assíncrona (ATM) necessárias para dar suporte aos serviços ATM nativos como expostos e especificados na especificação de UNI (interface de rede do usuário) do fórum do ATM versão 3. x (3,0 e 3,1).</span><span class="sxs-lookup"><span data-stu-id="56f79-118">This section describes the Asynchronous Transfer Mode (ATM)-specific extensions needed to support the native ATM services as exposed and specified in the ATM Forum User Network Interface (UNI) specification version 3.x (3.0 and 3.1).</span></span> <span data-ttu-id="56f79-119">Este documento dá suporte a AAL tipo 5 (modo de mensagem) e AAL definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="56f79-119">This document supports AAL type 5 (message mode) and user-defined AAL.</span></span> <span data-ttu-id="56f79-120">As versões futuras deste documento irão dar suporte a outros tipos de AAL, bem como a UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="56f79-120">Future versions of this document will support other types of AAL as well as UNI 4.0.</span></span>

 

 



