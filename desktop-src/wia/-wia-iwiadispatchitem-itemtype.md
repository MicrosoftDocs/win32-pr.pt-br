---
description: O tipo deste item. Somente leitura.
ms.assetid: 6c613a08-41aa-4242-80c0-75e1981a676f
title: Propriedade Item. ItemType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ItemType
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 9b70f7a1698ecdb4de023786f21a6ef9d55f681d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790395"
---
# <a name="itemitemtype-property"></a><span data-ttu-id="9aa6b-104">Propriedade Item. ItemType</span><span class="sxs-lookup"><span data-stu-id="9aa6b-104">Item.ItemType property</span></span>

<span data-ttu-id="9aa6b-105">O tipo deste item.</span><span class="sxs-lookup"><span data-stu-id="9aa6b-105">The type of this item.</span></span> <span data-ttu-id="9aa6b-106">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="9aa6b-106">Read-only.</span></span>

<span data-ttu-id="9aa6b-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="9aa6b-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa6b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9aa6b-108">Syntax</span></span>


```JScript
propVal = Item.ItemType
```



## <a name="property-value"></a><span data-ttu-id="9aa6b-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9aa6b-109">Property value</span></span>

<span data-ttu-id="9aa6b-110">Os seguintes valores são possíveis:</span><span class="sxs-lookup"><span data-stu-id="9aa6b-110">The following values are possible:</span></span>



| <span data-ttu-id="9aa6b-111">Valor</span><span class="sxs-lookup"><span data-stu-id="9aa6b-111">Value</span></span>  | <span data-ttu-id="9aa6b-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="9aa6b-112">Description</span></span>                                     |
|--------|-------------------------------------------------|
| <span data-ttu-id="9aa6b-113">dispositivo</span><span class="sxs-lookup"><span data-stu-id="9aa6b-113">device</span></span> | <span data-ttu-id="9aa6b-114">O item é um dispositivo de hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="9aa6b-114">The item is a WIA hardware device.</span></span>              |
| <span data-ttu-id="9aa6b-115">folder</span><span class="sxs-lookup"><span data-stu-id="9aa6b-115">folder</span></span> | <span data-ttu-id="9aa6b-116">O item é uma pasta que contém outros itens.</span><span class="sxs-lookup"><span data-stu-id="9aa6b-116">The item is a folder that contains other items.</span></span> |
| <span data-ttu-id="9aa6b-117">arquivo</span><span class="sxs-lookup"><span data-stu-id="9aa6b-117">file</span></span>   | <span data-ttu-id="9aa6b-118">O item é um arquivo de imagem ou áudio.</span><span class="sxs-lookup"><span data-stu-id="9aa6b-118">The item is an image or audio file.</span></span>             |
| <span data-ttu-id="9aa6b-119">áudio</span><span class="sxs-lookup"><span data-stu-id="9aa6b-119">audio</span></span>  | <span data-ttu-id="9aa6b-120">O item é um clipe de áudio.</span><span class="sxs-lookup"><span data-stu-id="9aa6b-120">The item is an audio clip.</span></span>                      |
| <span data-ttu-id="9aa6b-121">image</span><span class="sxs-lookup"><span data-stu-id="9aa6b-121">image</span></span>  | <span data-ttu-id="9aa6b-122">O item é uma imagem.</span><span class="sxs-lookup"><span data-stu-id="9aa6b-122">The item is an image.</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="9aa6b-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="9aa6b-123">Remarks</span></span>

<span data-ttu-id="9aa6b-124">Um item pode ter mais de um tipo.</span><span class="sxs-lookup"><span data-stu-id="9aa6b-124">An item can have more than one type.</span></span> <span data-ttu-id="9aa6b-125">Por exemplo, cada imagem é dos tipos "imagem" e "arquivo".</span><span class="sxs-lookup"><span data-stu-id="9aa6b-125">For example, every image is of both "image" and "file" types.</span></span> <span data-ttu-id="9aa6b-126">**ItemType** retorna uma cadeia de caracteres que inclui todos os tipos válidos para o item, separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="9aa6b-126">**ItemType** returns a string that includes all valid types for the item, separated by semicolons.</span></span> <span data-ttu-id="9aa6b-127">Por exemplo, "Image; File".</span><span class="sxs-lookup"><span data-stu-id="9aa6b-127">For example, "image;file".</span></span> <span data-ttu-id="9aa6b-128">Não há nenhum espaço nessa cadeia de caracteres e não há um ponto-e-vírgula no final.</span><span class="sxs-lookup"><span data-stu-id="9aa6b-128">There are no spaces in this string, and there is not a semicolon at the end.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa6b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aa6b-129">Requirements</span></span>



| <span data-ttu-id="9aa6b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aa6b-130">Requirement</span></span> | <span data-ttu-id="9aa6b-131">Valor</span><span class="sxs-lookup"><span data-stu-id="9aa6b-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa6b-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9aa6b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9aa6b-133">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9aa6b-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9aa6b-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9aa6b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9aa6b-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9aa6b-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9aa6b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9aa6b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aa6b-137"><dt>Wiascr.dll (versão 4,90 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9aa6b-137"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




