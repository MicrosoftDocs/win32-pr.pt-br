---
title: Entrada de registro de tempo de execução
description: Entrada de registro de tempo de execução
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Windows Media Player, entradas de registro de tempo de execução
- Windows Media Player, extensões de nome de arquivo
- Windows Media Player, registro
- registro, extensões de nome de arquivo
- registro, entradas de tempo de execução
- registro, configurações do Windows Media Player
- configurações do registro de extensão de nome de arquivo
- entradas do registro em tempo de execução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01a83c3642f49a9fdbe7f8c51f157a154a9843b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005763"
---
# <a name="runtime-registry-entry"></a><span data-ttu-id="63cf0-111">Entrada de registro de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="63cf0-111">Runtime Registry Entry</span></span>

<span data-ttu-id="63cf0-112">Quando o Windows Media Player encontra uma extensão de nome de arquivo Personalizada, ele procura uma subchave do registro que corresponda à extensão.</span><span class="sxs-lookup"><span data-stu-id="63cf0-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="63cf0-113">A subchave é descrita em [configurações de registro de extensão de nome de arquivo](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="63cf0-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="63cf0-114">Uma das entradas do registro que podem aparecer na subchave da extensão é a entrada de **tempo de execução** .</span><span class="sxs-lookup"><span data-stu-id="63cf0-114">One of the registry entries that can appear under the extension's subkey is the **Runtime** entry.</span></span>

<span data-ttu-id="63cf0-115">A entrada de **tempo de execução** especifica a tecnologia subjacente que o Windows Media Player pode usar para reproduzir ou converter arquivos de mídia digital que têm a extensão personalizada.</span><span class="sxs-lookup"><span data-stu-id="63cf0-115">The **Runtime** entry specifies the underlying technology that Windows Media Player can use to play or convert digital media files that have the custom extension.</span></span> <span data-ttu-id="63cf0-116">A entrada de **tempo de execução** tem o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="63cf0-116">The **Runtime** entry has the following form.</span></span>



|          |                |                                                               |
|----------|----------------|---------------------------------------------------------------|
| <span data-ttu-id="63cf0-117">**Nome**</span><span class="sxs-lookup"><span data-stu-id="63cf0-117">**Name**</span></span> | <span data-ttu-id="63cf0-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="63cf0-118">**Type**</span></span>       | <span data-ttu-id="63cf0-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="63cf0-119">**Value**</span></span>                                                     |
| <span data-ttu-id="63cf0-120">Runtime</span><span class="sxs-lookup"><span data-stu-id="63cf0-120">Runtime</span></span>  | <span data-ttu-id="63cf0-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="63cf0-121">**REG\_DWORD**</span></span> | <span data-ttu-id="63cf0-122">Um inteiro positivo que identifica a tecnologia subjacente.</span><span class="sxs-lookup"><span data-stu-id="63cf0-122">A positive integer that identifies the underlying technology.</span></span> |



 

<span data-ttu-id="63cf0-123">O valor da entrada de **tempo de execução** deve ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="63cf0-123">The value of the **Runtime** entry must be one the following.</span></span>



| <span data-ttu-id="63cf0-124">**Valor (Decimal)**</span><span class="sxs-lookup"><span data-stu-id="63cf0-124">**Value (decimal)**</span></span> | <span data-ttu-id="63cf0-125">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="63cf0-125">**Description**</span></span>                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="63cf0-126">6</span><span class="sxs-lookup"><span data-stu-id="63cf0-126">6</span></span>                   | <span data-ttu-id="63cf0-127">Renderizar usando o Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="63cf0-127">Render using the Windows Media Format SDK.</span></span>                                                 |
| <span data-ttu-id="63cf0-128">7</span><span class="sxs-lookup"><span data-stu-id="63cf0-128">7</span></span>                   | <span data-ttu-id="63cf0-129">Renderizar usando o Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="63cf0-129">Render using Microsoft DirectShow.</span></span>                                                         |
| <span data-ttu-id="63cf0-130">13</span><span class="sxs-lookup"><span data-stu-id="63cf0-130">13</span></span>                  | <span data-ttu-id="63cf0-131">Converta o arquivo usando o plug-in de conversão especificado.</span><span class="sxs-lookup"><span data-stu-id="63cf0-131">Convert the file using the specified conversion plug-in.</span></span> <span data-ttu-id="63cf0-132">Requer o Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="63cf0-132">Requires Windows Media Player 11.</span></span> |



 

<span data-ttu-id="63cf0-133">Os valores de entrada do registro de **tempo de execução** 6 e 7 têm suporte do Windows Media Player 9 Series e posterior.</span><span class="sxs-lookup"><span data-stu-id="63cf0-133">The **Runtime** registry entry values 6 and 7 are supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="63cf0-134">O valor 13 é suportado pelo Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="63cf0-134">The value 13 is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63cf0-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63cf0-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63cf0-136">**Subchave ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="63cf0-136">**ConvertPluginCLSID Subkey**</span></span>](convertpluginclsid-subkey.md)
</dt> <dt>

[<span data-ttu-id="63cf0-137">**Configurações do registro de extensão de nome de arquivo**</span><span class="sxs-lookup"><span data-stu-id="63cf0-137">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




