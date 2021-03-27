---
description: Essa classe é a classe de tipo de evento para eventos de carregamento de imagem. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 43bf0b2b-3ab4-4561-b48c-65fbace38a79
title: Classe Image_V1_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V1_Load
- Image_V1_Load.ImageBase
- Image_V1_Load.ImageSize
- Image_V1_Load.ProcessId
- Image_V1_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd0a2a61b263ce78c2cf28cdf1cd5df4b702140d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967292"
---
# <a name="image_v1_load-class"></a><span data-ttu-id="b79d0-104">\_Classe de \_ carga Image v1</span><span class="sxs-lookup"><span data-stu-id="b79d0-104">Image\_V1\_Load class</span></span>

<span data-ttu-id="b79d0-105">Essa classe é a classe de tipo de evento para eventos de carregamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="b79d0-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="b79d0-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="b79d0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b79d0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b79d0-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V1_Load : Image_V1
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="b79d0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b79d0-108">Members</span></span>

<span data-ttu-id="b79d0-109">A classe de **\_ \_ carga Image v1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b79d0-109">The **Image\_V1\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="b79d0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b79d0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b79d0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b79d0-111">Properties</span></span>

<span data-ttu-id="b79d0-112">A classe de **\_ \_ carga Image v1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b79d0-112">The **Image\_V1\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b79d0-113">FileName</span><span class="sxs-lookup"><span data-stu-id="b79d0-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b79d0-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b79d0-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b79d0-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b79d0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b79d0-116">Qualificadores: WmiDataId (4), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="b79d0-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="b79d0-117">Nome do arquivo e extensão da imagem DLL ou executável a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="b79d0-117">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="b79d0-118">ImageBase</span><span class="sxs-lookup"><span data-stu-id="b79d0-118">ImageBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b79d0-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b79d0-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b79d0-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b79d0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b79d0-121">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="b79d0-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b79d0-122">Endereço base do aplicativo no qual a imagem é carregada.</span><span class="sxs-lookup"><span data-stu-id="b79d0-122">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="b79d0-123">ImageSize</span><span class="sxs-lookup"><span data-stu-id="b79d0-123">ImageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b79d0-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b79d0-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b79d0-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b79d0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b79d0-126">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="b79d0-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b79d0-127">Tamanho da imagem que está sendo carregada.</span><span class="sxs-lookup"><span data-stu-id="b79d0-127">Size of the image being loaded.</span></span>

<span data-ttu-id="b79d0-128">Ao consumir essa propriedade, o tipo de dados para essa propriedade é realmente o tamanho \_ t.</span><span class="sxs-lookup"><span data-stu-id="b79d0-128">When consuming this property, the data type for this property is actually size\_t.</span></span> <span data-ttu-id="b79d0-129">O qualificador de ponteiro é usado para determinar se o tamanho \_ t é de 4 bytes ou 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="b79d0-129">The Pointer qualifier is used to determine if the size\_t is 4-bytes or 8-bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b79d0-130">ProcessId</span><span class="sxs-lookup"><span data-stu-id="b79d0-130">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b79d0-131">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b79d0-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b79d0-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b79d0-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b79d0-133">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="b79d0-133">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="b79d0-134">Identifica o processo no qual a imagem é carregada.</span><span class="sxs-lookup"><span data-stu-id="b79d0-134">Identifies the process into which the image is loaded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b79d0-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b79d0-135">Requirements</span></span>



| <span data-ttu-id="b79d0-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b79d0-136">Requirement</span></span> | <span data-ttu-id="b79d0-137">Valor</span><span class="sxs-lookup"><span data-stu-id="b79d0-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b79d0-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b79d0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b79d0-139">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b79d0-139">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b79d0-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b79d0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b79d0-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b79d0-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b79d0-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="b79d0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b79d0-143">**Imagem \_ v1**</span><span class="sxs-lookup"><span data-stu-id="b79d0-143">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 




