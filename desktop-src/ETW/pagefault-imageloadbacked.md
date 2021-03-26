---
description: Essa classe é a classe de tipo de evento para carregamento de imagem em eventos de arquivo de paginação. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 7d2f08e8-ec1f-4630-922a-548b55eadfda
title: Classe PageFault_ImageLoadBacked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_ImageLoadBacked
- PageFault_ImageLoadBacked.FileObject
- PageFault_ImageLoadBacked.DeviceChar
- PageFault_ImageLoadBacked.FileChar
- PageFault_ImageLoadBacked.LoadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1644db74c5c7c361acda796219ae1415ecc262bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968034"
---
# <a name="pagefault_imageloadbacked-class"></a><span data-ttu-id="4db92-104">\_Classe falhadepágina ImageLoadBacked</span><span class="sxs-lookup"><span data-stu-id="4db92-104">PageFault\_ImageLoadBacked class</span></span>

<span data-ttu-id="4db92-105">Essa classe é a classe de tipo de evento para carregamento de imagem em eventos de arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="4db92-105">This class is the event type class for image load in page file events.</span></span>

<span data-ttu-id="4db92-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="4db92-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4db92-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4db92-107">Syntax</span></span>

``` syntax
[EventType{105}, EventTypeName{"ImageLoadBacked"}]
class PageFault_ImageLoadBacked : PageFault_V2
{
  uint32 FileObject;
  uint32 DeviceChar;
  uint16 FileChar;
  uint16 LoadFlags;
};
```

## <a name="members"></a><span data-ttu-id="4db92-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4db92-108">Members</span></span>

<span data-ttu-id="4db92-109">A classe **falhadepágina \_ ImageLoadBacked** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4db92-109">The **PageFault\_ImageLoadBacked** class has these types of members:</span></span>

-   [<span data-ttu-id="4db92-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4db92-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4db92-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4db92-111">Properties</span></span>

<span data-ttu-id="4db92-112">A classe **falhadepágina \_ ImageLoadBacked** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4db92-112">The **PageFault\_ImageLoadBacked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4db92-113">**DeviceChar**</span><span class="sxs-lookup"><span data-stu-id="4db92-113">**DeviceChar**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db92-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4db92-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4db92-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4db92-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db92-116">Qualificadores: WmiDataId (2), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="4db92-116">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="4db92-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4db92-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="4db92-118">**Filechar**</span><span class="sxs-lookup"><span data-stu-id="4db92-118">**FileChar**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db92-119">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4db92-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4db92-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4db92-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db92-121">Qualificadores: WmiDataId (3), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="4db92-121">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="4db92-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4db92-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="4db92-123">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="4db92-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db92-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4db92-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4db92-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4db92-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db92-126">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="4db92-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4db92-127">Corresponda o valor desse ponteiro ao valor do ponteiro **FileObject** em um evento [**de \_ nome de FileIo**](fileio-name.md) para determinar o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="4db92-127">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="4db92-128">**Sinalizadores de**</span><span class="sxs-lookup"><span data-stu-id="4db92-128">**LoadFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4db92-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4db92-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4db92-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4db92-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4db92-131">Qualificadores: WmiDataId (4), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="4db92-131">Qualifiers: WmiDataId(4), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="4db92-132">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4db92-132">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4db92-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="4db92-133">Remarks</span></span>

<span data-ttu-id="4db92-134">O evento é registrado durante uma criação de seção de imagem (por exemplo, uma carga de DLL) quando o Gerenciador de memória determina que a imagem precisa ser copiada e executada a partir do arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="4db92-134">The event is logged during an image section creation (for example, a DLL load) when the memory manager determines that the image needs to be copied into and run from the page file.</span></span> <span data-ttu-id="4db92-135">Normalmente, as imagens são executadas a partir do arquivo de origem, mas o backup de paginação pode ocorrer quando o Gerenciador de memória determina que o arquivo de origem pode ser modificado de forma assíncrona por gravadores existentes ou quando o arquivo de origem está em uma mídia removível ou em um dispositivo remoto.</span><span class="sxs-lookup"><span data-stu-id="4db92-135">Typically, images are run from the source file but pagefile-backing can occur when the memory manager determines that the source file may be modified asynchronously by existing writers or when the source file is on a removable media or a remote device.</span></span>

## <a name="requirements"></a><span data-ttu-id="4db92-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4db92-136">Requirements</span></span>



| <span data-ttu-id="4db92-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="4db92-137">Requirement</span></span> | <span data-ttu-id="4db92-138">Valor</span><span class="sxs-lookup"><span data-stu-id="4db92-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4db92-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4db92-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4db92-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4db92-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4db92-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4db92-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4db92-142">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4db92-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4db92-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="4db92-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db92-144">**Falhadepágina \_ v2**</span><span class="sxs-lookup"><span data-stu-id="4db92-144">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




