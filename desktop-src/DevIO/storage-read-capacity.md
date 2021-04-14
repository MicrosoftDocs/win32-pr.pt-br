---
description: Contém informações sobre o tamanho de um dispositivo. Isso é retornado do código de \_ controle de capacidade de leitura do armazenamento do IOCTL \_ \_ .
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: Estrutura de STORAGE_READ_CAPACITY (Ntddstor. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_READ_CAPACITY
api_type:
- HeaderDef
api_location:
- Ntddstor.h
ms.openlocfilehash: e57a9f4420b977598e15f9aae219c060665c9d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370386"
---
# <a name="storage_read_capacity-structure"></a><span data-ttu-id="ad34b-104">Estrutura de capacidade de \_ leitura de armazenamento \_</span><span class="sxs-lookup"><span data-stu-id="ad34b-104">STORAGE\_READ\_CAPACITY structure</span></span>

<span data-ttu-id="ad34b-105">Contém informações sobre o tamanho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ad34b-105">Contains information about the size of a device.</span></span> <span data-ttu-id="ad34b-106">Isso é retornado do código de controle de [**capacidade de leitura do armazenamento do IOCTL \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) .</span><span class="sxs-lookup"><span data-stu-id="ad34b-106">This is returned from the [**IOCTL\_STORAGE\_READ\_CAPACITY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad34b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad34b-107">Syntax</span></span>


```C++
typedef struct _STORAGE_READ_CAPACITY {
  ULONG         Version;
  ULONG         Size;
  ULONG         BlockLength;
  LARGE_INTEGER NumberOfBlocks;
  LARGE_INTEGER DiskLength;
} STORAGE_READ_CAPACITY, *PSTORAGE_READ_CAPACITY;
```



## <a name="members"></a><span data-ttu-id="ad34b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ad34b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ad34b-109">**Versão**</span><span class="sxs-lookup"><span data-stu-id="ad34b-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="ad34b-110">A versão desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="ad34b-110">The version of this structure.</span></span> <span data-ttu-id="ad34b-111">O chamador deve definir esse membro como `sizeof(STORAGE_READ_CAPACITY)` .</span><span class="sxs-lookup"><span data-stu-id="ad34b-111">The caller must set this member to `sizeof(STORAGE_READ_CAPACITY)`.</span></span>

</dd> <dt>

<span data-ttu-id="ad34b-112">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="ad34b-112">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="ad34b-113">O tamanho dos dados retornados.</span><span class="sxs-lookup"><span data-stu-id="ad34b-113">The size of the data returned.</span></span>

</dd> <dt>

<span data-ttu-id="ad34b-114">**BlockLength**</span><span class="sxs-lookup"><span data-stu-id="ad34b-114">**BlockLength**</span></span>
</dt> <dd>

<span data-ttu-id="ad34b-115">O número de bytes por bloco.</span><span class="sxs-lookup"><span data-stu-id="ad34b-115">The number of bytes per block.</span></span>

</dd> <dt>

<span data-ttu-id="ad34b-116">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="ad34b-116">**NumberOfBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="ad34b-117">O número total de blocos no disco.</span><span class="sxs-lookup"><span data-stu-id="ad34b-117">The total number of blocks on the disk.</span></span>

</dd> <dt>

<span data-ttu-id="ad34b-118">**DiskLength**</span><span class="sxs-lookup"><span data-stu-id="ad34b-118">**DiskLength**</span></span>
</dt> <dd>

<span data-ttu-id="ad34b-119">O tamanho do disco em bytes.</span><span class="sxs-lookup"><span data-stu-id="ad34b-119">The disk size in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad34b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad34b-120">Remarks</span></span>

<span data-ttu-id="ad34b-121">O arquivo de cabeçalho Ntddstor. h está disponível no WDK (Kit de driver do Windows).</span><span class="sxs-lookup"><span data-stu-id="ad34b-121">The header file Ntddstor.h is available in the Windows Driver Kit (WDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad34b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad34b-122">Requirements</span></span>



| <span data-ttu-id="ad34b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad34b-123">Requirement</span></span> | <span data-ttu-id="ad34b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ad34b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad34b-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad34b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ad34b-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad34b-126">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="ad34b-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad34b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ad34b-128">Windows Server 2008, Windows Server 2003 com SP1</span><span class="sxs-lookup"><span data-stu-id="ad34b-128">Windows Server 2008, Windows Server 2003 with SP1</span></span><br/>                          |
| <span data-ttu-id="ad34b-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad34b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad34b-130"><dt>Ntddstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad34b-130"><dt>Ntddstor.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad34b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad34b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad34b-132">**\_capacidade de \_ leitura do armazenamento do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="ad34b-132">**IOCTL\_STORAGE\_READ\_CAPACITY**</span></span>](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




