---
description: SPI (interface do provedor de serviços) do Windows Sockets (Winsock).
ms.assetid: 59ac7ce6-10e7-40ac-bdce-dc01251b0bc5
title: SPI do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecf63a45f5175a86b8f5eb2a77ef0293182e38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752215"
---
# <a name="winsock-spi"></a><span data-ttu-id="18dbf-103">SPI do Winsock</span><span class="sxs-lookup"><span data-stu-id="18dbf-103">Winsock SPI</span></span>

<span data-ttu-id="18dbf-104">A interface do provedor de serviço do Winsock ou SPI do Winsock é uma disciplina especializada do Winsock usada para criar provedores; provedores de transporte, como as pilhas de protocolo TCP/IP ou IPX/SPX, usam a SPI do Winsock, como os provedores de namespace, como o DNS (sistema de cadastramento de domínio) da Internet.</span><span class="sxs-lookup"><span data-stu-id="18dbf-104">The Winsock Service Provider Interface, or Winsock SPI, is a specialized discipline of Winsock used to create providers; transport providers such as TCP/IP or IPX/SPX protocol stacks use the Winsock SPI, as do namespace providers such as the Internet's Domain Naming System (DNS).</span></span>

<span data-ttu-id="18dbf-105">Programação de rede tradicional, como permitir que aplicativos se comuniquem pela rede, não requer o uso de interfaces do Winsock SPI; em vez disso, use as interfaces padrão do [Winsock](winsock-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="18dbf-105">Traditional network programming, such as enabling applications to communicate over the network, does not require use of Winsock SPI interfaces; use standard [Winsock](winsock-reference.md) interfaces instead.</span></span>

 

<span data-ttu-id="18dbf-106">A SPI do Winsock usa a seguinte convenção de nomenclatura de prefixo de função.</span><span class="sxs-lookup"><span data-stu-id="18dbf-106">The Winsock SPI uses the following function prefix naming convention.</span></span>



| <span data-ttu-id="18dbf-107">Prefixo</span><span class="sxs-lookup"><span data-stu-id="18dbf-107">Prefix</span></span> | <span data-ttu-id="18dbf-108">Significado</span><span class="sxs-lookup"><span data-stu-id="18dbf-108">Meaning</span></span>                          | <span data-ttu-id="18dbf-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="18dbf-109">Description</span></span>                                       |
|--------|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="18dbf-110">WSP</span><span class="sxs-lookup"><span data-stu-id="18dbf-110">WSP</span></span>    | <span data-ttu-id="18dbf-111">Provedor de serviços do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="18dbf-111">Windows Sockets Service Provider</span></span> | <span data-ttu-id="18dbf-112">Pontos de entrada do provedor de serviço de transporte</span><span class="sxs-lookup"><span data-stu-id="18dbf-112">Transport service provider entry points</span></span>           |
| <span data-ttu-id="18dbf-113">WPU</span><span class="sxs-lookup"><span data-stu-id="18dbf-113">WPU</span></span>    | <span data-ttu-id="18dbf-114">Upchamada do provedor do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="18dbf-114">Windows Sockets Provider Upcall</span></span>  | <span data-ttu-id="18dbf-115">Ws2 \_ pontos de entrada de32.dll para provedores de serviço</span><span class="sxs-lookup"><span data-stu-id="18dbf-115">Ws2\_32.dll entry points for service providers</span></span>    |
| <span data-ttu-id="18dbf-116">WSC</span><span class="sxs-lookup"><span data-stu-id="18dbf-116">WSC</span></span>    | <span data-ttu-id="18dbf-117">Configuração do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="18dbf-117">Windows Sockets Configuration</span></span>    | <span data-ttu-id="18dbf-118">WS2 \_ pontos de entrada de32.dll para miniaplicativos de instalação</span><span class="sxs-lookup"><span data-stu-id="18dbf-118">WS2\_32.dll entry points for installation applets</span></span> |
| <span data-ttu-id="18dbf-119">NSP</span><span class="sxs-lookup"><span data-stu-id="18dbf-119">NSP</span></span>    | <span data-ttu-id="18dbf-120">Provedor de namespace</span><span class="sxs-lookup"><span data-stu-id="18dbf-120">Namespace Provider</span></span>               | <span data-ttu-id="18dbf-121">Pontos de entrada do provedor de namespace</span><span class="sxs-lookup"><span data-stu-id="18dbf-121">Namespace provider entry points</span></span>                   |



 

 

 



