---
description: Representa um endereço na MFT (tabela de arquivos mestre). O endereço é marcado com um número de sequência reutilizado circularmente que é definido no momento em que a referência de segmento de MFT era válida.
ms.assetid: 59d83b95-83fb-4630-8ce4-f58441c748ab
title: Estrutura de MFT_SEGMENT_REFERENCE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFT_SEGMENT_REFERENCE
api_type:
- NA
api_location: ''
ms.openlocfilehash: beabe7620dadd01b25b3556715b33e2f10c2c230
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088819"
---
# <a name="mft_segment_reference-structure"></a><span data-ttu-id="6a3e8-104">Estrutura de referência de \_ segmento de MFT \_</span><span class="sxs-lookup"><span data-stu-id="6a3e8-104">MFT\_SEGMENT\_REFERENCE structure</span></span>

<span data-ttu-id="6a3e8-105">\[Essa estrutura é válida somente para a versão 3 de volumes NTFS; Ele pode ser alterado em versões futuras.\]</span><span class="sxs-lookup"><span data-stu-id="6a3e8-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="6a3e8-106">Representa um endereço na MFT (tabela de arquivos mestre).</span><span class="sxs-lookup"><span data-stu-id="6a3e8-106">Represents an address in the master file table (MFT).</span></span> <span data-ttu-id="6a3e8-107">O endereço é marcado com um número de sequência reutilizado circularmente que é definido no momento em que a referência de segmento de MFT era válida.</span><span class="sxs-lookup"><span data-stu-id="6a3e8-107">The address is tagged with a circularly reused sequence number that is set at the time the MFT segment reference was valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a3e8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a3e8-108">Syntax</span></span>


```C++
typedef struct _MFT_SEGMENT_REFERENCE {
  ULONG  SegmentNumberLowPart;
  USHORT SegmentNumberHighPart;
  USHORT SequenceNumber;
} MFT_SEGMENT_REFERENCE, *PMFT_SEGMENT_REFERENCE;
```



## <a name="members"></a><span data-ttu-id="6a3e8-109">Membros</span><span class="sxs-lookup"><span data-stu-id="6a3e8-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="6a3e8-110">**SegmentNumberLowPart**</span><span class="sxs-lookup"><span data-stu-id="6a3e8-110">**SegmentNumberLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="6a3e8-111">A parte inferior do número do segmento.</span><span class="sxs-lookup"><span data-stu-id="6a3e8-111">The low part of the segment number.</span></span>

</dd> <dt>

<span data-ttu-id="6a3e8-112">**SegmentNumberHighPart**</span><span class="sxs-lookup"><span data-stu-id="6a3e8-112">**SegmentNumberHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="6a3e8-113">A parte superior do número do segmento.</span><span class="sxs-lookup"><span data-stu-id="6a3e8-113">The high part of the segment number.</span></span>

</dd> <dt>

<span data-ttu-id="6a3e8-114">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="6a3e8-114">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="6a3e8-115">O número de sequência diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="6a3e8-115">The nonzero sequence number.</span></span> <span data-ttu-id="6a3e8-116">O valor 0 é reservado.</span><span class="sxs-lookup"><span data-stu-id="6a3e8-116">The value 0 is reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a3e8-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a3e8-117">Remarks</span></span>

<span data-ttu-id="6a3e8-118">Observe que não há nenhum arquivo de cabeçalho associado para essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="6a3e8-118">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="6a3e8-119">Essa definição de estrutura é válida somente para a versão principal 3 e secundária 0 ou 1, conforme relatado [**pelo \_ fsctl \_ obter \_ \_ dados de volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="6a3e8-119">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="6a3e8-120">O tipo de dados de **\_ referência de arquivo** é definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="6a3e8-120">The **FILE\_REFERENCE** data type is defined as follows.</span></span>

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a><span data-ttu-id="6a3e8-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a3e8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a3e8-122">Tabela de arquivos mestre</span><span class="sxs-lookup"><span data-stu-id="6a3e8-122">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
