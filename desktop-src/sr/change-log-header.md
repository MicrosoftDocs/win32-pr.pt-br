---
title: Estrutura de CHANGE_LOG_HEADER
description: O cabeçalho do log de alterações.
ms.assetid: 24fee9a5-b073-474f-afd5-d81f66399936
keywords:
- Restauração do sistema de estrutura CHANGE_LOG_HEADER
- Restauração do sistema de ponteiro de estrutura de PCHANGE_LOG_HEADER
topic_type:
- apiref
api_name:
- CHANGE_LOG_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5512ff9c9e708095f38e3ae1dcf80ce2e0e4443b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369284"
---
# <a name="change_log_header-structure"></a><span data-ttu-id="2c23e-105">ALTERAR \_ a \_ estrutura do cabeçalho do log</span><span class="sxs-lookup"><span data-stu-id="2c23e-105">CHANGE\_LOG\_HEADER structure</span></span>

<span data-ttu-id="2c23e-106">\[Essas informações se aplicam somente ao Windows XP com Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="2c23e-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="2c23e-107">O cabeçalho do log de alterações.</span><span class="sxs-lookup"><span data-stu-id="2c23e-107">The change log header.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c23e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c23e-108">Syntax</span></span>


```C++
typedef struct _CHANGE_LOG_HEADER {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwLogVersion;
  RECORD_HEADER DataHeader;
  BYTE          byteData[1];
} CHANGE_LOG_HEADER, *PCHANGE_LOG_HEADER;
```



## <a name="members"></a><span data-ttu-id="2c23e-109">Membros</span><span class="sxs-lookup"><span data-stu-id="2c23e-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="2c23e-110">**RecordHeader**</span><span class="sxs-lookup"><span data-stu-id="2c23e-110">**RecordHeader**</span></span>
</dt> <dd>

<span data-ttu-id="2c23e-111">Uma estrutura de [**\_ cabeçalho de registro**](record-header.md) .</span><span class="sxs-lookup"><span data-stu-id="2c23e-111">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="2c23e-112">O membro **dwRecordType** deve ser definido como RecordTypeLogHeader (0).</span><span class="sxs-lookup"><span data-stu-id="2c23e-112">The **dwRecordType** member should be set to RecordTypeLogHeader (0).</span></span> <span data-ttu-id="2c23e-113">O membro **dwRecordSize** deve considerar todos os membros, mais o valor **DWORD** extra que segue esse cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="2c23e-113">The **dwRecordSize** member should account for all the members, plus the extra **DWORD** value that follows this header.</span></span> <span data-ttu-id="2c23e-114">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="2c23e-114">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2c23e-115">**dwMagicNum**</span><span class="sxs-lookup"><span data-stu-id="2c23e-115">**dwMagicNum**</span></span>
</dt> <dd>

<span data-ttu-id="2c23e-116">Esse membro deve ser definido como 0xabcdef12.</span><span class="sxs-lookup"><span data-stu-id="2c23e-116">This member should be set to 0xabcdef12.</span></span>

</dd> <dt>

<span data-ttu-id="2c23e-117">**dwLogVersion**</span><span class="sxs-lookup"><span data-stu-id="2c23e-117">**dwLogVersion**</span></span>
</dt> <dd>

<span data-ttu-id="2c23e-118">Esse membro deve ser definido como 2.</span><span class="sxs-lookup"><span data-stu-id="2c23e-118">This member should be set to 2.</span></span>

</dd> <dt>

<span data-ttu-id="2c23e-119">**Dataheader**</span><span class="sxs-lookup"><span data-stu-id="2c23e-119">**DataHeader**</span></span>
</dt> <dd>

<span data-ttu-id="2c23e-120">Uma estrutura de [**\_ cabeçalho de registro**](record-header.md) .</span><span class="sxs-lookup"><span data-stu-id="2c23e-120">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="2c23e-121">O membro **dwRecordType** deve ser definido como **RecordTypeVolumePath** (2).</span><span class="sxs-lookup"><span data-stu-id="2c23e-121">The **dwRecordType** member should be set to **RecordTypeVolumePath** (2).</span></span>

</dd> <dt>

<span data-ttu-id="2c23e-122">**byteData**</span><span class="sxs-lookup"><span data-stu-id="2c23e-122">**byteData**</span></span>
</dt> <dd>

<span data-ttu-id="2c23e-123">O início de uma cadeia de caracteres terminada em nulo que especifica o caminho do volume.</span><span class="sxs-lookup"><span data-stu-id="2c23e-123">The start of a null-terminated string that specifies the volume path.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c23e-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c23e-124">Remarks</span></span>

<span data-ttu-id="2c23e-125">Esse cabeçalho é seguido por um valor **DWORD** que deve ser idêntico ao valor do membro **dwRecordSize** de **RecordHeader**.</span><span class="sxs-lookup"><span data-stu-id="2c23e-125">This header is followed by a **DWORD** value that should be identical to the value of the **dwRecordSize** member of **RecordHeader**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c23e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c23e-126">Requirements</span></span>



| <span data-ttu-id="2c23e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c23e-127">Requirement</span></span> | <span data-ttu-id="2c23e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="2c23e-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2c23e-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c23e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2c23e-130">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="2c23e-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2c23e-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c23e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2c23e-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2c23e-132">None supported</span></span><br/>                            |
| <span data-ttu-id="2c23e-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2c23e-133">End of client support</span></span><br/>    | <span data-ttu-id="2c23e-134">Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="2c23e-134">Windows XP with SP2</span></span><br/>                       |



 

 





