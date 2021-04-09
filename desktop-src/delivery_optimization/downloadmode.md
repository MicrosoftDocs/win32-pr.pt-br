---
title: Enumeração de downloadmode (Deliveryoptimization. h)
description: Define os diferentes modos de download que a otimização de entrega usa.
ms.assetid: 7E9407C6-A22F-459E-B316-5E7809F0067A
keywords:
- Ignore a Otimização de Entrega e use o BITS. Por exemplo, selecione esse modo para que os clientes possam usar o BranchCache. enumeração
topic_type:
- apiref
api_name:
- DownloadMode
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0cde44a3d211040e2cc1dd62afd54f8284f5493e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009286"
---
# <a name="downloadmode-enumeration"></a><span data-ttu-id="7dcf9-106">Enumeração de downloadmode</span><span class="sxs-lookup"><span data-stu-id="7dcf9-106">DownloadMode enumeration</span></span>

<span data-ttu-id="7dcf9-107">Define os diferentes modos de download que a otimização de entrega usa.</span><span class="sxs-lookup"><span data-stu-id="7dcf9-107">Defines the different download modes that Delivery Optimization uses.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dcf9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7dcf9-108">Syntax</span></span>


```C++
typedef enum _DownloadMode { 
  DownloadMode_CdnOnly   = 0,
  DownloadMode_Lan       = 1,
  DownloadMode_Group     = 2,
  DownloadMode_Internet  = 3,
  DownloadMode_Simple    = 99,
  DownloadMode_Bypass    = 100
} DownloadMode;
```



## <a name="constants"></a><span data-ttu-id="7dcf9-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="7dcf9-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7dcf9-110"><span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**</span><span class="sxs-lookup"><span data-stu-id="7dcf9-110"><span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**</span></span>
</dt> <dd>

<span data-ttu-id="7dcf9-111">Essa configuração desabilita o cache ponto a ponto, mas ainda permite que a otimização de entrega Baixe conteúdo de servidores da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7dcf9-111">This setting disables peer-to-peer caching but still allows Delivery Optimization to download content from Microsoft servers.</span></span> <span data-ttu-id="7dcf9-112">Esse modo usa metadados adicionais fornecidos pelos serviços de nuvem da Otimização de Entrega para oferecer uma experiência de download poderosa, confiável e eficientes.</span><span class="sxs-lookup"><span data-stu-id="7dcf9-112">This mode uses additional metadata provided by the Delivery Optimization cloud services for a peerless reliable and efficient download experience.</span></span>

</dd> <dt>

<span data-ttu-id="7dcf9-113"><span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**</span><span class="sxs-lookup"><span data-stu-id="7dcf9-113"><span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**</span></span>
</dt> <dd>

<span data-ttu-id="7dcf9-114">Esse modo de operação padrão para Otimização de Entrega permite que o compartilhamento ponto a ponto na mesma rede.</span><span class="sxs-lookup"><span data-stu-id="7dcf9-114">This default operating mode for Delivery Optimization enables peer sharing on the same network.</span></span>

</dd> <dt>

<span data-ttu-id="7dcf9-115"><span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**</span><span class="sxs-lookup"><span data-stu-id="7dcf9-115"><span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**</span></span>
</dt> <dd>

<span data-ttu-id="7dcf9-116">Quando o modo de grupo é definido, o grupo é selecionado automaticamente com base no site do Active Directory Domain Services do dispositivo (AD DS) (Windows 10, versão 1607) ou no domínio no qual o dispositivo é autenticado (Windows 10, versão 1511).</span><span class="sxs-lookup"><span data-stu-id="7dcf9-116">When group mode is set, the group is automatically selected based on the device s Active Directory Domain Services (AD DS) site (Windows 10, version 1607) or the domain the device is authenticated to (Windows 10, version 1511).</span></span> <span data-ttu-id="7dcf9-117">No modo de grupo, o emparelhamento ocorre em sub-redes internas, entre dispositivos que pertencem ao mesmo grupo, incluindo dispositivos em escritórios remotos.</span><span class="sxs-lookup"><span data-stu-id="7dcf9-117">In group mode, peering occurs across internal subnets, between devices that belong to the same group, including devices in remote offices.</span></span> <span data-ttu-id="7dcf9-118">Você pode usar a opção GroupID para criar seu próprio grupo personalizado independentemente domínios e sites do AD DS.</span><span class="sxs-lookup"><span data-stu-id="7dcf9-118">You can use the GroupID option to create your own custom group independently of domains and AD DS sites.</span></span> <span data-ttu-id="7dcf9-119">O modo de download de grupo é a opção recomendada para a maioria das organizações que desejam obter a melhor otimização de largura de banda com a Otimização de Entrega.</span><span class="sxs-lookup"><span data-stu-id="7dcf9-119">Group download mode is the recommended option for most organizations looking to achieve the best bandwidth optimization with Delivery Optimization.</span></span>

</dd> <dt>

<span data-ttu-id="7dcf9-120"><span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**</span><span class="sxs-lookup"><span data-stu-id="7dcf9-120"><span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**</span></span>
</dt> <dd>

<span data-ttu-id="7dcf9-121">Habilite fontes de emparelhamento da Internet para Otimização de Entrega.</span><span class="sxs-lookup"><span data-stu-id="7dcf9-121">Enable Internet peer sources for Delivery Optimization.</span></span>

</dd> <dt>

<span data-ttu-id="7dcf9-122"><span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**</span><span class="sxs-lookup"><span data-stu-id="7dcf9-122"><span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**</span></span>
</dt> <dd>

<span data-ttu-id="7dcf9-123">O modo Simples desabilita o uso dos serviços de nuvem de Otimização de Entrega completamente (para ambientes offline).</span><span class="sxs-lookup"><span data-stu-id="7dcf9-123">Simple mode disables the use of Delivery Optimization cloud services completely (for offline environments).</span></span> <span data-ttu-id="7dcf9-124">A Otimização de Entrega alterna para esse modo automaticamente quando os serviços de nuvem de Otimização de Entrega não estão disponíveis ou acessíveis ou quando o tamanho do arquivo de conteúdo é menor que 10 MB.</span><span class="sxs-lookup"><span data-stu-id="7dcf9-124">Delivery Optimization switches to this mode automatically when the Delivery Optimization cloud services are unavailable, unreachable or when the content file size is less than 10 MB.</span></span> <span data-ttu-id="7dcf9-125">Nesse modo, a Otimização de Entrega fornece uma experiência de download confiável, sem cache ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="7dcf9-125">In this mode, Delivery Optimization provides a reliable download experience, with no peer-to-peer caching.</span></span>

</dd> <dt>

<span data-ttu-id="7dcf9-126"><span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**</span><span class="sxs-lookup"><span data-stu-id="7dcf9-126"><span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**</span></span>
</dt> <dd>

<span data-ttu-id="7dcf9-127">Ignore a Otimização de Entrega e use o BITS.</span><span class="sxs-lookup"><span data-stu-id="7dcf9-127">Bypass Delivery Optimization and use BITS, instead.</span></span> <span data-ttu-id="7dcf9-128">Por exemplo, selecione esse modo para que os clientes possam usar o BranchCache.</span><span class="sxs-lookup"><span data-stu-id="7dcf9-128">For example, select this mode so that clients can use BranchCache.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7dcf9-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7dcf9-129">Requirements</span></span>

| <span data-ttu-id="7dcf9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dcf9-130">Requirement</span></span> | <span data-ttu-id="7dcf9-131">Valor</span><span class="sxs-lookup"><span data-stu-id="7dcf9-131">Value</span></span> |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="7dcf9-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7dcf9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7dcf9-133">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="7dcf9-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="7dcf9-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7dcf9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7dcf9-135">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="7dcf9-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>  |
| <span data-ttu-id="7dcf9-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7dcf9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dcf9-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dcf9-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>               |
