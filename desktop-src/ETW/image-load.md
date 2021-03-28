---
description: Essa classe é a classe de tipo de evento para eventos de imagem. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 70ec0542-16d3-4186-a346-7f3c44dedf67
title: Classe Image_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_Load
- Image_Load.ImageBase
- Image_Load.ImageSize
- Image_Load.ProcessId
- Image_Load.ImageCheckSum
- Image_Load.TimeDateStamp
- Image_Load.Reserved0
- Image_Load.DefaultBase
- Image_Load.Reserved1
- Image_Load.Reserved2
- Image_Load.Reserved3
- Image_Load.Reserved4
- Image_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 647879b972c7cff2c086f656f76fa8decedb49a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505727"
---
# <a name="image_load-class"></a><span data-ttu-id="1817a-104">Classe de carregamento de imagem \_</span><span class="sxs-lookup"><span data-stu-id="1817a-104">Image\_Load class</span></span>

<span data-ttu-id="1817a-105">Essa classe é a classe de tipo de evento para eventos de imagem.</span><span class="sxs-lookup"><span data-stu-id="1817a-105">This class is the event type class for image events.</span></span>

<span data-ttu-id="1817a-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="1817a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1817a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1817a-107">Syntax</span></span>

``` syntax
[EventType(10, 2, 3, 4), EventTypeName("Load", "Unload", "DCStart", "DCEnd")]
class Image_Load : Image
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  uint32 ImageCheckSum;
  uint32 TimeDateStamp;
  uint32 Reserved0;
  uint32 DefaultBase;
  uint32 Reserved1;
  uint32 Reserved2;
  uint32 Reserved3;
  uint32 Reserved4;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="1817a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1817a-108">Members</span></span>

<span data-ttu-id="1817a-109">A classe de **\_ carregamento de imagem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1817a-109">The **Image\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="1817a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1817a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1817a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1817a-111">Properties</span></span>

<span data-ttu-id="1817a-112">A classe de **\_ carregamento de imagem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1817a-112">The **Image\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1817a-113">Defaultbase</span><span class="sxs-lookup"><span data-stu-id="1817a-113">DefaultBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1817a-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1817a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1817a-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1817a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1817a-116">Qualificadores: WmiDataId (7), ponteiro</span><span class="sxs-lookup"><span data-stu-id="1817a-116">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1817a-117">Endereço base padrão.</span><span class="sxs-lookup"><span data-stu-id="1817a-117">Default base address.</span></span>

</dd> <dt>

<span data-ttu-id="1817a-118">FileName</span><span class="sxs-lookup"><span data-stu-id="1817a-118">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1817a-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1817a-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1817a-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1817a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1817a-121">Qualificadores: WmiDataId (12), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="1817a-121">Qualifiers: WmiDataId(12), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="1817a-122">Nome do arquivo e extensão da imagem DLL ou executável.</span><span class="sxs-lookup"><span data-stu-id="1817a-122">File name and extension of the DLL or executable image.</span></span>

</dd> <dt>

<span data-ttu-id="1817a-123">ImageBase</span><span class="sxs-lookup"><span data-stu-id="1817a-123">ImageBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1817a-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1817a-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1817a-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1817a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1817a-126">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="1817a-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1817a-127">Endereço base do aplicativo no qual a imagem é carregada.</span><span class="sxs-lookup"><span data-stu-id="1817a-127">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="1817a-128">ImageCheckSum</span><span class="sxs-lookup"><span data-stu-id="1817a-128">ImageCheckSum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1817a-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1817a-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1817a-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1817a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1817a-131">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="1817a-131">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="1817a-132">Soma da verificação de imagem.</span><span class="sxs-lookup"><span data-stu-id="1817a-132">Image check sum.</span></span>

</dd> <dt>

<span data-ttu-id="1817a-133">ImageSize</span><span class="sxs-lookup"><span data-stu-id="1817a-133">ImageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1817a-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1817a-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1817a-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1817a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1817a-136">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="1817a-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1817a-137">Tamanho da imagem que está sendo carregada.</span><span class="sxs-lookup"><span data-stu-id="1817a-137">Size of the image being loaded.</span></span>

<span data-ttu-id="1817a-138">Ao consumir essa propriedade, o tipo de dados para essa propriedade é realmente o tamanho \_ t.</span><span class="sxs-lookup"><span data-stu-id="1817a-138">When consuming this property, the data type for this property is actually size\_t.</span></span> <span data-ttu-id="1817a-139">O qualificador de ponteiro é usado para determinar se o tamanho \_ t é de 4 bytes ou 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="1817a-139">The Pointer qualifier is used to determine if the size\_t is 4-bytes or 8-bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1817a-140">ProcessId</span><span class="sxs-lookup"><span data-stu-id="1817a-140">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1817a-141">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1817a-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1817a-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1817a-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1817a-143">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="1817a-143">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="1817a-144">Identifica o processo no qual a imagem é carregada.</span><span class="sxs-lookup"><span data-stu-id="1817a-144">Identifies the process into which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="1817a-145">Reserved0</span><span class="sxs-lookup"><span data-stu-id="1817a-145">Reserved0</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1817a-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1817a-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1817a-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1817a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1817a-148">Qualificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="1817a-148">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="1817a-149">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1817a-149">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="1817a-150">Reserved1</span><span class="sxs-lookup"><span data-stu-id="1817a-150">Reserved1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1817a-151">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1817a-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1817a-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1817a-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1817a-153">Qualificadores: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="1817a-153">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="1817a-154">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1817a-154">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="1817a-155">Reserved2</span><span class="sxs-lookup"><span data-stu-id="1817a-155">Reserved2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1817a-156">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1817a-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1817a-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1817a-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1817a-158">Qualificadores: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="1817a-158">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="1817a-159">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1817a-159">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="1817a-160">Reserved3</span><span class="sxs-lookup"><span data-stu-id="1817a-160">Reserved3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1817a-161">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1817a-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1817a-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1817a-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1817a-163">Qualificadores: WmiDataId (10)</span><span class="sxs-lookup"><span data-stu-id="1817a-163">Qualifiers: WmiDataId(10)</span></span>
</dt> </dl>

<span data-ttu-id="1817a-164">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1817a-164">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="1817a-165">Reserved4</span><span class="sxs-lookup"><span data-stu-id="1817a-165">Reserved4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1817a-166">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1817a-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1817a-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1817a-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1817a-168">Qualificadores: WmiDataId (11)</span><span class="sxs-lookup"><span data-stu-id="1817a-168">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="1817a-169">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1817a-169">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="1817a-170">TimeDateStamp</span><span class="sxs-lookup"><span data-stu-id="1817a-170">TimeDateStamp</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1817a-171">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1817a-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1817a-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1817a-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1817a-173">Qualificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="1817a-173">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="1817a-174">Hora e data em que a imagem foi carregada ou descarregada.</span><span class="sxs-lookup"><span data-stu-id="1817a-174">Time and date that the image was loaded or unloaded.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1817a-175">Comentários</span><span class="sxs-lookup"><span data-stu-id="1817a-175">Remarks</span></span>

<span data-ttu-id="1817a-176">Os eventos DCStart e DCEnd enumeram todas as imagens carregadas no início e no final do rastreamento, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1817a-176">The DCStart and DCEnd events enumerate all loaded images at the beginning and end of the trace, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="1817a-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1817a-177">Requirements</span></span>



| <span data-ttu-id="1817a-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="1817a-178">Requirement</span></span> | <span data-ttu-id="1817a-179">Valor</span><span class="sxs-lookup"><span data-stu-id="1817a-179">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1817a-180">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1817a-180">Minimum supported client</span></span><br/> | <span data-ttu-id="1817a-181">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1817a-181">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1817a-182">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1817a-182">Minimum supported server</span></span><br/> | <span data-ttu-id="1817a-183">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1817a-183">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1817a-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="1817a-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1817a-185">**Imagem**</span><span class="sxs-lookup"><span data-stu-id="1817a-185">**Image**</span></span>](image.md)
</dt> <dt>

[<span data-ttu-id="1817a-186">**V0 de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="1817a-186">**Image\_V0**</span></span>](image-v0.md)
</dt> <dt>

[<span data-ttu-id="1817a-187">**Imagem \_ v1**</span><span class="sxs-lookup"><span data-stu-id="1817a-187">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 




