---
description: Especifica um BLOB a assinar.
ms.assetid: 214c9c05-5c95-4803-8993-23a87266f991
title: Estrutura de SIGNER_BLOB_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_BLOB_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: a05e99cc4d7fa2eff196159bb449fa7dbfbf3026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506273"
---
# <a name="signer_blob_info-structure"></a><span data-ttu-id="f80e5-103">Estrutura de informações de \_ blob do assinante \_</span><span class="sxs-lookup"><span data-stu-id="f80e5-103">SIGNER\_BLOB\_INFO structure</span></span>

<span data-ttu-id="f80e5-104">\[A estrutura de **\_ \_ informações de blob do assinante** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="f80e5-104">\[The **SIGNER\_BLOB\_INFO** structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f80e5-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="f80e5-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="f80e5-106">A estrutura de **\_ \_ informações de blob do assinante** especifica um [*blob*](../secgloss/b-gly.md) a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="f80e5-106">The **SIGNER\_BLOB\_INFO** structure specifies a [*BLOB*](../secgloss/b-gly.md) to sign.</span></span>

> [!Note]  
> <span data-ttu-id="f80e5-107">Essa estrutura não está definida em nenhum arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="f80e5-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="f80e5-108">Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.</span><span class="sxs-lookup"><span data-stu-id="f80e5-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f80e5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f80e5-109">Syntax</span></span>


```C++
typedef struct _SIGNER_BLOB_INFO {
  DWORD   cbSize;
  GUID    *pGuidSubject;
  DWORD   cbBlob;
  BYTE    *pbBlob;
  LPCWSTR pwszDisplayName;
} SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
```



## <a name="members"></a><span data-ttu-id="f80e5-110">Membros</span><span class="sxs-lookup"><span data-stu-id="f80e5-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="f80e5-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="f80e5-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="f80e5-112">O tamanho, em bytes, da estrutura.</span><span class="sxs-lookup"><span data-stu-id="f80e5-112">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="f80e5-113">**pGuidSubject**</span><span class="sxs-lookup"><span data-stu-id="f80e5-113">**pGuidSubject**</span></span>
</dt> <dd>

<span data-ttu-id="f80e5-114">Um ponteiro para um **GUID** que especifica o pacote de interface de entidade (SIP) a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="f80e5-114">A pointer to a **GUID** that specifies the Subject Interface Package (SIP) to load.</span></span>

</dd> <dt>

<span data-ttu-id="f80e5-115">**cbBlob**</span><span class="sxs-lookup"><span data-stu-id="f80e5-115">**cbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="f80e5-116">O tamanho, em bytes, do BLOB a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="f80e5-116">The size, in bytes, of the BLOB to sign.</span></span>

</dd> <dt>

<span data-ttu-id="f80e5-117">**pbBlob**</span><span class="sxs-lookup"><span data-stu-id="f80e5-117">**pbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="f80e5-118">Um ponteiro para o BLOB a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="f80e5-118">A pointer to the BLOB to sign.</span></span>

</dd> <dt>

<span data-ttu-id="f80e5-119">**pwszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="f80e5-119">**pwszDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="f80e5-120">O nome de exibição do BLOB.</span><span class="sxs-lookup"><span data-stu-id="f80e5-120">The display name of the BLOB.</span></span> <span data-ttu-id="f80e5-121">Esse membro pode ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f80e5-121">This member can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f80e5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f80e5-122">Requirements</span></span>



| <span data-ttu-id="f80e5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f80e5-123">Requirement</span></span> | <span data-ttu-id="f80e5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f80e5-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f80e5-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f80e5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f80e5-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f80e5-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f80e5-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f80e5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f80e5-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f80e5-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f80e5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f80e5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f80e5-130">**\_informações de assunto do assinante \_**</span><span class="sxs-lookup"><span data-stu-id="f80e5-130">**SIGNER\_SUBJECT\_INFO**</span></span>](signer-subject-info.md)
</dt> </dl>

 

 
