---
title: StorAHCI substitui MSAHCI
description: StorAHCI substitui MSAHCI
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a41a9b113ba33c35e3a1a1c4b2ea5dad3054c8
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "105761514"
---
# <a name="storahci-replaces-msahci"></a><span data-ttu-id="500d2-103">StorAHCI substitui MSAHCI</span><span class="sxs-lookup"><span data-stu-id="500d2-103">StorAHCI replaces MSAHCI</span></span>

## <a name="platforms"></a><span data-ttu-id="500d2-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="500d2-104">Platforms</span></span>

<span data-ttu-id="500d2-105">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="500d2-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="500d2-106">**Servidores** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="500d2-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="500d2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="500d2-107">Description</span></span>

<span data-ttu-id="500d2-108">O StorAHCI, uma miniporta Storport, dá suporte aos controladores AHCI (Serial Advanced Technology Attachment) avançados do controlador de host no Windows e substitui o MSAHCI, uma miniporta ATAport.</span><span class="sxs-lookup"><span data-stu-id="500d2-108">StorAHCI, a Storport miniport, supports serial advanced technology attachment (SATA) advanced host controller interface (AHCI) controllers in Windows, and replaces MSAHCI, an ATAport miniport.</span></span>

## <a name="manifestation"></a><span data-ttu-id="500d2-109">Manifestação</span><span class="sxs-lookup"><span data-stu-id="500d2-109">Manifestation</span></span>

<span data-ttu-id="500d2-110">Não deve haver nenhuma alteração na funcionalidade ou no desempenho; Esse driver dá suporte a todos os mesmos dispositivos aos quais o MSAHCI dá suporte.</span><span class="sxs-lookup"><span data-stu-id="500d2-110">There should be no change in functionality or performance; this driver supports all the same devices that MSAHCI supports.</span></span>

<span data-ttu-id="500d2-111">Essa alteração é transparente para o usuário.</span><span class="sxs-lookup"><span data-stu-id="500d2-111">This change is transparent to the user.</span></span>

## <a name="mitigation"></a><span data-ttu-id="500d2-112">Atenuação</span><span class="sxs-lookup"><span data-stu-id="500d2-112">Mitigation</span></span>

<span data-ttu-id="500d2-113">Atualize todos os utilitários e scripts que dependem de associações ATAport.</span><span class="sxs-lookup"><span data-stu-id="500d2-113">Update any utilities and scripts that rely on ATAport bindings.</span></span> <span data-ttu-id="500d2-114">Não confie no nome da unidade.</span><span class="sxs-lookup"><span data-stu-id="500d2-114">Do not rely on the drive name.</span></span> <span data-ttu-id="500d2-115">Em vez disso, use a detecção de disco padrão.</span><span class="sxs-lookup"><span data-stu-id="500d2-115">Instead use standard disk detection.</span></span>

 

 




