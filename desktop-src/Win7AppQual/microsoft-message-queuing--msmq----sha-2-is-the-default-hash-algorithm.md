---
description: MSMQ (enfileiramento de mensagens da Microsoft)-o SHA 2 é o algoritmo de hash padrão
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: MSMQ (enfileiramento de mensagens da Microsoft)-o SHA 2 é o algoritmo de hash padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2b73e347f5d5a768780afc5d2153909c6f5a9a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088094"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a><span data-ttu-id="cc8bc-103">MSMQ (enfileiramento de mensagens da Microsoft)-o SHA 2 é o algoritmo de hash padrão</span><span class="sxs-lookup"><span data-stu-id="cc8bc-103">Microsoft Message Queuing (MSMQ) - SHA 2 Is the Default Hash Algorithm</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="cc8bc-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="cc8bc-104">Affected Platforms</span></span>

 <span data-ttu-id="cc8bc-105">**Clientes** -Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="cc8bc-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="cc8bc-106">**Servidores** -windows Server 2003, windows Server 2008, windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cc8bc-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="cc8bc-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="cc8bc-107">Feature Impact</span></span>

 <span data-ttu-id="cc8bc-108">**Severidade** -baixa</span><span class="sxs-lookup"><span data-stu-id="cc8bc-108">**Severity** - Low</span></span>  
<span data-ttu-id="cc8bc-109">**Frequência** -baixa</span><span class="sxs-lookup"><span data-stu-id="cc8bc-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="cc8bc-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc8bc-110">Description</span></span>

<span data-ttu-id="cc8bc-111">No Windows 7, o MSMQ usa o SHA-2 como padrão ao assinar uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="cc8bc-111">In Windows 7, MSMQ uses SHA-2 as the default when signing an outgoing message.</span></span> <span data-ttu-id="cc8bc-112">Além disso, todas as mensagens de entrada devem ser assinadas com SHA-2.</span><span class="sxs-lookup"><span data-stu-id="cc8bc-112">Additionally, all incoming messages must be signed with SHA-2.</span></span> <span data-ttu-id="cc8bc-113">Você pode habilitar o suporte para um algoritmo de criptografia inferior por meio de uma chave do registro acessível pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="cc8bc-113">You can enable support for a lower encryption algorithm through an administrator-accessible registry key.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="cc8bc-114">Manifestação do impacto</span><span class="sxs-lookup"><span data-stu-id="cc8bc-114">Manifestation of Impact</span></span>

-   <span data-ttu-id="cc8bc-115">O MSMQ no Windows 2003 ou inferior não aceitará mensagens assinadas provenientes do MSMQ no Windows 7</span><span class="sxs-lookup"><span data-stu-id="cc8bc-115">MSMQ in Windows 2003 or below will not accept signed messages originating from MSMQ in Windows 7</span></span>
-   <span data-ttu-id="cc8bc-116">O MSMQ no Windows 7 não aceitará mensagens assinadas provenientes do Windows 2008 ou abaixo</span><span class="sxs-lookup"><span data-stu-id="cc8bc-116">MSMQ in Windows 7 will not accept signed messages originating from Windows 2008 or below</span></span>

## <a name="mitigation"></a><span data-ttu-id="cc8bc-117">Atenuação</span><span class="sxs-lookup"><span data-stu-id="cc8bc-117">Mitigation</span></span>

<span data-ttu-id="cc8bc-118">Os usuários devem considerar a atualização para o Windows 7 para aproveitar o algoritmo de assinatura mais forte.</span><span class="sxs-lookup"><span data-stu-id="cc8bc-118">Users should consider upgrading to Windows 7 to leverage the stronger signing algorithm.</span></span> <span data-ttu-id="cc8bc-119">Para habilitar a troca direta de mensagens assinadas entre o Windows 7 e qualquer sistema operacional de nível inferior, o administrador deve adicionar as exceções apropriadas nas máquinas MSMQ.</span><span class="sxs-lookup"><span data-stu-id="cc8bc-119">To enable seamless signed message exchange between Windows 7 and any down-level operating system, the Administrator must add appropriate exceptions on the MSMQ machines.</span></span>

 

 



