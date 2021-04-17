---
title: Estrutura ICONRESDIR
description: Contém as dimensões e o formato de cor de uma imagem de ícone individual em um grupo de recursos. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: 4c727369-2e90-40ad-85af-96d7e060b97a
keywords:
- Menus de estrutura ICONRESDIR e outros recursos
topic_type:
- apiref
api_name:
- ICONRESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de3d15bf250685e0b0cad935cd5e8094b2f2ceee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753895"
---
# <a name="iconresdir-structure"></a><span data-ttu-id="d7d97-105">Estrutura ICONRESDIR</span><span class="sxs-lookup"><span data-stu-id="d7d97-105">ICONRESDIR structure</span></span>

<span data-ttu-id="d7d97-106">Contém as dimensões e o formato de cor de uma imagem de ícone individual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7d97-106">Contains the dimensions and color format of an individual icon image in a resource group.</span></span> <span data-ttu-id="d7d97-107">A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="d7d97-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7d97-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7d97-108">Syntax</span></span>


```C++
typedef struct {
  BYTE Width;
  BYTE Height;
  BYTE ColorCount;
  BYTE reserved;
} ICONRESDIR;
```



## <a name="members"></a><span data-ttu-id="d7d97-109">Membros</span><span class="sxs-lookup"><span data-stu-id="d7d97-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7d97-110">**Largura**</span><span class="sxs-lookup"><span data-stu-id="d7d97-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="d7d97-111">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="d7d97-111">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="d7d97-112">A largura do ícone, em pixels.</span><span class="sxs-lookup"><span data-stu-id="d7d97-112">The width of the icon, in pixels.</span></span> <span data-ttu-id="d7d97-113">Os valores aceitáveis são 16, 32 e 64.</span><span class="sxs-lookup"><span data-stu-id="d7d97-113">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="d7d97-114">**Altura**</span><span class="sxs-lookup"><span data-stu-id="d7d97-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="d7d97-115">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="d7d97-115">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="d7d97-116">A altura do ícone, em pixels.</span><span class="sxs-lookup"><span data-stu-id="d7d97-116">The height of the icon, in pixels.</span></span> <span data-ttu-id="d7d97-117">Os valores aceitáveis são 16, 32 e 64.</span><span class="sxs-lookup"><span data-stu-id="d7d97-117">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="d7d97-118">**ColorCount**</span><span class="sxs-lookup"><span data-stu-id="d7d97-118">**ColorCount**</span></span>
</dt> <dd>

<span data-ttu-id="d7d97-119">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="d7d97-119">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="d7d97-120">O número de cores no ícone.</span><span class="sxs-lookup"><span data-stu-id="d7d97-120">The number of colors in the icon.</span></span> <span data-ttu-id="d7d97-121">Os valores aceitáveis são 2, 8 e 16.</span><span class="sxs-lookup"><span data-stu-id="d7d97-121">Acceptable values are 2, 8, and 16.</span></span>

</dd> <dt>

<span data-ttu-id="d7d97-122">**reservado**</span><span class="sxs-lookup"><span data-stu-id="d7d97-122">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="d7d97-123">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="d7d97-123">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="d7d97-124">Reservado deve ser definido com o mesmo valor do campo reservado no cabeçalho do arquivo de ícone.</span><span class="sxs-lookup"><span data-stu-id="d7d97-124">Reserved; must be set to the same value as that of the reserved field in the icon file header.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7d97-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7d97-125">Remarks</span></span>

<span data-ttu-id="d7d97-126">A estrutura **ICONRESDIR** será passada na estrutura [**RESDIR**](resdir.md) se a estrutura **RESDIR** descrever um ícone.</span><span class="sxs-lookup"><span data-stu-id="d7d97-126">The **ICONRESDIR** structure is passed in the [**RESDIR**](resdir.md) structure if the **RESDIR** structure describes an icon.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7d97-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7d97-127">Requirements</span></span>



| <span data-ttu-id="d7d97-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7d97-128">Requirement</span></span> | <span data-ttu-id="d7d97-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d7d97-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d7d97-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7d97-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d7d97-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d7d97-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d7d97-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7d97-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d7d97-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d7d97-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d7d97-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7d97-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="d7d97-135">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d7d97-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d7d97-136">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="d7d97-136">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="d7d97-137">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="d7d97-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d7d97-138">Recursos</span><span class="sxs-lookup"><span data-stu-id="d7d97-138">Resources</span></span>](resources.md)
</dt> </dl>

 

 





