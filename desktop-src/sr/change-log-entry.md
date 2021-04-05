---
title: Estrutura de CHANGE_LOG_ENTRY
description: Uma entrada do log de alterações.
ms.assetid: adbdc6e6-895e-486d-a194-c74d2cbd0052
keywords:
- Restauração do sistema de estrutura CHANGE_LOG_ENTRY
- Restauração do sistema de ponteiro de estrutura de PCHANGE_LOG_ENTRY
topic_type:
- apiref
api_name:
- CHANGE_LOG_ENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a129b7c8368e6af1d259d6c19a9dde963d9deef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009010"
---
# <a name="change_log_entry-structure"></a><span data-ttu-id="4b917-105">ALTERAR \_ estrutura de entrada de log \_</span><span class="sxs-lookup"><span data-stu-id="4b917-105">CHANGE\_LOG\_ENTRY structure</span></span>

<span data-ttu-id="4b917-106">\[Essas informações se aplicam somente ao Windows XP com Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="4b917-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="4b917-107">Uma entrada do log de alterações.</span><span class="sxs-lookup"><span data-stu-id="4b917-107">A change log entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b917-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b917-108">Syntax</span></span>


```C++
typedef struct _CHANGE_LOG_ENTRY {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwEntryType;
  DWORD         dwEntryFlags;
  DWORD         dwAttributes;
  INT64         i64SequenceNum;
  WCHAR         szProcName[16];
} CHANGE_LOG_ENTRY, *PCHANGE_LOG_ENTRY;
```



## <a name="members"></a><span data-ttu-id="4b917-109">Membros</span><span class="sxs-lookup"><span data-stu-id="4b917-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="4b917-110">**RecordHeader**</span><span class="sxs-lookup"><span data-stu-id="4b917-110">**RecordHeader**</span></span>
</dt> <dd>

<span data-ttu-id="4b917-111">Uma estrutura de [**\_ cabeçalho de registro**](record-header.md) .</span><span class="sxs-lookup"><span data-stu-id="4b917-111">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="4b917-112">O membro **dwRecordType** deve ser definido como **RecordTypeLogEntry** (1).</span><span class="sxs-lookup"><span data-stu-id="4b917-112">The **dwRecordType** member should be set to **RecordTypeLogEntry** (1).</span></span>

</dd> <dt>

<span data-ttu-id="4b917-113">**dwMagicNum**</span><span class="sxs-lookup"><span data-stu-id="4b917-113">**dwMagicNum**</span></span>
</dt> <dd>

<span data-ttu-id="4b917-114">Esse membro deve ser definido como 0xabcdef12.</span><span class="sxs-lookup"><span data-stu-id="4b917-114">This member should be set to 0xabcdef12.</span></span>

</dd> <dt>

<span data-ttu-id="4b917-115">**dwEntryType**</span><span class="sxs-lookup"><span data-stu-id="4b917-115">**dwEntryType**</span></span>
</dt> <dd>

<span data-ttu-id="4b917-116">Esse membro pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="4b917-116">This member can be one of the following values:</span></span>

<dl><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0x2_"></span><span id="change_log_entrytypes_aclchange__0x2_"></span><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0X2_"></span><dt>

<span data-ttu-id="4b917-117">LOG de alterações \_ \_ ENTRYTYPES \_ ACLCHANGE \* \* (0x2) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-117">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ACLCHANGE\*\* (0x2)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0x4_"></span><span id="change_log_entrytypes_attrchange__0x4_"></span><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0X4_"></span><dt>

<span data-ttu-id="4b917-118">LOG de alterações \_ \_ ENTRYTYPES \_ ATTRCHANGE \* \* (0x4) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-118">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ATTRCHANGE\*\* (0x4)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0x80_"></span><span id="change_log_entrytypes_dircreate__0x80_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0X80_"></span><dt>

<span data-ttu-id="4b917-119">LOG de alterações \_ \_ ENTRYTYPES \_ DIRCREATE \* \* (0x80) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-119">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRCREATE\*\* (0x80)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0x100_"></span><span id="change_log_entrytypes_dirrename__0x100_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0X100_"></span><dt>

<span data-ttu-id="4b917-120">LOG de alterações \_ \_ ENTRYTYPES \_ DIRRENAME \* \* (0x100) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-120">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRRENAME\*\* (0x100)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0x200_"></span><span id="change_log_entrytypes_dirdelete__0x200_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0X200_"></span><dt>

<span data-ttu-id="4b917-121">LOG de alterações \_ \_ ENTRYTYPES \_ DIRDELETE \* \* (0x200) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-121">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRDELETE\*\* (0x200)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0x20_"></span><span id="change_log_entrytypes_filecreate__0x20_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0X20_"></span><dt>

<span data-ttu-id="4b917-122">\_ENTRYTYPES de log de alteração \ \_ \_ Create \* \* (0x20) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-122">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILECREATE\*\* (0x20)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0x10_"></span><span id="change_log_entrytypes_filedelete__0x10_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0X10_"></span><dt>

<span data-ttu-id="4b917-123">ALTERAR \_ log \_ ENTRYTYPES \_ filedelete \* \* (0x10) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-123">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILEDELETE\*\* (0x10)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0x40_"></span><span id="change_log_entrytypes_filerename__0x40_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0X40_"></span><dt>

<span data-ttu-id="4b917-124">\_ENTRYTYPES de log de alteração \ \_ \_ renomeação de logs \* \* (0x40) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-124">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILERENAME\*\* (0x40)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0x100000_"></span><span id="change_log_entrytypes_inprecreate__0x100000_"></span><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0X100000_"></span><dt>

<span data-ttu-id="4b917-125">LOG de alterações \_ \_ ENTRYTYPES \_ INPRECREATE \* \* (0x100000) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-125">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_INPRECREATE\*\* (0x100000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0x20000_"></span><span id="change_log_entrytypes_isdir__0x20000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0X20000_"></span><dt>

<span data-ttu-id="4b917-126">LOG de alterações \_ \_ ENTRYTYPES \_ ISDIR \* \* (0x20000) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-126">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ISDIR\*\* (0x20000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0x40000_"></span><span id="change_log_entrytypes_isnotdir__0x40000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0X40000_"></span><dt>

<span data-ttu-id="4b917-127">LOG de alterações \_ \_ ENTRYTYPES \_ ISNOTDIR \* \* (0x40000) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-127">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ISNOTDIR\*\* (0x40000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0x400_"></span><span id="change_log_entrytypes_mountcreate__0x400_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0X400_"></span><dt>

<span data-ttu-id="4b917-128">LOG de alterações \_ \_ ENTRYTYPES \_ MOUNTCREATE \* \* (0x400) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-128">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_MOUNTCREATE\*\* (0x400)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0x800_"></span><span id="change_log_entrytypes_mountdelete__0x800_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0X800_"></span><dt>

<span data-ttu-id="4b917-129">LOG de alterações \_ \_ ENTRYTYPES \_ MOUNTDELETE \* \* (0x800) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-129">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_MOUNTDELETE\*\* (0x800)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0x10000_"></span><span id="change_log_entrytypes_nooptimize__0x10000_"></span><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0X10000_"></span><dt>

<span data-ttu-id="4b917-130">ALTERAR \_ log \_ ENTRYTYPES \_ nooptimize \* \* (0x10000) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-130">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_NOOPTIMIZE\*\* (0x10000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0x200000_"></span><span id="change_log_entrytypes_openbyid__0x200000_"></span><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0X200000_"></span><dt>

<span data-ttu-id="4b917-131">LOG de alterações \_ \_ ENTRYTYPES \_ OPENBYID \* \* (0x200000) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-131">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_OPENBYID\*\* (0x200000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0x80000_"></span><span id="change_log_entrytypes_simulatedelete__0x80000_"></span><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0X80000_"></span><dt>

<span data-ttu-id="4b917-132">LOG de alterações \_ \_ ENTRYTYPES \_ SIMULATEDELETE \* \* (0x80000) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-132">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_SIMULATEDELETE\*\* (0x80000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0x1_"></span><span id="change_log_entrytypes_streamchange__0x1_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0X1_"></span><dt>

<span data-ttu-id="4b917-133">LOG de alterações \_ \_ ENTRYTYPES \_ STREAMCHANGE \* \* (0x1) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-133">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMCHANGE\*\* (0x1)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0x2000_"></span><span id="change_log_entrytypes_streamcreate__0x2000_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0X2000_"></span><dt>

<span data-ttu-id="4b917-134">LOG de alterações \_ \_ ENTRYTYPES \_ STREAMCREATE \* \* (0x2000) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-134">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMCREATE\*\* (0x2000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0x8_"></span><span id="change_log_entrytypes_streamoverwrite__0x8_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0X8_"></span><dt>

<span data-ttu-id="4b917-135">LOG de alterações \_ \_ ENTRYTYPES \_ STREAMOVERWRITE \* \* (0x8) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-135">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMOVERWRITE\*\* (0x8)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0x1000_"></span><span id="change_log_entrytypes_volumeerror__0x1000_"></span><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0X1000_"></span><dt>

<span data-ttu-id="4b917-136">LOG de alterações \_ \_ ENTRYTYPES \_ VOLUMEERROR \* \* (0x1000) \* \*</span><span class="sxs-lookup"><span data-stu-id="4b917-136">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_VOLUMEERROR\*\* (0x1000)\*\*</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="4b917-137">**dwEntryFlags**</span><span class="sxs-lookup"><span data-stu-id="4b917-137">**dwEntryFlags**</span></span>
</dt> <dd>

<span data-ttu-id="4b917-138">Esse membro pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="4b917-138">This member can be one of the following values:</span></span>

<dl><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0x4_"></span><span id="change_log_entryflags_aclinfo__0x4_"></span><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0X4_"></span><dt>

<span data-ttu-id="4b917-139">**\_ \_ \_ ACLINFO ENTRYFLAGS do log de alterações (0x4)**</span><span class="sxs-lookup"><span data-stu-id="4b917-139">**CHANGE\_LOG\_ENTRYFLAGS\_ACLINFO (0x4)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0x8_"></span><span id="change_log_entryflags_debuginfo__0x8_"></span><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0X8_"></span><dt>

<span data-ttu-id="4b917-140">**\_ \_ ENTRYFLAGS \_ DEBUGINFO (0x8) do log de alterações**</span><span class="sxs-lookup"><span data-stu-id="4b917-140">**CHANGE\_LOG\_ENTRYFLAGS\_DEBUGINFO (0x8)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0x2_"></span><span id="change_log_entryflags_secondpath__0x2_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0X2_"></span><dt>

<span data-ttu-id="4b917-141">**\_ \_ ENTRYFLAGS \_ SECONDPATH (0x2) do log de alterações**</span><span class="sxs-lookup"><span data-stu-id="4b917-141">**CHANGE\_LOG\_ENTRYFLAGS\_SECONDPATH (0x2)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0x10_"></span><span id="change_log_entryflags_shortname__0x10_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0X10_"></span><dt>

<span data-ttu-id="4b917-142">**\_ \_ ENTRYFLAGS do log \_ de alterações curtoname (0x10)**</span><span class="sxs-lookup"><span data-stu-id="4b917-142">**CHANGE\_LOG\_ENTRYFLAGS\_SHORTNAME (0x10)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0x1_"></span><span id="change_log_entryflags_temppath__0x1_"></span><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0X1_"></span><dt>

<span data-ttu-id="4b917-143">**\_ \_ ENTRYFLAGS \_ TEMPPATH (0x1) do log de alterações**</span><span class="sxs-lookup"><span data-stu-id="4b917-143">**CHANGE\_LOG\_ENTRYFLAGS\_TEMPPATH (0x1)**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="4b917-144">**dwAttributes**</span><span class="sxs-lookup"><span data-stu-id="4b917-144">**dwAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="4b917-145">Os atributos de arquivo do arquivo de log de alteração.</span><span class="sxs-lookup"><span data-stu-id="4b917-145">The file attributes of the change log file.</span></span> <span data-ttu-id="4b917-146">Se nenhum atributo for especificado, esse valor deverá ser definido como 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="4b917-146">If no attributes are specified, this value should be set to 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="4b917-147">**i64SequenceNum**</span><span class="sxs-lookup"><span data-stu-id="4b917-147">**i64SequenceNum**</span></span>
</dt> <dd>

<span data-ttu-id="4b917-148">O número de sequência atribuído à entrada do log de alterações.</span><span class="sxs-lookup"><span data-stu-id="4b917-148">The sequence number assigned to the change log entry.</span></span>

</dd> <dt>

<span data-ttu-id="4b917-149">**szProcName**</span><span class="sxs-lookup"><span data-stu-id="4b917-149">**szProcName**</span></span>
</dt> <dd>

<span data-ttu-id="4b917-150">O nome do processo que faz a alteração.</span><span class="sxs-lookup"><span data-stu-id="4b917-150">The name of the process making the change.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b917-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b917-151">Remarks</span></span>

<span data-ttu-id="4b917-152">Essa estrutura é seguida por um número variável de registros de dados de comprimento variável, além de um valor **DWORD** que deve ser idêntico ao valor do membro **dwRecordSize** de **RecordHeader**.</span><span class="sxs-lookup"><span data-stu-id="4b917-152">This structure is followed by a variable number of variable-length data records, plus a **DWORD** value that should be identical to the value of the **dwRecordSize** member of **RecordHeader**.</span></span>

<span data-ttu-id="4b917-153">Os registros de dados de comprimento variável consistem em uma estrutura de [**\_ cabeçalho de registro**](record-header.md) mais dados que podem ser usados para restaurar a entrada do log de alterações.</span><span class="sxs-lookup"><span data-stu-id="4b917-153">The variable-length data records consist of a [**RECORD\_HEADER**](record-header.md) structure plus data that can be used to restore the change log entry.</span></span> <span data-ttu-id="4b917-154">O formato dos dados depende do valor do membro **dwRecordType** da estrutura do cabeçalho do **registro \_** .</span><span class="sxs-lookup"><span data-stu-id="4b917-154">The format of the data depends on the value of the **dwRecordType** member of the **RECORD\_HEADER** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b917-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b917-155">Requirements</span></span>



| <span data-ttu-id="4b917-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b917-156">Requirement</span></span> | <span data-ttu-id="4b917-157">Valor</span><span class="sxs-lookup"><span data-stu-id="4b917-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4b917-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b917-158">Minimum supported client</span></span><br/> | <span data-ttu-id="4b917-159">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="4b917-159">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4b917-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b917-160">Minimum supported server</span></span><br/> | <span data-ttu-id="4b917-161">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4b917-161">None supported</span></span><br/>                            |
| <span data-ttu-id="4b917-162">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4b917-162">End of client support</span></span><br/>    | <span data-ttu-id="4b917-163">Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="4b917-163">Windows XP with SP2</span></span><br/>                       |



 

 





