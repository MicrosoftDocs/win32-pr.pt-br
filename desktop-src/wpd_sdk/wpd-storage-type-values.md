---
description: O \_ tipo de enumeração de valores de tipo de armazenamento WPD \_ \_ descreve os diferentes tipos de armazenamento de dispositivo portátil do Windows.
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: Enumeração de WPD_STORAGE_TYPE_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STORAGE_TYPE_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b741feb1cb9a834e16a35627fe98718ac8acf30f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752759"
---
# <a name="wpd_storage_type_values-enumeration"></a><span data-ttu-id="16aba-103">\_Enumeração de \_ valores de tipo de armazenamento WPD \_</span><span class="sxs-lookup"><span data-stu-id="16aba-103">WPD\_STORAGE\_TYPE\_VALUES enumeration</span></span>

<span data-ttu-id="16aba-104">O tipo de enumeração de **\_ valores de \_ tipo \_ de armazenamento WPD** descreve os diferentes tipos de armazenamento de dispositivo portátil do Windows.</span><span class="sxs-lookup"><span data-stu-id="16aba-104">The **WPD\_STORAGE\_TYPE\_VALUES** enumeration type describes the different Windows Portable Device storage types.</span></span>

## <a name="syntax"></a><span data-ttu-id="16aba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="16aba-105">Syntax</span></span>


```C++
typedef enum tagWPD_STORAGE_TYPE_VALUES { 
  WPD_STORAGE_TYPE_UNDEFINED      = 0,
  WPD_STORAGE_TYPE_FIXED_ROM      = 1,
  WPD_STORAGE_TYPE_REMOVABLE_ROM  = 2,
  WPD_STORAGE_TYPE_FIXED_RAM      = 3,
  WPD_STORAGE_TYPE_REMOVABLE_RAM  = 4
} WPD_STORAGE_TYPE_VALUES;
```



## <a name="constants"></a><span data-ttu-id="16aba-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="16aba-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="16aba-107"><span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**\_tipo de armazenamento WPD \_ \_ indefinido**</span><span class="sxs-lookup"><span data-stu-id="16aba-107"><span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**WPD\_STORAGE\_TYPE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="16aba-108">O armazenamento é de um tipo indefinido.</span><span class="sxs-lookup"><span data-stu-id="16aba-108">The storage is of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="16aba-109"><span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**\_ \_ ROM fixa de tipo de armazenamento WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="16aba-109"><span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**WPD\_STORAGE\_TYPE\_FIXED\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="16aba-110">O armazenamento não é removível e somente leitura.</span><span class="sxs-lookup"><span data-stu-id="16aba-110">The storage is non-removable and read-only.</span></span>

</dd> <dt>

<span data-ttu-id="16aba-111"><span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**\_ \_ \_ ROM removível de tipo de armazenamento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="16aba-111"><span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**WPD\_STORAGE\_TYPE\_REMOVABLE\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="16aba-112">O armazenamento é removível e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="16aba-112">The storage is removable and is read-only.</span></span>

</dd> <dt>

<span data-ttu-id="16aba-113"><span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**\_ \_ RAM fixa de tipo de armazenamento WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="16aba-113"><span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**WPD\_STORAGE\_TYPE\_FIXED\_RAM**</span></span>
</dt> <dd>

<span data-ttu-id="16aba-114">O armazenamento não é removível e é compatível com leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="16aba-114">The storage is non-removable and is read/write capable.</span></span>

</dd> <dt>

<span data-ttu-id="16aba-115"><span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**\_ \_ \_ RAM removível de tipo de armazenamento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="16aba-115"><span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**WPD\_STORAGE\_TYPE\_REMOVABLE\_RAM**</span></span>
</dt> <dd>

<span data-ttu-id="16aba-116">O armazenamento é removível e é compatível com leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="16aba-116">The storage is removable and is read/write capable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16aba-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="16aba-117">Remarks</span></span>

<span data-ttu-id="16aba-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="16aba-118">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="16aba-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16aba-119">Requirements</span></span>



| <span data-ttu-id="16aba-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="16aba-120">Requirement</span></span> | <span data-ttu-id="16aba-121">Valor</span><span class="sxs-lookup"><span data-stu-id="16aba-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="16aba-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16aba-122">Header</span></span><br/> | <dl> <span data-ttu-id="16aba-123"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="16aba-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16aba-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="16aba-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16aba-125">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="16aba-125">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




