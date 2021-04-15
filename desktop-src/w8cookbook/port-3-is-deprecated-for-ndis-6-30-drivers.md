---
title: A porta 3 foi preterida para drivers NDIS 6,30
description: A porta 3 foi preterida para drivers NDIS 6,30
ms.assetid: 900BD08D-3EAF-43F3-A74A-359815474FAD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0b4c7f6a33b179a14d3d7f8151d3850e16dd44
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104454409"
---
# <a name="port-3-is-deprecated-for-ndis-630-drivers"></a><span data-ttu-id="6e31a-103">A porta 3 foi preterida para drivers NDIS 6,30</span><span class="sxs-lookup"><span data-stu-id="6e31a-103">Port 3 is deprecated for NDIS 6.30 drivers</span></span>

## <a name="platforms"></a><span data-ttu-id="6e31a-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="6e31a-104">Platforms</span></span>

<span data-ttu-id="6e31a-105">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="6e31a-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="6e31a-106">**Servidores** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6e31a-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="6e31a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6e31a-107">Description</span></span>

<span data-ttu-id="6e31a-108">O Windows 8 remove o suporte de plataforma para drivers WLAN da miniporta NDIS para criar ou iniciar a porta de extensibilidade do IHV (também conhecida como 3ª porta).</span><span class="sxs-lookup"><span data-stu-id="6e31a-108">Windows 8 removes platform support for NDIS miniport WLAN drivers to create or start up the IHV extensibility port (also known as 3rd port).</span></span> <span data-ttu-id="6e31a-109">Esse recurso foi introduzido no Windows 7 como uma medida paliativa enquanto a WFA (Aliança de Wi-Fi) desenvolveu a especificação Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="6e31a-109">This feature was introduced in Windows 7 as a stopgap measure while the Wi-Fi Alliance (WFA) developed the Wi-Fi Direct specification.</span></span> <span data-ttu-id="6e31a-110">A especificação agora está concluída, os produtos que usam Wi-Fi Direct estão sendo certificados e o Windows 8 introduz uma pilha nativa Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="6e31a-110">The specification is now finished, products using Wi-Fi Direct are being certified, and Windows 8 introduces a native Wi-Fi Direct stack.</span></span>

## <a name="manifestation"></a><span data-ttu-id="6e31a-111">Manifestação</span><span class="sxs-lookup"><span data-stu-id="6e31a-111">Manifestation</span></span>

<span data-ttu-id="6e31a-112">Nada, pois a terceira porta é uma funcionalidade de plataforma que os drivers de miniporta WLAN iniciam se precisarem dessa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="6e31a-112">Nothing, as third port is a platform capability that WLAN miniport drivers start up if they need this functionality.</span></span>

## <a name="solution"></a><span data-ttu-id="6e31a-113">Solução</span><span class="sxs-lookup"><span data-stu-id="6e31a-113">Solution</span></span>

<span data-ttu-id="6e31a-114">Estamos mantendo o recurso de porta de extensibilidade disponível para drivers existentes que não relatam o NDIS 6,30 para manter a compatibilidade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6e31a-114">We are keeping the extensibility port feature available for existing drivers that do not report NDIS 6.30 to maintain device compatibility.</span></span> <span data-ttu-id="6e31a-115">No entanto, novos drivers WLAN que relatam a NDIS 6,30 não poderão iniciar essa porta; em vez disso, os desenvolvedores desses drivers devem usar o Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="6e31a-115">However, new WLAN drivers that report NDIS 6.30 will not be able to start this port; instead, developers of these drivers should use Wi-Fi Direct.</span></span>

 

 




