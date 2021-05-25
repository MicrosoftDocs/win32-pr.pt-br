---
description: X opções de formato de arquivo, carregar e salvar.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e230fc08ac4d7f8713959f2025f67262046ecea5
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343641"
---
# <a name="d3dxf"></a><span data-ttu-id="dd792-103">D3DXF</span><span class="sxs-lookup"><span data-stu-id="dd792-103">D3DXF</span></span>

<span data-ttu-id="dd792-104">X opções de formato de arquivo, carregar e salvar.</span><span class="sxs-lookup"><span data-stu-id="dd792-104">X file format, load, and save options.</span></span>

## <a name="file-formats"></a><span data-ttu-id="dd792-105">Formatos de arquivo</span><span class="sxs-lookup"><span data-stu-id="dd792-105">File Formats</span></span>

<span data-ttu-id="dd792-106">A tabela a seguir especifica o tipo de dados de arquivo:</span><span class="sxs-lookup"><span data-stu-id="dd792-106">The following table specifies the type of file data:</span></span>



| <span data-ttu-id="dd792-107">\#define para o formato de arquivo</span><span class="sxs-lookup"><span data-stu-id="dd792-107">\#defines for File Format</span></span>     | <span data-ttu-id="dd792-108">Valor</span><span class="sxs-lookup"><span data-stu-id="dd792-108">Value</span></span> | <span data-ttu-id="dd792-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd792-109">Description</span></span>                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd792-110">\_Binário de FILEFORMATO D3DXF \_</span><span class="sxs-lookup"><span data-stu-id="dd792-110">D3DXF\_FILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="dd792-111">0</span><span class="sxs-lookup"><span data-stu-id="dd792-111">0</span></span>     | <span data-ttu-id="dd792-112">Arquivo binário de formato herdado.</span><span class="sxs-lookup"><span data-stu-id="dd792-112">Legacy-format binary file.</span></span> <span data-ttu-id="dd792-113">Consulte [referência de arquivo X (Herdado)](dx9-graphics-reference-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="dd792-113">See [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span> |
| <span data-ttu-id="dd792-114">Texto do D3DXF \_ FILEformat \_</span><span class="sxs-lookup"><span data-stu-id="dd792-114">D3DXF\_FILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="dd792-115">1</span><span class="sxs-lookup"><span data-stu-id="dd792-115">1</span></span>     | <span data-ttu-id="dd792-116">Arquivo de texto.</span><span class="sxs-lookup"><span data-stu-id="dd792-116">Text file.</span></span>                                                                                     |
| <span data-ttu-id="dd792-117">FORMATO de fileD3DXF \_ \_ compactado</span><span class="sxs-lookup"><span data-stu-id="dd792-117">D3DXF\_FILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="dd792-118">2</span><span class="sxs-lookup"><span data-stu-id="dd792-118">2</span></span>     | <span data-ttu-id="dd792-119">Arquivo compactado.</span><span class="sxs-lookup"><span data-stu-id="dd792-119">Compressed file.</span></span> <span data-ttu-id="dd792-120">Com esse sinalizador, você também deve especificar o formato binário ou o formato de texto.</span><span class="sxs-lookup"><span data-stu-id="dd792-120">With this flag, you must also specify the binary format or the text format.</span></span>   |



 

## <a name="file-load-options"></a><span data-ttu-id="dd792-121">Opções de carregamento de arquivo</span><span class="sxs-lookup"><span data-stu-id="dd792-121">File Load Options</span></span>

<span data-ttu-id="dd792-122">A tabela a seguir especifica opções de carregamento de arquivo com arquivos. x:</span><span class="sxs-lookup"><span data-stu-id="dd792-122">The following table specifies file load options with .x files:</span></span>



| <span data-ttu-id="dd792-123">\#definir</span><span class="sxs-lookup"><span data-stu-id="dd792-123">\#define</span></span>                      | <span data-ttu-id="dd792-124">Valor</span><span class="sxs-lookup"><span data-stu-id="dd792-124">Value</span></span> | <span data-ttu-id="dd792-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd792-125">Description</span></span>                |
|-------------------------------|-------|----------------------------|
| <span data-ttu-id="dd792-126">D3DXF \_ fileload \_ defile</span><span class="sxs-lookup"><span data-stu-id="dd792-126">D3DXF\_FILELOAD\_FromFile</span></span>     | <span data-ttu-id="dd792-127">0</span><span class="sxs-lookup"><span data-stu-id="dd792-127">0</span></span>     | <span data-ttu-id="dd792-128">Carregar dados de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="dd792-128">Load data from a file.</span></span>     |
| <span data-ttu-id="dd792-129">D3DXF \_ fileload \_ FROMWFILE</span><span class="sxs-lookup"><span data-stu-id="dd792-129">D3DXF\_FILELOAD\_FROMWFILE</span></span>    | <span data-ttu-id="dd792-130">1</span><span class="sxs-lookup"><span data-stu-id="dd792-130">1</span></span>     | <span data-ttu-id="dd792-131">Carregar dados de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="dd792-131">Load data from a file.</span></span>     |
| <span data-ttu-id="dd792-132">D3DXF \_ FILELOAD \_ FROMRESOURCE</span><span class="sxs-lookup"><span data-stu-id="dd792-132">D3DXF\_FILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="dd792-133">2</span><span class="sxs-lookup"><span data-stu-id="dd792-133">2</span></span>     | <span data-ttu-id="dd792-134">Carregar dados de um recurso.</span><span class="sxs-lookup"><span data-stu-id="dd792-134">Load data from a resource.</span></span> |
| <span data-ttu-id="dd792-135">D3DXF \_ FILELOAD \_ FROMMEMORY</span><span class="sxs-lookup"><span data-stu-id="dd792-135">D3DXF\_FILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="dd792-136">3</span><span class="sxs-lookup"><span data-stu-id="dd792-136">3</span></span>     | <span data-ttu-id="dd792-137">Carregar dados da memória.</span><span class="sxs-lookup"><span data-stu-id="dd792-137">Load data from memory.</span></span>     |



 

## <a name="file-save-options"></a><span data-ttu-id="dd792-138">Opções de salvar arquivo</span><span class="sxs-lookup"><span data-stu-id="dd792-138">File Save Options</span></span>

<span data-ttu-id="dd792-139">A tabela a seguir especifica opções de salvar e carregar arquivos com arquivos .x:</span><span class="sxs-lookup"><span data-stu-id="dd792-139">The following table specifies file save and load options with .x files:</span></span>



| <span data-ttu-id="dd792-140">\#Definir</span><span class="sxs-lookup"><span data-stu-id="dd792-140">\#define</span></span>                 | <span data-ttu-id="dd792-141">Valor</span><span class="sxs-lookup"><span data-stu-id="dd792-141">Value</span></span> | <span data-ttu-id="dd792-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd792-142">Description</span></span>                    |
|--------------------------|-------|--------------------------------|
| <span data-ttu-id="dd792-143">ARQUIVOS D3DXFAVE \_ \_ TOFILE</span><span class="sxs-lookup"><span data-stu-id="dd792-143">D3DXF\_FILESAVE\_TOFILE</span></span>  | <span data-ttu-id="dd792-144">0</span><span class="sxs-lookup"><span data-stu-id="dd792-144">0</span></span>     | <span data-ttu-id="dd792-145">Salve em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="dd792-145">Save to a file.</span></span>                |
| <span data-ttu-id="dd792-146">ARQUIVOS D3DXFAVE \_ \_ TOWFILE</span><span class="sxs-lookup"><span data-stu-id="dd792-146">D3DXF\_FILESAVE\_TOWFILE</span></span> | <span data-ttu-id="dd792-147">1</span><span class="sxs-lookup"><span data-stu-id="dd792-147">1</span></span>     | <span data-ttu-id="dd792-148">Salve em um arquivo de caractere largo.</span><span class="sxs-lookup"><span data-stu-id="dd792-148">Save to a wide-character file.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="dd792-149">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="dd792-149">Constant Information</span></span>



| <span data-ttu-id="dd792-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd792-150">Requirement</span></span>                         | <span data-ttu-id="dd792-151">Valor</span><span class="sxs-lookup"><span data-stu-id="dd792-151">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="dd792-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd792-152">Header</span></span>                   | <span data-ttu-id="dd792-153">d3dx9xof.h</span><span class="sxs-lookup"><span data-stu-id="dd792-153">d3dx9xof.h</span></span> |
| <span data-ttu-id="dd792-154">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="dd792-154">Minimum operating system</span></span> | <span data-ttu-id="dd792-155">Windows 98</span><span class="sxs-lookup"><span data-stu-id="dd792-155">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="dd792-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd792-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd792-157">Constantes de arquivo D3DX X</span><span class="sxs-lookup"><span data-stu-id="dd792-157">D3DX X File Constants</span></span>](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[<span data-ttu-id="dd792-158">**D3DXSaveMeshToX**</span><span class="sxs-lookup"><span data-stu-id="dd792-158">**D3DXSaveMeshToX**</span></span>](d3dxsavemeshtox.md)
</dt> </dl>

 

 



