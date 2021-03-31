---
title: Estrutura de WINBIO_BIR_DATA (WinBio \_ Types. h)
description: Especifica o tamanho, em bytes, e o deslocamento de um bloco de informações biométricas.
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_BIR_DATA
topic_type:
- apiref
api_name:
- WINBIO_BIR_DATA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ebf7b157c5bd806442cdc120350a89ce646f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369585"
---
# <a name="winbio_bir_data-structure"></a><span data-ttu-id="a268b-104">\_Estrutura de \_ dados WINBIO Bir</span><span class="sxs-lookup"><span data-stu-id="a268b-104">WINBIO\_BIR\_DATA structure</span></span>

<span data-ttu-id="a268b-105">A estrutura de **\_ \_ dados WINBIO Bir** especifica o tamanho, em bytes, e o deslocamento de um bloco de informações biométricas.</span><span class="sxs-lookup"><span data-stu-id="a268b-105">The **WINBIO\_BIR\_DATA** structure specifies the size, in bytes, and the offset of a block of biometric information.</span></span> <span data-ttu-id="a268b-106">Essa estrutura é usada pela estrutura [**WINBIO \_ Bir**](winbio-bir.md) para especificar onde as várias partes de um registro de informações biométricas estão localizadas.</span><span class="sxs-lookup"><span data-stu-id="a268b-106">This structure is used by the [**WINBIO\_BIR**](winbio-bir.md) structure to specify where the various parts of a biometric information record are located.</span></span>

## <a name="syntax"></a><span data-ttu-id="a268b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a268b-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR_DATA {
  ULONG Size;
  ULONG Offset;
} WINBIO_BIR_DATA;
```



## <a name="members"></a><span data-ttu-id="a268b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a268b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a268b-109">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="a268b-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="a268b-110">Tamanho, em bytes, das informações biométricas.</span><span class="sxs-lookup"><span data-stu-id="a268b-110">Size, in bytes, of the biometric information.</span></span>

</dd> <dt>

<span data-ttu-id="a268b-111">**Deslocamento**</span><span class="sxs-lookup"><span data-stu-id="a268b-111">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="a268b-112">Offset, em bytes do início da estrutura [**WINBIO \_ Bir**](winbio-bir.md) , das informações biométricas.</span><span class="sxs-lookup"><span data-stu-id="a268b-112">Offset, in bytes from the beginning of the [**WINBIO\_BIR**](winbio-bir.md) structure, of the biometric information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a268b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a268b-113">Remarks</span></span>

<span data-ttu-id="a268b-114">O uso de deslocamentos em vez de ponteiros permite uma fácil serialização do BIR e para uma tradução menos complicada entre os ambientes de 32 e 64 bits ou entre o modo de usuário e kernel.</span><span class="sxs-lookup"><span data-stu-id="a268b-114">The use of offsets rather than pointers allows for easy serialization of the BIR and for less complicated translation between 32 and 64-bit environments or between user and kernel mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="a268b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a268b-115">Requirements</span></span>



| <span data-ttu-id="a268b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a268b-116">Requirement</span></span> | <span data-ttu-id="a268b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a268b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a268b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a268b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a268b-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a268b-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="a268b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a268b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a268b-121">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="a268b-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a268b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a268b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a268b-123"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a268b-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a268b-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a268b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a268b-125">Estruturas de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="a268b-125">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="a268b-126">**WINBIO \_ Bir**</span><span class="sxs-lookup"><span data-stu-id="a268b-126">**WINBIO\_BIR**</span></span>](winbio-bir.md)
</dt> <dt>

[<span data-ttu-id="a268b-127">**\_cabeçalho WINBIO Bir \_**</span><span class="sxs-lookup"><span data-stu-id="a268b-127">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





