---
title: Classe IMemoryAllocator
description: Implementado pelo alocador de memória para a função StgConvertPropertyToVariant.
ms.assetid: a0735b62-5ed3-42df-a320-b58c742645a8
keywords:
- Armazenamento estruturado da classe IMemoryAllocator
- Armazenamento estruturado da classe IMemoryAllocator, descrito
topic_type:
- apiref
api_name:
- IMemoryAllocator
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421162fd0ee6228f1dbae03eeb52e5643b0e0b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369669"
---
# <a name="imemoryallocator-class"></a><span data-ttu-id="cffad-105">Classe IMemoryAllocator</span><span class="sxs-lookup"><span data-stu-id="cffad-105">IMemoryAllocator class</span></span>

<span data-ttu-id="cffad-106">A classe **IMemoryAllocator** é implementada pelo alocador de memória para a função [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .</span><span class="sxs-lookup"><span data-stu-id="cffad-106">The **IMemoryAllocator** class is implemented by the memory allocator for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function.</span></span>

## <a name="methods"></a><span data-ttu-id="cffad-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="cffad-107">Methods</span></span>



| <span data-ttu-id="cffad-108">Nome</span><span class="sxs-lookup"><span data-stu-id="cffad-108">Name</span></span>                                                     | <span data-ttu-id="cffad-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="cffad-109">Description</span></span>                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cffad-110">**Aloca**</span><span class="sxs-lookup"><span data-stu-id="cffad-110">**Allocate**</span></span>](imemoryallocator-allocate.md)<br/> | <span data-ttu-id="cffad-111">Aloca memória para a função [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) quando a função converte um tipo de dados **SERIALIZEDPROPERTYVALUE** para um tipo de dados **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="cffad-111">Allocates memory for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function when the function converts a **SERIALIZEDPROPERTYVALUE** data type to a **PROPVARIANT** data type.</span></span><br/> |
| [<span data-ttu-id="cffad-112">**Gratuita**</span><span class="sxs-lookup"><span data-stu-id="cffad-112">**Free**</span></span>](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize)<br/>        | <span data-ttu-id="cffad-113">Libera a memória alocada pelo método [**ALLOCATE**](imemoryallocator-allocate.md) .</span><span class="sxs-lookup"><span data-stu-id="cffad-113">Frees the memory allocated by the [**Allocate**](imemoryallocator-allocate.md) method.</span></span><br/>                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="cffad-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cffad-114">Remarks</span></span>

<span data-ttu-id="cffad-115">Essa classe é usada somente pela função [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .</span><span class="sxs-lookup"><span data-stu-id="cffad-115">This class is only used by the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cffad-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cffad-116">Requirements</span></span>



| <span data-ttu-id="cffad-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cffad-117">Requirement</span></span> | <span data-ttu-id="cffad-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cffad-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cffad-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cffad-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cffad-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cffad-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cffad-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cffad-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cffad-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cffad-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cffad-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cffad-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="cffad-124"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cffad-124"><dt>Ole32.lib</dt></span></span> </dl> |



 

