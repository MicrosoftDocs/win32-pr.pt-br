---
title: Método IMemoryAllocator Allocate
description: O método Allocate aloca memória para a função StgConvertPropertyToVariant quando a função converte um tipo de dados SERIALIZEDPROPERTYVALUE para um tipo de dados PROPVARIANT.
ms.assetid: aa9c9308-fb55-405c-901a-9d5abfac5395
keywords:
- Alocar o armazenamento estruturado do método
- Alocar o armazenamento estruturado do método, interface IMemoryAllocator
- Armazenamento estruturado da interface IMemoryAllocator, método Allocate
topic_type:
- apiref
api_name:
- IMemoryAllocator.Allocate
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ee4b220e1c1e14ceed685e9b2adc694a44d2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755779"
---
# <a name="imemoryallocatorallocate-method"></a><span data-ttu-id="bdd71-106">Método IMemoryAllocator:: Allocate</span><span class="sxs-lookup"><span data-stu-id="bdd71-106">IMemoryAllocator::Allocate method</span></span>

<span data-ttu-id="bdd71-107">O método **ALLOCATE aloca** memória para a função [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) quando a função converte um tipo de dados **SERIALIZEDPROPERTYVALUE** para um tipo de dados **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="bdd71-107">The **Allocate** method allocates memory for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function when the function converts a **SERIALIZEDPROPERTYVALUE** data type to a **PROPVARIANT** data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdd71-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdd71-108">Syntax</span></span>


```C++
virtual void* Allocate(
  [in] ULONG cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="bdd71-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdd71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdd71-110">*cbSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bdd71-110">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdd71-111">Especifica o tamanho da memória a ser alocada.</span><span class="sxs-lookup"><span data-stu-id="bdd71-111">Specifies the size of memory to be allocated.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bdd71-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdd71-112">Requirements</span></span>



| <span data-ttu-id="bdd71-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdd71-113">Requirement</span></span> | <span data-ttu-id="bdd71-114">Valor</span><span class="sxs-lookup"><span data-stu-id="bdd71-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd71-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdd71-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bdd71-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bdd71-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bdd71-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdd71-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bdd71-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bdd71-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bdd71-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bdd71-119">Library</span></span><br/>                  | <dl> <span data-ttu-id="bdd71-120"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdd71-120"><dt>Ole32.lib</dt></span></span> </dl> |



 

