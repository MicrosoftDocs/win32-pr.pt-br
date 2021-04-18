---
description: Especifica uma lista de comandos de script e os parâmetros para um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao objeto de comando de script no cabeçalho ASF, definido na especificação ASF.
ms.assetid: c85c9da4-f0b5-4055-a645-2a71cabbe4a3
title: Atributo MF_PD_ASF_SCRIPT (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03de86298d28183aa57cc80b451c4e46bb054de2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798271"
---
# <a name="mf_pd_asf_script-attribute"></a><span data-ttu-id="fe894-104">\_Atributo de script MF PD \_ ASF \_</span><span class="sxs-lookup"><span data-stu-id="fe894-104">MF\_PD\_ASF\_SCRIPT attribute</span></span>

<span data-ttu-id="fe894-105">Especifica uma lista de comandos de script e os parâmetros para um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="fe894-105">Specifies a list of script commands and the parameters for an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="fe894-106">Esse atributo corresponde ao objeto de comando de script no cabeçalho ASF, definido na especificação ASF.</span><span class="sxs-lookup"><span data-stu-id="fe894-106">This attribute corresponds to the Script Command Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="fe894-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fe894-107">Data type</span></span>

<span data-ttu-id="fe894-108">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="fe894-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="fe894-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe894-109">Remarks</span></span>

<span data-ttu-id="fe894-110">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="fe894-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="fe894-111">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) cria o descritor de apresentação e gera esse atributo a partir do cabeçalho de objeto de comando de script.</span><span class="sxs-lookup"><span data-stu-id="fe894-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Script Command Object header.</span></span> <span data-ttu-id="fe894-112">A tabela a seguir mostra o formato do blob:</span><span class="sxs-lookup"><span data-stu-id="fe894-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="fe894-113">Campo de objeto de comando de script</span><span class="sxs-lookup"><span data-stu-id="fe894-113">Script Command Object field</span></span> | <span data-ttu-id="fe894-114">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fe894-114">Data type</span></span>    | <span data-ttu-id="fe894-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="fe894-115">Size</span></span>    | <span data-ttu-id="fe894-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe894-116">Description</span></span>               |
|-----------------------------|--------------|---------|---------------------------|
| <span data-ttu-id="fe894-117">Contagem de comandos</span><span class="sxs-lookup"><span data-stu-id="fe894-117">Commands Count</span></span>              | <span data-ttu-id="fe894-118">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fe894-118">**DWORD**</span></span>    | <span data-ttu-id="fe894-119">4 bytes</span><span class="sxs-lookup"><span data-stu-id="fe894-119">4 bytes</span></span> | <span data-ttu-id="fe894-120">Número de comandos de script</span><span class="sxs-lookup"><span data-stu-id="fe894-120">Number of script commands</span></span> |
| <span data-ttu-id="fe894-121">Tipo de comando, comandos</span><span class="sxs-lookup"><span data-stu-id="fe894-121">Command Type, Commands</span></span>      | <span data-ttu-id="fe894-122">**MINUCIOSA**\[\]</span><span class="sxs-lookup"><span data-stu-id="fe894-122">**BYTE**\[\]</span></span> | <span data-ttu-id="fe894-123">Varia</span><span class="sxs-lookup"><span data-stu-id="fe894-123">Varies</span></span>  | <span data-ttu-id="fe894-124">Matriz de comandos de script</span><span class="sxs-lookup"><span data-stu-id="fe894-124">Array of script commands</span></span>  |



 

<span data-ttu-id="fe894-125">O primeiro **DWORD** é o número de comandos de script, seguidos por uma matriz de comandos.</span><span class="sxs-lookup"><span data-stu-id="fe894-125">The first **DWORD** is the number of script commands, followed by an array of commands.</span></span> <span data-ttu-id="fe894-126">Cada comando de script tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="fe894-126">Each script command has the following format:</span></span>



| <span data-ttu-id="fe894-127">Campo de objeto de comando de script</span><span class="sxs-lookup"><span data-stu-id="fe894-127">Script Command Object field</span></span> | <span data-ttu-id="fe894-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fe894-128">Data type</span></span>     | <span data-ttu-id="fe894-129">Tamanho</span><span class="sxs-lookup"><span data-stu-id="fe894-129">Size</span></span>    | <span data-ttu-id="fe894-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe894-130">Description</span></span>                                                              |
|-----------------------------|---------------|---------|--------------------------------------------------------------------------|
| <span data-ttu-id="fe894-131">Comprimento do nome do comando</span><span class="sxs-lookup"><span data-stu-id="fe894-131">Command Name Length</span></span>         | <span data-ttu-id="fe894-132">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fe894-132">**DWORD**</span></span>     | <span data-ttu-id="fe894-133">4 bytes</span><span class="sxs-lookup"><span data-stu-id="fe894-133">4 bytes</span></span> | <span data-ttu-id="fe894-134">Tamanho da cadeia de caracteres do comando, em bytes, incluindo o caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="fe894-134">Size of the command string, in bytes, including the NULL character.</span></span>      |
| <span data-ttu-id="fe894-135">Nome do comando</span><span class="sxs-lookup"><span data-stu-id="fe894-135">Command Name</span></span>                | <span data-ttu-id="fe894-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="fe894-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="fe894-137">Varia</span><span class="sxs-lookup"><span data-stu-id="fe894-137">Varies</span></span>  | <span data-ttu-id="fe894-138">Cadeia de caracteres terminada em nulo que contém o comando de script.</span><span class="sxs-lookup"><span data-stu-id="fe894-138">Null-terminated string that contains the script command.</span></span>                 |
| <span data-ttu-id="fe894-139">Comprimento do nome do tipo de comando</span><span class="sxs-lookup"><span data-stu-id="fe894-139">Command Type Name Length</span></span>    | <span data-ttu-id="fe894-140">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fe894-140">**DWORD**</span></span>     | <span data-ttu-id="fe894-141">4 bytes</span><span class="sxs-lookup"><span data-stu-id="fe894-141">4 bytes</span></span> | <span data-ttu-id="fe894-142">Tamanho da cadeia de caracteres do tipo de comando, em bytes, incluindo o caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="fe894-142">Size of the command type string, in bytes, including the NULL character.</span></span> |
| <span data-ttu-id="fe894-143">Nome do tipo de comando</span><span class="sxs-lookup"><span data-stu-id="fe894-143">Command Type Name</span></span>           | <span data-ttu-id="fe894-144">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="fe894-144">**WCHAR**\[\]</span></span> | <span data-ttu-id="fe894-145">Varia</span><span class="sxs-lookup"><span data-stu-id="fe894-145">Varies</span></span>  | <span data-ttu-id="fe894-146">Cadeia de caracteres terminada em nulo que contém o tipo de comando.</span><span class="sxs-lookup"><span data-stu-id="fe894-146">Null-terminated string that contains the command type.</span></span>                   |
| <span data-ttu-id="fe894-147">Tempo da apresentação</span><span class="sxs-lookup"><span data-stu-id="fe894-147">Presentation Time</span></span>           | <span data-ttu-id="fe894-148">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="fe894-148">**DWORD**</span></span>     | <span data-ttu-id="fe894-149">4 bytes</span><span class="sxs-lookup"><span data-stu-id="fe894-149">4 bytes</span></span> | <span data-ttu-id="fe894-150">Hora da apresentação do comando em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="fe894-150">Presentation time of the command in milliseconds.</span></span>                        |



 

## <a name="requirements"></a><span data-ttu-id="fe894-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe894-151">Requirements</span></span>



| <span data-ttu-id="fe894-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe894-152">Requirement</span></span> | <span data-ttu-id="fe894-153">Valor</span><span class="sxs-lookup"><span data-stu-id="fe894-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe894-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe894-154">Minimum supported client</span></span><br/> | <span data-ttu-id="fe894-155">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe894-155">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fe894-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe894-156">Minimum supported server</span></span><br/> | <span data-ttu-id="fe894-157">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe894-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fe894-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe894-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe894-159"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe894-159"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe894-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe894-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe894-161">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fe894-161">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fe894-162">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="fe894-162">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="fe894-163">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="fe894-163">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="fe894-164">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fe894-164">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="fe894-165">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="fe894-165">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="fe894-166">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="fe894-166">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="fe894-167">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="fe894-167">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




