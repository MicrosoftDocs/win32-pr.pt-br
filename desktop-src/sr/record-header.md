---
title: Estrutura de RECORD_HEADER
description: O cabeçalho de registro usado pela entrada de log de alteração \_ e as \_ estruturas de cabeçalho de log de alteração \_ \_ .
ms.assetid: f8d2147c-ad13-4be4-94d7-ae0ca26511da
keywords:
- Restauração do sistema de estrutura RECORD_HEADER
- Restauração do sistema de ponteiro de estrutura de PRECORD_HEADER
topic_type:
- apiref
api_name:
- RECORD_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2fd304d2f1b6a5ece08d3d3535aacd7a1abcf614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455671"
---
# <a name="record_header-structure"></a><span data-ttu-id="9dc3a-105">Estrutura do cabeçalho do registro \_</span><span class="sxs-lookup"><span data-stu-id="9dc3a-105">RECORD\_HEADER structure</span></span>

<span data-ttu-id="9dc3a-106">\[Essas informações se aplicam somente ao Windows XP com Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="9dc3a-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="9dc3a-107">O cabeçalho de registro usado pela [**\_ \_ entrada de log de alteração**](change-log-entry.md) e as estruturas de [**\_ \_ cabeçalho de log de alteração**](change-log-header.md) .</span><span class="sxs-lookup"><span data-stu-id="9dc3a-107">The record header used by the [**CHANGE\_LOG\_ENTRY**](change-log-entry.md) and [**CHANGE\_LOG\_HEADER**](change-log-header.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dc3a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9dc3a-108">Syntax</span></span>


```C++
typedef struct _RECORD_HEADER {
  DWORD dwRecordSize;
  DWORD dwRecordType;
} RECORD_HEADER, *PRECORD_HEADER;
```



## <a name="members"></a><span data-ttu-id="9dc3a-109">Membros</span><span class="sxs-lookup"><span data-stu-id="9dc3a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="9dc3a-110">**dwRecordSize**</span><span class="sxs-lookup"><span data-stu-id="9dc3a-110">**dwRecordSize**</span></span>
</dt> <dd>

<span data-ttu-id="9dc3a-111">O tamanho total do registro, incluindo o cabeçalho, em bytes.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-111">The total size of the record, including the header, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9dc3a-112">**dwRecordType**</span><span class="sxs-lookup"><span data-stu-id="9dc3a-112">**dwRecordType**</span></span>
</dt> <dd>

<span data-ttu-id="9dc3a-113">O tipo de registro.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-113">The record type.</span></span> <span data-ttu-id="9dc3a-114">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-114">This member may be one of the following values.</span></span>



| <span data-ttu-id="9dc3a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9dc3a-115">Value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="9dc3a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="9dc3a-116">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RecordTypeLogHeader"></span><span id="recordtypelogheader"></span><span id="RECORDTYPELOGHEADER"></span><dl> <span data-ttu-id="9dc3a-117"><dt>**RecordTypeLogHeader**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9dc3a-117"><dt>**RecordTypeLogHeader**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="9dc3a-118">O registro é o cabeçalho do log de alterações.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-118">The record is the header for the change log.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="RecordTypeLogEntry"></span><span id="recordtypelogentry"></span><span id="RECORDTYPELOGENTRY"></span><dl> <span data-ttu-id="9dc3a-119"><dt>**RecordTypeLogEntry**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9dc3a-119"><dt>**RecordTypeLogEntry**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="9dc3a-120">O registro é o cabeçalho de uma entrada de log de alterações.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-120">The record is the header for a change log entry.</span></span><br/>                                                                                                                                                                                                                        |
| <span id="RecordTypeVolumePath"></span><span id="recordtypevolumepath"></span><span id="RECORDTYPEVOLUMEPATH"></span><dl> <span data-ttu-id="9dc3a-121"><dt>**RecordTypeVolumePath**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9dc3a-121"><dt>**RecordTypeVolumePath**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="9dc3a-122">Os dados são o caminho do volume para a entrada do log de alterações.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-122">The data is the volume path for the change log entry.</span></span><br/>                                                                                                                                                                                                                   |
| <span id="RecordTypeFirstPath"></span><span id="recordtypefirstpath"></span><span id="RECORDTYPEFIRSTPATH"></span><dl> <span data-ttu-id="9dc3a-123"><dt>**RecordTypeFirstPath**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9dc3a-123"><dt>**RecordTypeFirstPath**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="9dc3a-124">Os dados são o caminho do arquivo para a entrada do log de alterações.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-124">The data is the file path for the change log entry.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="RecordTypeSecondPath"></span><span id="recordtypesecondpath"></span><span id="RECORDTYPESECONDPATH"></span><dl> <span data-ttu-id="9dc3a-125"><dt>**RecordTypeSecondPath**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9dc3a-125"><dt>**RecordTypeSecondPath**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="9dc3a-126">Os dados são usados ao renomear as entradas do log de alterações; esse caminho é onde o arquivo renomeado é armazenado.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-126">The data is used when renaming change log entries; this path is where the renamed file is stored.</span></span><br/>                                                                                                                                                                       |
| <span id="RecordTypeTempPath"></span><span id="recordtypetemppath"></span><span id="RECORDTYPETEMPPATH"></span><dl> <span data-ttu-id="9dc3a-127"><dt>**RecordTypeTempPath**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9dc3a-127"><dt>**RecordTypeTempPath**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="9dc3a-128">Os dados são o nome do arquivo de backup usado para restaurar a entrada do log de alterações.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-128">The data is the name of the backup file used to restore the change log entry.</span></span> <span data-ttu-id="9dc3a-129">Os arquivos de backup estão localizados na pasta RP *n* .</span><span class="sxs-lookup"><span data-stu-id="9dc3a-129">The backup files are located in the RP *n* folder.</span></span> <span data-ttu-id="9dc3a-130">O nome do arquivo tem o seguinte formato: um *xxxxxxx*. *ext*, em que *xxxxxxx* é um número de sete dígitos e *ext* é a extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-130">The file name has the following format: A *xxxxxxx*.*ext*, where *xxxxxxx* is a seven-digit number and *ext* is the file name extension.</span></span><br/> |
| <span id="RecordTypeAclInline"></span><span id="recordtypeaclinline"></span><span id="RECORDTYPEACLINLINE"></span><dl> <span data-ttu-id="9dc3a-131"><dt>**RecordTypeAclInline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9dc3a-131"><dt>**RecordTypeAclInline**</dt> <dt>6</dt></span></span> </dl>     | <span data-ttu-id="9dc3a-132">Os dados são uma ACL.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-132">The data is an ACL.</span></span> <span data-ttu-id="9dc3a-133">O formato de dados é uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="9dc3a-133">The data format is a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure.</span></span> <br/> <span data-ttu-id="9dc3a-134">Esse valor não pode ser maior que 8.192 bytes.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-134">This value cannot be larger than 8,192 bytes.</span></span> <span data-ttu-id="9dc3a-135">Para especificar um valor maior que 8.192 bytes, use o membro **RecordTypeAclFile** .</span><span class="sxs-lookup"><span data-stu-id="9dc3a-135">To specify a value larger than 8,192 bytes, use the **RecordTypeAclFile** member.</span></span><br/>                |
| <span id="RecordTypeAclFile"></span><span id="recordtypeaclfile"></span><span id="RECORDTYPEACLFILE"></span><dl> <span data-ttu-id="9dc3a-136"><dt>**RecordTypeAclFile**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9dc3a-136"><dt>**RecordTypeAclFile**</dt> <dt>7</dt></span></span> </dl>             | <span data-ttu-id="9dc3a-137">Os dados são o nome do arquivo ACL usado para armazenar a ACL.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-137">The data is the name of the ACL file used to store the ACL.</span></span> <span data-ttu-id="9dc3a-138">Os arquivos ACL estão localizados na pasta RP *n* .</span><span class="sxs-lookup"><span data-stu-id="9dc3a-138">The ACL files are located in the RP *n* folder.</span></span> <span data-ttu-id="9dc3a-139">O nome do arquivo tem o seguinte formato: S *xxxxxxx*. ACL, em que *xxxxxxx* é um número de sete dígitos.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-139">The file name has the following format: S *xxxxxxx*.acl, where *xxxxxxx* is a seven-digit number.</span></span><br/>                                                             |
| <span id="RecordTypeDebugInfo"></span><span id="recordtypedebuginfo"></span><span id="RECORDTYPEDEBUGINFO"></span><dl> <span data-ttu-id="9dc3a-140"><dt>**RecordTypeDebugInfo**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9dc3a-140"><dt>**RecordTypeDebugInfo**</dt> <dt>8</dt></span></span> </dl>     | <span data-ttu-id="9dc3a-141">Os dados são informações de depuração para a entrada do log de alterações.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-141">The data is debug information for the change log entry.</span></span> <span data-ttu-id="9dc3a-142">O formato de dados é uma estrutura de **informações de depuração de log do Sr \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="9dc3a-142">The data format is a **SR\_LOG\_DEBUG\_INFO** structure.</span></span> <span data-ttu-id="9dc3a-143">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-143">For more information, see Remarks.</span></span><br/>                                                                                                                     |
| <span id="RecordTypeShortName"></span><span id="recordtypeshortname"></span><span id="RECORDTYPESHORTNAME"></span><dl> <span data-ttu-id="9dc3a-144"><dt>**RecordTypeShortName**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9dc3a-144"><dt>**RecordTypeShortName**</dt> <dt>9</dt></span></span> </dl>     | <span data-ttu-id="9dc3a-145">Os dados são o nome curto do arquivo de backup.</span><span class="sxs-lookup"><span data-stu-id="9dc3a-145">The data is the short name of the backup file.</span></span><br/>                                                                                                                                                                                                                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9dc3a-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="9dc3a-146">Remarks</span></span>

<span data-ttu-id="9dc3a-147">A estrutura de informações de depuração do log do Sr é definida da seguinte maneira. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9dc3a-147">The **SR\_LOG\_DEBUG\_INFO** structure is defined as follows.</span></span>

``` syntax
typedef struct _SR_LOG_DEBUG_INFO {
    RECORD_HEADER Header;         // log entry header
    HANDLE ThreadId;              // thread identifier
    HANDLE ProcessId;             // process identifier
    ULARGER_INTEGER TimeStamp;    // event time stamp
    CHAR ProcesName[13];          // process name
} SR_LOG_DEBUG_INFO, *PSR_LOG_DEBUG_INFO;
```

## <a name="requirements"></a><span data-ttu-id="9dc3a-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dc3a-148">Requirements</span></span>



| <span data-ttu-id="9dc3a-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dc3a-149">Requirement</span></span> | <span data-ttu-id="9dc3a-150">Valor</span><span class="sxs-lookup"><span data-stu-id="9dc3a-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9dc3a-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9dc3a-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9dc3a-152">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="9dc3a-152">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9dc3a-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9dc3a-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9dc3a-154">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9dc3a-154">None supported</span></span><br/>                            |
| <span data-ttu-id="9dc3a-155">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="9dc3a-155">End of client support</span></span><br/>    | <span data-ttu-id="9dc3a-156">Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="9dc3a-156">Windows XP with SP2</span></span><br/>                       |



 

