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
ms.openlocfilehash: 3bf485038965184add320e49c29482672c770f48
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424105"
---
# <a name="runtime-registry-entry"></a><span data-ttu-id="cbb4c-111">Entrada de registro de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="cbb4c-111">Runtime Registry Entry</span></span>

<span data-ttu-id="cbb4c-112">Quando o Windows Media Player encontra uma extensão de nome de arquivo Personalizada, ele procura uma subchave do registro que corresponda à extensão.</span><span class="sxs-lookup"><span data-stu-id="cbb4c-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="cbb4c-113">A subchave é descrita em [configurações de registro de extensão de nome de arquivo](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="cbb4c-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="cbb4c-114">Uma das entradas do registro que podem aparecer na subchave da extensão é a entrada de **tempo de execução** .</span><span class="sxs-lookup"><span data-stu-id="cbb4c-114">One of the registry entries that can appear under the extension's subkey is the **Runtime** entry.</span></span>

<span data-ttu-id="cbb4c-115">A entrada de **tempo de execução** especifica a tecnologia subjacente que o Windows Media Player pode usar para reproduzir ou converter arquivos de mídia digital que têm a extensão personalizada.</span><span class="sxs-lookup"><span data-stu-id="cbb4c-115">The **Runtime** entry specifies the underlying technology that Windows Media Player can use to play or convert digital media files that have the custom extension.</span></span> <span data-ttu-id="cbb4c-116">A entrada de **tempo de execução** tem o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="cbb4c-116">The **Runtime** entry has the following form.</span></span>



|   <span data-ttu-id="cbb4c-117">Nome</span><span class="sxs-lookup"><span data-stu-id="cbb4c-117">Name</span></span>   |   <span data-ttu-id="cbb4c-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb4c-118">Type</span></span>         |   <span data-ttu-id="cbb4c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cbb4c-119">Value</span></span>                                                       |
|----------|----------------|---------------------------------------------------------------|
| <span data-ttu-id="cbb4c-120">Runtime</span><span class="sxs-lookup"><span data-stu-id="cbb4c-120">Runtime</span></span>  | <span data-ttu-id="cbb4c-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="cbb4c-121">**REG\_DWORD**</span></span> | <span data-ttu-id="cbb4c-122">Um inteiro positivo que identifica a tecnologia subjacente.</span><span class="sxs-lookup"><span data-stu-id="cbb4c-122">A positive integer that identifies the underlying technology.</span></span> |



 

<span data-ttu-id="cbb4c-123">O valor da entrada de **tempo de execução** deve ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="cbb4c-123">The value of the **Runtime** entry must be one the following.</span></span>



| <span data-ttu-id="cbb4c-124">**Valor (Decimal)**</span><span class="sxs-lookup"><span data-stu-id="cbb4c-124">**Value (decimal)**</span></span> | <span data-ttu-id="cbb4c-125">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cbb4c-125">**Description**</span></span>                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb4c-126">6</span><span class="sxs-lookup"><span data-stu-id="cbb4c-126">6</span></span>                   | <span data-ttu-id="cbb4c-127">Renderizar usando o Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="cbb4c-127">Render using the Windows Media Format SDK.</span></span>                                                 |
| <span data-ttu-id="cbb4c-128">7</span><span class="sxs-lookup"><span data-stu-id="cbb4c-128">7</span></span>                   | <span data-ttu-id="cbb4c-129">Renderizar usando o Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cbb4c-129">Render using Microsoft DirectShow.</span></span>                                                         |
| <span data-ttu-id="cbb4c-130">13</span><span class="sxs-lookup"><span data-stu-id="cbb4c-130">13</span></span>                  | <span data-ttu-id="cbb4c-131">Converta o arquivo usando o plug-in de conversão especificado.</span><span class="sxs-lookup"><span data-stu-id="cbb4c-131">Convert the file using the specified conversion plug-in.</span></span> <span data-ttu-id="cbb4c-132">Requer Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="cbb4c-132">Requires Windows Media Player 11.</span></span> |



 

<span data-ttu-id="cbb4c-133">Os valores de entrada do Registro de **Runtime** 6 e 7 têm suporte Windows Media Player Série 9 e posteriores.</span><span class="sxs-lookup"><span data-stu-id="cbb4c-133">The **Runtime** registry entry values 6 and 7 are supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="cbb4c-134">O valor 13 é suportado pelo Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="cbb4c-134">The value 13 is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbb4c-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cbb4c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbb4c-136">**ConvertPluginCLSID Subkey**</span><span class="sxs-lookup"><span data-stu-id="cbb4c-136">**ConvertPluginCLSID Subkey**</span></span>](convertpluginclsid-subkey.md)
</dt> <dt>

[<span data-ttu-id="cbb4c-137">**Configurações do Registro de Extensão de Nome de Arquivo**</span><span class="sxs-lookup"><span data-stu-id="cbb4c-137">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




