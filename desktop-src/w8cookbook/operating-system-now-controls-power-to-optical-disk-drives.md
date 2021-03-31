---
title: O sistema operacional agora controla a energia em unidades de disco ópticos
description: O sistema operacional agora controla a energia em unidades de disco ópticos
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aee28a7606f022c877077dbe5477ede959dbdb
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103641958"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a><span data-ttu-id="9f83d-103">O sistema operacional agora controla a energia em unidades de disco ópticos</span><span class="sxs-lookup"><span data-stu-id="9f83d-103">Operating system now controls power to optical disk drives</span></span>

## <a name="platforms"></a><span data-ttu-id="9f83d-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="9f83d-104">Platforms</span></span>

<span data-ttu-id="9f83d-105">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="9f83d-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="9f83d-106">**Servidores** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9f83d-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="9f83d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f83d-107">Description</span></span>

<span data-ttu-id="9f83d-108">Nas versões anteriores do Windows, a energia para a unidade óptica não era gerenciada quando a unidade óptica não estava em uso.</span><span class="sxs-lookup"><span data-stu-id="9f83d-108">In previous versions of Windows, power to the optical drive was not managed when the optical drive was not in use.</span></span> <span data-ttu-id="9f83d-109">Agora, se não houver nenhuma mídia presente na unidade de disco óptico (ímpar), o sistema operacional desligará a potência para a unidade óptica.</span><span class="sxs-lookup"><span data-stu-id="9f83d-109">Now, if there is no media present in the optical disk drive (ODD), the operating system turns off the power to the optical drive.</span></span> <span data-ttu-id="9f83d-110">Esse recurso é chamado de energia ímpar (ZPODD).</span><span class="sxs-lookup"><span data-stu-id="9f83d-110">This feature is called zero power ODD (ZPODD).</span></span> <span data-ttu-id="9f83d-111">O recurso é aplicável somente a unidades ópticas que usam um conector Slimline SATA (Serial Advanced Technology Attachment).</span><span class="sxs-lookup"><span data-stu-id="9f83d-111">The feature is applicable only to optical drives that use a Slimline SATA (Serial Advanced Technology Attachment) connector.</span></span>

## <a name="manifestation"></a><span data-ttu-id="9f83d-112">Manifestação</span><span class="sxs-lookup"><span data-stu-id="9f83d-112">Manifestation</span></span>

<span data-ttu-id="9f83d-113">Não encontramos nenhum impacto negativo desse novo comportamento; no entanto, você deve estar ciente dela, pois isso pode resultar em um comportamento inesperado do software de gravação de mídia.</span><span class="sxs-lookup"><span data-stu-id="9f83d-113">We have not found any negative impacts from this new behavior; however, you should be aware of it as it may result in unexpected behavior of media-writing software.</span></span>

## <a name="mitigation"></a><span data-ttu-id="9f83d-114">Atenuação</span><span class="sxs-lookup"><span data-stu-id="9f83d-114">Mitigation</span></span>

<span data-ttu-id="9f83d-115">Para reverter para o status do Always on, desative essa funcionalidade no registro.</span><span class="sxs-lookup"><span data-stu-id="9f83d-115">To revert to always-on status, turn off this functionality in the Registry.</span></span> <span data-ttu-id="9f83d-116">O caminho absoluto para o valor do registro é:</span><span class="sxs-lookup"><span data-stu-id="9f83d-116">The absolute path to the registry value is:</span></span>

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

<span data-ttu-id="9f83d-117">Seu tipo é DWORD (32 bits) e, se seu valor for 0, ZPODD será desabilitado; Se for qualquer outro valor, ZPODD será habilitado.</span><span class="sxs-lookup"><span data-stu-id="9f83d-117">Its type is DWORD (32 bit), and if its value is 0, then ZPODD is disabled; if it’s any other value, then ZPODD is enabled.</span></span>

## <a name="tests"></a><span data-ttu-id="9f83d-118">Testes</span><span class="sxs-lookup"><span data-stu-id="9f83d-118">Tests</span></span>

<span data-ttu-id="9f83d-119">Teste seu software de gravação de mídia para qualquer anomalia que ocorra devido a esse novo recurso.</span><span class="sxs-lookup"><span data-stu-id="9f83d-119">Test your media-writing software for any anomalies that occur due to this new feature.</span></span> <span data-ttu-id="9f83d-120">[Informe a Microsoft](mailto:OptIssue@microsoft.com) sobre os problemas encontrados com esse novo recurso.</span><span class="sxs-lookup"><span data-stu-id="9f83d-120">Please [inform Microsoft](mailto:OptIssue@microsoft.com) of any issues you find with this new feature.</span></span>

 

 




