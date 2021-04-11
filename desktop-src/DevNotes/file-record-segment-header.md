---
description: Representa o segmento de registro de arquivo. Este é o cabeçalho de cada segmento de registro de arquivo na MFT (tabela de arquivos mestre).
ms.assetid: 4548ad49-1924-4888-8966-c45f8e453c6f
title: Estrutura de FILE_RECORD_SEGMENT_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_RECORD_SEGMENT_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 293bb14dbaee0853aa1ef293502724458e02e26f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163918"
---
# <a name="file_record_segment_header-structure"></a><span data-ttu-id="97bed-104">\_Estrutura do \_ cabeçalho do segmento de registro de arquivo \_</span><span class="sxs-lookup"><span data-stu-id="97bed-104">FILE\_RECORD\_SEGMENT\_HEADER structure</span></span>

<span data-ttu-id="97bed-105">\[Essa estrutura é válida somente para a versão 3 de volumes NTFS; Ele pode ser alterado em versões futuras.\]</span><span class="sxs-lookup"><span data-stu-id="97bed-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="97bed-106">Representa o segmento de registro de arquivo.</span><span class="sxs-lookup"><span data-stu-id="97bed-106">Represents the file record segment.</span></span> <span data-ttu-id="97bed-107">Este é o cabeçalho de cada segmento de registro de arquivo na MFT (tabela de arquivos mestre).</span><span class="sxs-lookup"><span data-stu-id="97bed-107">This is the header for each file record segment in the master file table (MFT).</span></span>

## <a name="syntax"></a><span data-ttu-id="97bed-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97bed-108">Syntax</span></span>


```C++
typedef struct _FILE_RECORD_SEGMENT_HEADER {
  MULTI_SECTOR_HEADER   MultiSectorHeader;
  ULONGLONG             Reserved1;
  USHORT                SequenceNumber;
  USHORT                Reserved2;
  USHORT                FirstAttributeOffset;
  USHORT                Flags;
  ULONG                 Reserved3[2];
  FILE_REFERENCE        BaseFileRecordSegment;
  USHORT                Reserved4;
  UPDATE_SEQUENCE_ARRAY UpdateSequenceArray;
} FILE_RECORD_SEGMENT_HEADER, *PFILE_RECORD_SEGMENT_HEADER;
```



## <a name="members"></a><span data-ttu-id="97bed-109">Membros</span><span class="sxs-lookup"><span data-stu-id="97bed-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="97bed-110">**MultiSectorHeader**</span><span class="sxs-lookup"><span data-stu-id="97bed-110">**MultiSectorHeader**</span></span>
</dt> <dd>

<span data-ttu-id="97bed-111">O cabeçalho de multisetor definido pelo Gerenciador de cache.</span><span class="sxs-lookup"><span data-stu-id="97bed-111">The multisector header defined by the cache manager.</span></span> <span data-ttu-id="97bed-112">A estrutura de [**\_ \_ cabeçalho de vários setores**](multi-sector-header.md) sempre contém a assinatura "File" e uma descrição do local e do tamanho da matriz de sequência de atualização.</span><span class="sxs-lookup"><span data-stu-id="97bed-112">The [**MULTI\_SECTOR\_HEADER**](multi-sector-header.md) structure always contains the signature "FILE" and a description of the location and size of the update sequence array.</span></span>

</dd> <dt>

<span data-ttu-id="97bed-113">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="97bed-113">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="97bed-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="97bed-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="97bed-115">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="97bed-115">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="97bed-116">O número de sequência.</span><span class="sxs-lookup"><span data-stu-id="97bed-116">The sequence number.</span></span> <span data-ttu-id="97bed-117">Esse valor é incrementado toda vez que um segmento de registro de arquivo é liberado; será 0 se o segmento não for usado.</span><span class="sxs-lookup"><span data-stu-id="97bed-117">This value is incremented each time that a file record segment is freed; it is 0 if the segment is not used.</span></span> <span data-ttu-id="97bed-118">O campo **SequenceNumber** de uma referência de arquivo deve corresponder ao conteúdo desse campo; Se eles não corresponderem, a referência do arquivo estará incorreta e provavelmente será obsoleta.</span><span class="sxs-lookup"><span data-stu-id="97bed-118">The **SequenceNumber** field of a file reference must match the contents of this field; if they do not match, the file reference is incorrect and probably obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="97bed-119">**Reserved2**</span><span class="sxs-lookup"><span data-stu-id="97bed-119">**Reserved2**</span></span>
</dt> <dd>

<span data-ttu-id="97bed-120">Reservado.</span><span class="sxs-lookup"><span data-stu-id="97bed-120">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="97bed-121">**FirstAttributeOffset**</span><span class="sxs-lookup"><span data-stu-id="97bed-121">**FirstAttributeOffset**</span></span>
</dt> <dd>

<span data-ttu-id="97bed-122">O deslocamento do primeiro registro de atributo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="97bed-122">The offset of the first attribute record, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="97bed-123">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="97bed-123">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="97bed-124">Os sinalizadores de arquivo.</span><span class="sxs-lookup"><span data-stu-id="97bed-124">The file flags.</span></span>

<dl> <dt>

<span data-ttu-id="97bed-125"><span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>Do **arquivo \_ \_Segmento \_ de registro em \_ uso** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="97bed-125"><span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**FILE\_RECORD\_SEGMENT\_IN\_USE** (0x0001)</span></span>
</dt> <dt>

<span data-ttu-id="97bed-126"><span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>Do **arquivo \_ Índice de nome de arquivo \_ \_ \_ presente** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="97bed-126"><span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**FILE\_FILE\_NAME\_INDEX\_PRESENT** (0x0002)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="97bed-127">**Reserved3**</span><span class="sxs-lookup"><span data-stu-id="97bed-127">**Reserved3**</span></span>
</dt> <dd>

<span data-ttu-id="97bed-128">Reservado.</span><span class="sxs-lookup"><span data-stu-id="97bed-128">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="97bed-129">**BaseFileRecordSegment**</span><span class="sxs-lookup"><span data-stu-id="97bed-129">**BaseFileRecordSegment**</span></span>
</dt> <dd>

<span data-ttu-id="97bed-130">Uma referência de arquivo para o segmento de registro de arquivo base para este arquivo.</span><span class="sxs-lookup"><span data-stu-id="97bed-130">A file reference to the base file record segment for this file.</span></span> <span data-ttu-id="97bed-131">Se esse for o registro de arquivo base, o valor será 0.</span><span class="sxs-lookup"><span data-stu-id="97bed-131">If this is the base file record, the value is 0.</span></span> <span data-ttu-id="97bed-132">Consulte [**\_ \_ referência de segmento de MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="97bed-132">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bed-133">**Reserved4**</span><span class="sxs-lookup"><span data-stu-id="97bed-133">**Reserved4**</span></span>
</dt> <dd>

<span data-ttu-id="97bed-134">Reservado.</span><span class="sxs-lookup"><span data-stu-id="97bed-134">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="97bed-135">**UpdateSequenceArray**</span><span class="sxs-lookup"><span data-stu-id="97bed-135">**UpdateSequenceArray**</span></span>
</dt> <dd>

<span data-ttu-id="97bed-136">A matriz de sequência de atualização para proteger as transferências de multisetor do segmento de registro de arquivo.</span><span class="sxs-lookup"><span data-stu-id="97bed-136">The update sequence array to protect multisector transfers of the file record segment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97bed-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="97bed-137">Remarks</span></span>

<span data-ttu-id="97bed-138">Observe que não há nenhum arquivo de cabeçalho associado para essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="97bed-138">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="97bed-139">Essa definição de estrutura é válida somente para a versão principal 3 e secundária 0 ou 1, conforme relatado [**pelo \_ fsctl \_ obter \_ \_ dados de volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="97bed-139">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="97bed-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="97bed-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97bed-141">Tabela de arquivos mestre</span><span class="sxs-lookup"><span data-stu-id="97bed-141">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
