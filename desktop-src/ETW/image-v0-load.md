---
description: Classe Image_V0_Load-essa classe é a classe de tipo de evento para eventos de carregamento de imagem. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: e2836153-8e4f-4c7f-9542-9402ed9e4356
title: Classe Image_V0_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V0_Load
- Image_V0_Load.BaseAddress
- Image_V0_Load.ModuleSize
- Image_V0_Load.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: ed15254ac509334c802ba4c6165c73e681a2c7b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106504"
---
# <a name="image_v0_load-class"></a><span data-ttu-id="6f2db-104">\_Classe de carregamento V0 de imagem \_</span><span class="sxs-lookup"><span data-stu-id="6f2db-104">Image\_V0\_Load class</span></span>

<span data-ttu-id="6f2db-105">Essa classe é a classe de tipo de evento para eventos de carregamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="6f2db-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="6f2db-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="6f2db-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f2db-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f2db-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="6f2db-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6f2db-108">Members</span></span>

<span data-ttu-id="6f2db-109">A classe de **\_ \_ carga V0 de imagem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6f2db-109">The **Image\_V0\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="6f2db-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f2db-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f2db-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f2db-111">Properties</span></span>

<span data-ttu-id="6f2db-112">A classe de **\_ \_ carregamento V0 de imagem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6f2db-112">The **Image\_V0\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f2db-113">BaseAddress</span><span class="sxs-lookup"><span data-stu-id="6f2db-113">BaseAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f2db-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f2db-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f2db-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f2db-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f2db-116">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="6f2db-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6f2db-117">Endereço base do aplicativo no qual a imagem é carregada.</span><span class="sxs-lookup"><span data-stu-id="6f2db-117">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="6f2db-118">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="6f2db-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f2db-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f2db-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f2db-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f2db-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f2db-121">Qualificadores: WmiDataId (3), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="6f2db-121">Qualifiers: WmiDataId(3), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="6f2db-122">Nome do arquivo e extensão da imagem DLL ou executável a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="6f2db-122">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="6f2db-123">Módulosize</span><span class="sxs-lookup"><span data-stu-id="6f2db-123">ModuleSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f2db-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f2db-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f2db-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f2db-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f2db-126">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="6f2db-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="6f2db-127">Tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="6f2db-127">Size of the image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f2db-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f2db-128">Requirements</span></span>



| <span data-ttu-id="6f2db-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f2db-129">Requirement</span></span> | <span data-ttu-id="6f2db-130">Valor</span><span class="sxs-lookup"><span data-stu-id="6f2db-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6f2db-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f2db-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6f2db-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f2db-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6f2db-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f2db-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6f2db-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f2db-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6f2db-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6f2db-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f2db-136">**V0 de imagem \_**</span><span class="sxs-lookup"><span data-stu-id="6f2db-136">**Image\_V0**</span></span>](image-v0.md)
</dt> </dl>

 

 




