---
title: Estrutura WMDMMetadataView
description: A estrutura WMDMMetadataView define a exibição de metadados. O conteúdo é organizado com base nessa definição.
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- Estrutura WMDMMetadataView Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDMMetadataView
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aa38a8fe7f19137c5caff18417d48ea23168b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788808"
---
# <a name="wmdmmetadataview-structure"></a><span data-ttu-id="25779-105">Estrutura WMDMMetadataView</span><span class="sxs-lookup"><span data-stu-id="25779-105">WMDMMetadataView structure</span></span>

<span data-ttu-id="25779-106">A estrutura **WMDMMetadataView** define a exibição de metadados.</span><span class="sxs-lookup"><span data-stu-id="25779-106">The **WMDMMetadataView** structure defines the metadata view.</span></span> <span data-ttu-id="25779-107">O conteúdo é organizado com base nessa definição.</span><span class="sxs-lookup"><span data-stu-id="25779-107">Content is organized based on this definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="25779-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25779-108">Syntax</span></span>


```C++
typedef struct _WMDMMetadataView {
  WCHAR *pwszViewName;
  UINT  nDepth;
  WCHAR **ppwszTags;
} WMDMMetadataView;
```



## <a name="members"></a><span data-ttu-id="25779-109">Membros</span><span class="sxs-lookup"><span data-stu-id="25779-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="25779-110">**pwszViewName**</span><span class="sxs-lookup"><span data-stu-id="25779-110">**pwszViewName**</span></span>
</dt> <dd>

<span data-ttu-id="25779-111">Ponteiro para uma cadeia de caracteres com terminação nula de caractere largo que contém o nome da exibição.</span><span class="sxs-lookup"><span data-stu-id="25779-111">Pointer to a wide-character null-terminated string containing the name of the view.</span></span> <span data-ttu-id="25779-112">Isso é usado como o nome do nó raiz no qual essa exibição é apresentada.</span><span class="sxs-lookup"><span data-stu-id="25779-112">This is used as the name of the root node under which this view is presented.</span></span>

</dd> <dt>

<span data-ttu-id="25779-113">**nDepth**</span><span class="sxs-lookup"><span data-stu-id="25779-113">**nDepth**</span></span>
</dt> <dd>

<span data-ttu-id="25779-114">Inteiro que contém a profundidade da exibição, que indica quantas marcas de metadados aninhadas são usadas para a exibição.</span><span class="sxs-lookup"><span data-stu-id="25779-114">Integer containing the depth of the view, which indicates how many nested metadata tags are used for the view.</span></span>

</dd> <dt>

<span data-ttu-id="25779-115">**ppwszTags**</span><span class="sxs-lookup"><span data-stu-id="25779-115">**ppwszTags**</span></span>
</dt> <dd>

<span data-ttu-id="25779-116">Matriz de cadeias de caracteres de marca de metadados para as marcas aninhadas.</span><span class="sxs-lookup"><span data-stu-id="25779-116">Array of metadata tag strings for the nested tags.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="25779-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="25779-117">Examples</span></span>

<span data-ttu-id="25779-118">O código a seguir cria uma exibição de metadados:</span><span class="sxs-lookup"><span data-stu-id="25779-118">The following code creates a metadata view:</span></span>


```C++
WMDMMetadataView view;
view.pwszName = L"My View";
view.nDepth = 3;  // genre, artist, album
LPCWSTR wszTagArray[3]; 
wszTagArray[0] = g_wszWMDMGenre;
wszTagArray[1] = g_wszWMDMAuthor;
wszTagArray[2] = g_wszWMDMAlbumTitle;
view.ppwszTags = wszTagArray;
```



<span data-ttu-id="25779-119">O código anterior organiza o conteúdo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="25779-119">The preceding code organizes content as follows:</span></span>

<dl> <span data-ttu-id="25779-120">Minha exibição</span><span class="sxs-lookup"><span data-stu-id="25779-120">My View</span></span><dl> <span data-ttu-id="25779-121">Genre1</span><span class="sxs-lookup"><span data-stu-id="25779-121">Genre1</span></span><dl> <span data-ttu-id="25779-122">Artist1</span><span class="sxs-lookup"><span data-stu-id="25779-122">Artist1</span></span><dl> <span data-ttu-id="25779-123">Album1</span><span class="sxs-lookup"><span data-stu-id="25779-123">Album1</span></span><dl> <span data-ttu-id="25779-124">Song1</span><span class="sxs-lookup"><span data-stu-id="25779-124">Song1</span></span>  
<span data-ttu-id="25779-125">Song2</span><span class="sxs-lookup"><span data-stu-id="25779-125">Song2</span></span>  
<span data-ttu-id="25779-126">...</span><span class="sxs-lookup"><span data-stu-id="25779-126">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> <span data-ttu-id="25779-127">Album1</span><span class="sxs-lookup"><span data-stu-id="25779-127">Album1</span></span><dl> <span data-ttu-id="25779-128">Song1</span><span class="sxs-lookup"><span data-stu-id="25779-128">Song1</span></span>  
<span data-ttu-id="25779-129">Song2</span><span class="sxs-lookup"><span data-stu-id="25779-129">Song2</span></span>  
<span data-ttu-id="25779-130">...</span><span class="sxs-lookup"><span data-stu-id="25779-130">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> <span data-ttu-id="25779-131">Artist1</span><span class="sxs-lookup"><span data-stu-id="25779-131">Artist1</span></span><dl> <span data-ttu-id="25779-132">Album1</span><span class="sxs-lookup"><span data-stu-id="25779-132">Album1</span></span><dl> <span data-ttu-id="25779-133">Song1</span><span class="sxs-lookup"><span data-stu-id="25779-133">Song1</span></span>  
<span data-ttu-id="25779-134">Song2</span><span class="sxs-lookup"><span data-stu-id="25779-134">Song2</span></span>  
<span data-ttu-id="25779-135">...</span><span class="sxs-lookup"><span data-stu-id="25779-135">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> <span data-ttu-id="25779-136">Album1</span><span class="sxs-lookup"><span data-stu-id="25779-136">Album1</span></span><dl> <span data-ttu-id="25779-137">Song1</span><span class="sxs-lookup"><span data-stu-id="25779-137">Song1</span></span>  
<span data-ttu-id="25779-138">Song2</span><span class="sxs-lookup"><span data-stu-id="25779-138">Song2</span></span>  
<span data-ttu-id="25779-139">...</span><span class="sxs-lookup"><span data-stu-id="25779-139">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> ...  
</dl> </dd> ...  
</dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25779-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25779-140">Requirements</span></span>



| <span data-ttu-id="25779-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="25779-141">Requirement</span></span> | <span data-ttu-id="25779-142">Valor</span><span class="sxs-lookup"><span data-stu-id="25779-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="25779-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="25779-143">Header</span></span><br/> | <dl> <span data-ttu-id="25779-144"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="25779-144"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25779-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="25779-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25779-146">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="25779-146">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





