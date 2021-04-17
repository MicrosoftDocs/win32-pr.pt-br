---
description: Especifica um assunto a ser assinado.
ms.assetid: ba569443-e50f-450b-82cc-b7328f0ca25a
title: Estrutura de SIGNER_SUBJECT_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SUBJECT_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05b5d780e50f8ea10fcf68cc90ae7092bbc2c473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811787"
---
# <a name="signer_subject_info-structure"></a><span data-ttu-id="a3928-103">Estrutura de informações de \_ assunto do assinante \_</span><span class="sxs-lookup"><span data-stu-id="a3928-103">SIGNER\_SUBJECT\_INFO structure</span></span>

<span data-ttu-id="a3928-104">A estrutura de **\_ \_ informações da entidade do assinante** especifica um assunto a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="a3928-104">The **SIGNER\_SUBJECT\_INFO** structure specifies a subject to sign.</span></span>

> [!Note]  
> <span data-ttu-id="a3928-105">Essa estrutura não está definida em nenhum arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="a3928-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="a3928-106">Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.</span><span class="sxs-lookup"><span data-stu-id="a3928-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a3928-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3928-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SUBJECT_INFO {
  DWORD cbSize;
  DWORD *pdwIndex;
  DWORD dwSubjectChoice;
  union {
    SIGNER_FILE_INFO *pSignerFileInfo;
    SIGNER_BLOB_INFO *pSignerBlobInfo;
  };
} SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
```



## <a name="members"></a><span data-ttu-id="a3928-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a3928-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a3928-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="a3928-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="a3928-110">O tamanho, em bytes, da estrutura.</span><span class="sxs-lookup"><span data-stu-id="a3928-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="a3928-111">**pdwIndex**</span><span class="sxs-lookup"><span data-stu-id="a3928-111">**pdwIndex**</span></span>
</dt> <dd>

<span data-ttu-id="a3928-112">Este membro está reservado.</span><span class="sxs-lookup"><span data-stu-id="a3928-112">This member is reserved.</span></span> <span data-ttu-id="a3928-113">Ele deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="a3928-113">It must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a3928-114">**dwSubjectChoice**</span><span class="sxs-lookup"><span data-stu-id="a3928-114">**dwSubjectChoice**</span></span>
</dt> <dd>

<span data-ttu-id="a3928-115">Especifica se o assunto é um arquivo ou um [*blob*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a3928-115">Specifies whether the subject is a file or a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="a3928-116">Esse membro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a3928-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="a3928-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a3928-117">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="a3928-118">Significado</span><span class="sxs-lookup"><span data-stu-id="a3928-118">Meaning</span></span>                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SIGNER_SUBJECT_BLOB"></span><span id="signer_subject_blob"></span><dl> <span data-ttu-id="a3928-119"><dt>**Signatário \_ \_Blob de assunto**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="a3928-119"><dt>**SIGNER\_SUBJECT\_BLOB**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="a3928-120">O assunto é um BLOB.</span><span class="sxs-lookup"><span data-stu-id="a3928-120">The subject is a BLOB.</span></span><br/> |
| <span id="SIGNER_SUBJECT_FILE"></span><span id="signer_subject_file"></span><dl> <span data-ttu-id="a3928-121"><dt>**Signatário \_ \_Arquivo de assunto**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="a3928-121"><dt>**SIGNER\_SUBJECT\_FILE**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="a3928-122">O assunto é um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a3928-122">The subject is a file.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a3928-123">**pSignerFileInfo**</span><span class="sxs-lookup"><span data-stu-id="a3928-123">**pSignerFileInfo**</span></span>
</dt> <dd>

<span data-ttu-id="a3928-124">Um ponteiro para uma estrutura de [**\_ \_ informações do arquivo de signatário**](signer-file-info.md) que especifica o arquivo a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="a3928-124">A pointer to a [**SIGNER\_FILE\_INFO**](signer-file-info.md) structure that specifies the file to sign.</span></span>

</dd> <dt>

<span data-ttu-id="a3928-125">**pSignerBlobInfo**</span><span class="sxs-lookup"><span data-stu-id="a3928-125">**pSignerBlobInfo**</span></span>
</dt> <dd>

<span data-ttu-id="a3928-126">Um ponteiro para uma estrutura de [**\_ \_ informações de blob de assinante**](signer-blob-info.md) que especifica o blob a assinar.</span><span class="sxs-lookup"><span data-stu-id="a3928-126">A pointer to a [**SIGNER\_BLOB\_INFO**](signer-blob-info.md) structure that specifies the BLOB to sign.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3928-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3928-127">Requirements</span></span>



| <span data-ttu-id="a3928-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3928-128">Requirement</span></span> | <span data-ttu-id="a3928-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a3928-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a3928-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3928-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a3928-131">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a3928-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a3928-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3928-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a3928-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a3928-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a3928-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3928-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3928-135">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="a3928-135">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="a3928-136">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="a3928-136">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
