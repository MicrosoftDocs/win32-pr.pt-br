---
description: Contém informações sobre uma assinatura digital.
ms.assetid: 0b86fdf9-533f-4640-8c70-c3c8f4ef2c68
title: Estrutura de SIGNER_SIGNATURE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SIGNATURE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8e2b1fa68da51a649a01d4356ebfb1519ceeffb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169691"
---
# <a name="signer_signature_info-structure"></a><span data-ttu-id="58405-103">Estrutura de informações de \_ assinatura do assinante \_</span><span class="sxs-lookup"><span data-stu-id="58405-103">SIGNER\_SIGNATURE\_INFO structure</span></span>

<span data-ttu-id="58405-104">A estrutura de **\_ \_ informações de assinatura do assinante** contém informações sobre uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="58405-104">The **SIGNER\_SIGNATURE\_INFO** structure contains information about a digital signature.</span></span>

> [!Note]  
> <span data-ttu-id="58405-105">Essa estrutura não está definida em nenhum arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="58405-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="58405-106">Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.</span><span class="sxs-lookup"><span data-stu-id="58405-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="58405-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58405-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SIGNATURE_INFO {
  DWORD             cbSize;
  ALG_ID            algidHash;
  DWORD             dwAttrChoice;
  union {
    SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
  };
  PCRYPT_ATTRIBUTES psAuthenticated;
  PCRYPT_ATTRIBUTES psUnauthenticated;
} SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
```



## <a name="members"></a><span data-ttu-id="58405-108">Membros</span><span class="sxs-lookup"><span data-stu-id="58405-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="58405-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="58405-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="58405-110">O tamanho, em bytes, da estrutura.</span><span class="sxs-lookup"><span data-stu-id="58405-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="58405-111">**algidHash**</span><span class="sxs-lookup"><span data-stu-id="58405-111">**algidHash**</span></span>
</dt> <dd>

<span data-ttu-id="58405-112">O algoritmo de hash usado para a assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="58405-112">The hash algorithm used for the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="58405-113">**dwAttrChoice**</span><span class="sxs-lookup"><span data-stu-id="58405-113">**dwAttrChoice**</span></span>
</dt> <dd>

<span data-ttu-id="58405-114">Especifica se a assinatura tem atributos de [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="58405-114">Specifies whether the signature has [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span> <span data-ttu-id="58405-115">Esse membro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="58405-115">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="58405-116">Valor</span><span class="sxs-lookup"><span data-stu-id="58405-116">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="58405-117">Significado</span><span class="sxs-lookup"><span data-stu-id="58405-117">Meaning</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_AUTHCODE_ATTR"></span><span id="signer_authcode_attr"></span><dl> <span data-ttu-id="58405-118"><dt>**Signatário \_ FATORES \_ attr**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="58405-118"><dt>**SIGNER\_AUTHCODE\_ATTR**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="58405-119">A assinatura tem atributos de [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="58405-119">The signature has [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span><br/>           |
| <span id="SIGNER_NO_ATTR"></span><span id="signer_no_attr"></span><dl> <span data-ttu-id="58405-120"><dt>**Signatário \_ SEM \_ attr**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="58405-120"><dt>**SIGNER\_NO\_ATTR**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="58405-121">A assinatura não tem atributos de [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="58405-121">The signature does not have [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="58405-122">**pAttrAuthcode**</span><span class="sxs-lookup"><span data-stu-id="58405-122">**pAttrAuthcode**</span></span>
</dt> <dd>

<span data-ttu-id="58405-123">Especifica atributos para uma assinatura [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="58405-123">Specifies attributes for an [*Authenticode*](../secgloss/a-gly.md) signature.</span></span> <span data-ttu-id="58405-124">Esse membro será necessário se o valor do membro **dwAttrChoice** for **signatário \_ fatores \_ attr**.</span><span class="sxs-lookup"><span data-stu-id="58405-124">This member is required if the value of the **dwAttrChoice** member is **SIGNER\_AUTHCODE\_ATTR**.</span></span>

</dd> <dt>

<span data-ttu-id="58405-125">**psAuthenticated**</span><span class="sxs-lookup"><span data-stu-id="58405-125">**psAuthenticated**</span></span>
</dt> <dd>

<span data-ttu-id="58405-126">Atributos fornecidos pelo usuário autenticados adicionados à assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="58405-126">Authenticated user-supplied attributes added to the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="58405-127">**psUnauthenticated**</span><span class="sxs-lookup"><span data-stu-id="58405-127">**psUnauthenticated**</span></span>
</dt> <dd>

<span data-ttu-id="58405-128">Atributos fornecidos pelo usuário não autenticados adicionados à assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="58405-128">Unauthenticated user-supplied attributes added to the digital signature.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58405-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58405-129">Requirements</span></span>



| <span data-ttu-id="58405-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="58405-130">Requirement</span></span> | <span data-ttu-id="58405-131">Valor</span><span class="sxs-lookup"><span data-stu-id="58405-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="58405-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58405-132">Minimum supported client</span></span><br/> | <span data-ttu-id="58405-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="58405-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="58405-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58405-134">Minimum supported server</span></span><br/> | <span data-ttu-id="58405-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="58405-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58405-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="58405-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58405-137">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="58405-137">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="58405-138">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="58405-138">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
