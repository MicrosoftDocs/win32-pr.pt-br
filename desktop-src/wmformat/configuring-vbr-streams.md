---
title: Configurando fluxos de VBR
description: Configurando fluxos de VBR
ms.assetid: 83caabb7-b7fa-4b0a-a608-d5a86e4101b8
keywords:
- fluxos, configurando fluxos de VBR
- fluxos, taxa de bits variável (VBR)
- taxa de bits variável (VBR), fluxos
- VBR (taxa de bits variável), fluxos
- fluxos, interface IWMPropertyVault
- IWMPropertyVault
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6667dc9cf66932cf8af90da0b0e59ad27860ab3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916984"
---
# <a name="configuring-vbr-streams"></a><span data-ttu-id="734b0-109">Configurando fluxos de VBR</span><span class="sxs-lookup"><span data-stu-id="734b0-109">Configuring VBR Streams</span></span>

<span data-ttu-id="734b0-110">Você pode usar a codificação de taxa de bits variável (VBR) para produzir fluxos de alta qualidade para arquivos locais ou para download e reprodução.</span><span class="sxs-lookup"><span data-stu-id="734b0-110">You can use variable bit rate (VBR) encoding to produce high quality streams for local files or for downloading and playing.</span></span> <span data-ttu-id="734b0-111">Há três opções de VBR: baseada em qualidade (uma passagem), não restrita (duas passagens) e restrita (duas passagens)...</span><span class="sxs-lookup"><span data-stu-id="734b0-111">There are three options for VBR: quality-based (one-pass), unconstrained (two-pass), and constrained (two-pass).</span></span> <span data-ttu-id="734b0-112">Para obter mais informações sobre os tipos de codificação de VBR, consulte [codificação de taxa de bits variável (VBR)](variable-bit-rate--vbr--encoding.md).</span><span class="sxs-lookup"><span data-stu-id="734b0-112">For more information about the types of VBR encoding, see [Variable Bit Rate (VBR) Encoding](variable-bit-rate--vbr--encoding.md).</span></span>

<span data-ttu-id="734b0-113">Você pode configurar a codificação de VBR em um perfil definindo propriedades com a interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) .</span><span class="sxs-lookup"><span data-stu-id="734b0-113">You can configure VBR encoding in a profile by setting properties with the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface.</span></span> <span data-ttu-id="734b0-114">A tabela a seguir descreve as propriedades usadas para configurar a codificação de VBR.</span><span class="sxs-lookup"><span data-stu-id="734b0-114">The following table describes the properties used to configure VBR encoding.</span></span>



| <span data-ttu-id="734b0-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="734b0-115">Property</span></span>                     | <span data-ttu-id="734b0-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="734b0-116">Description</span></span>                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="734b0-117">**g \_ wszVBREnabled**</span><span class="sxs-lookup"><span data-stu-id="734b0-117">**g\_wszVBREnabled**</span></span>         | <span data-ttu-id="734b0-118">$True.</span><span class="sxs-lookup"><span data-stu-id="734b0-118">Boolean value.</span></span> <span data-ttu-id="734b0-119">Defina como true para usar a codificação de VBR.</span><span class="sxs-lookup"><span data-stu-id="734b0-119">Set to True to use VBR encoding.</span></span>                                                   |
| <span data-ttu-id="734b0-120">**g \_ wszVBRQuality**</span><span class="sxs-lookup"><span data-stu-id="734b0-120">**g\_wszVBRQuality**</span></span>         | <span data-ttu-id="734b0-121">Valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="734b0-121">**DWORD** value.</span></span> <span data-ttu-id="734b0-122">Defina para o nível de qualidade desejado (de 1 a 100) para a codificação de VBR com base na qualidade.</span><span class="sxs-lookup"><span data-stu-id="734b0-122">Set to the desired quality level (1 to 100) for quality-based VBR encoding.</span></span>      |
| <span data-ttu-id="734b0-123">**g \_ wszVBRBitrateMax**</span><span class="sxs-lookup"><span data-stu-id="734b0-123">**g\_wszVBRBitrateMax**</span></span>      | <span data-ttu-id="734b0-124">Valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="734b0-124">**DWORD** value.</span></span> <span data-ttu-id="734b0-125">Defina como a taxa de bits máxima, em bits por segundo, para a codificação de VBR restrita.</span><span class="sxs-lookup"><span data-stu-id="734b0-125">Set to the maximum bit rate, in bits per second, for constrained VBR encoding.</span></span>   |
| <span data-ttu-id="734b0-126">**g \_ wszVBRBufferWindowMax**</span><span class="sxs-lookup"><span data-stu-id="734b0-126">**g\_wszVBRBufferWindowMax**</span></span> | <span data-ttu-id="734b0-127">Valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="734b0-127">**DWORD** value.</span></span> <span data-ttu-id="734b0-128">Defina para a janela de buffer máximo, em milissegundos, para a codificação de VBR restrita.</span><span class="sxs-lookup"><span data-stu-id="734b0-128">Set to the maximum buffer window, in milliseconds, for constrained VBR encoding.</span></span> |



 

<span data-ttu-id="734b0-129">As seções a seguir descrevem como usar os diferentes tipos de codificação de taxa de bits variável.</span><span class="sxs-lookup"><span data-stu-id="734b0-129">The following sections describe how to use the different types of variable bit rate encoding.</span></span>



| <span data-ttu-id="734b0-130">Seção</span><span class="sxs-lookup"><span data-stu-id="734b0-130">Section</span></span>                                                              | <span data-ttu-id="734b0-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="734b0-131">Description</span></span>                                                                                                        |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="734b0-132">Para configurar Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="734b0-132">To Configure Quality-Based VBR</span></span>](to-configure-quality-based-vbr.md) | <span data-ttu-id="734b0-133">Descreve como usar a codificação de taxa de bits variável com base em um nível de qualidade estática.</span><span class="sxs-lookup"><span data-stu-id="734b0-133">Describes how to use variable bit rate encoding based on a static quality level.</span></span>                                   |
| [<span data-ttu-id="734b0-134">Para configurar a VBR não restringida</span><span class="sxs-lookup"><span data-stu-id="734b0-134">To Configure Unconstrained VBR</span></span>](to-configure-unconstrained-vbr.md) | <span data-ttu-id="734b0-135">Descreve como usar a codificação de taxa de bits variável com base em uma taxa de bits média de destino sem um valor de pico explícito.</span><span class="sxs-lookup"><span data-stu-id="734b0-135">Describes how to use variable bit rate encoding based on a target average bit rate without an explicit peak value.</span></span> |
| [<span data-ttu-id="734b0-136">Para configurar a VBR restrita</span><span class="sxs-lookup"><span data-stu-id="734b0-136">To Configure Constrained VBR</span></span>](to-configure-constrained-vbr.md)     | <span data-ttu-id="734b0-137">Descreve como usar a codificação de taxa de bits variável com base em uma taxa de bits média de destino e um valor de pico explícito.</span><span class="sxs-lookup"><span data-stu-id="734b0-137">Describes how to use variable bit rate encoding based on a target average bit rate and an explicit peak value.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="734b0-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="734b0-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="734b0-139">**Configurando fluxos**</span><span class="sxs-lookup"><span data-stu-id="734b0-139">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




