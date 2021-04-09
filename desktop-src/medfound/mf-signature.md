---
description: Contém uma assinatura de GRL (lista de revogação global).
ms.assetid: 388a901c-6202-41cf-9c3d-f29d8ccca76b
title: Estrutura de MF_SIGNATURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_SIGNATURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4827fea8e4259609cbb54f2b58a3d1c88ad6c23e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171605"
---
# <a name="mf_signature-structure"></a><span data-ttu-id="6451e-103">\_Estrutura de assinatura MF</span><span class="sxs-lookup"><span data-stu-id="6451e-103">MF\_SIGNATURE structure</span></span>

<span data-ttu-id="6451e-104">Contém uma assinatura de GRL (lista de revogação global).</span><span class="sxs-lookup"><span data-stu-id="6451e-104">Contains a global revocation list (GRL) signature.</span></span>

## <a name="syntax"></a><span data-ttu-id="6451e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6451e-105">Syntax</span></span>


```C++
typedef struct _MF_SIGNATURE {
  DWORD dwSignVer;
  DWORD cbSign;
  BYTE  rgSign[1];
} MF_SIGNATURE;
```



## <a name="members"></a><span data-ttu-id="6451e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="6451e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6451e-107">**dwSignVer**</span><span class="sxs-lookup"><span data-stu-id="6451e-107">**dwSignVer**</span></span>
</dt> <dd>

<span data-ttu-id="6451e-108">O número de versão da assinatura.</span><span class="sxs-lookup"><span data-stu-id="6451e-108">The signature version number.</span></span>

</dd> <dt>

<span data-ttu-id="6451e-109">**cbSign**</span><span class="sxs-lookup"><span data-stu-id="6451e-109">**cbSign**</span></span>
</dt> <dd>

<span data-ttu-id="6451e-110">O tamanho da assinatura em bytes.</span><span class="sxs-lookup"><span data-stu-id="6451e-110">The size of the signature in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6451e-111">**rgSign**</span><span class="sxs-lookup"><span data-stu-id="6451e-111">**rgSign**</span></span>
</dt> <dd>

<span data-ttu-id="6451e-112">Uma matriz de bytes de tamanho **cbSign** que contém a assinatura.</span><span class="sxs-lookup"><span data-stu-id="6451e-112">A byte array of size **cbSign** that contains the signature.</span></span> <span data-ttu-id="6451e-113">O tamanho real da matriz é maior do que o tamanho fornecido na declaração de estrutura.</span><span class="sxs-lookup"><span data-stu-id="6451e-113">The actual array size is larger than the size given in the structure declaration.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6451e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6451e-114">Remarks</span></span>

<span data-ttu-id="6451e-115">Essa estrutura não é declarada em um cabeçalho do SDK.</span><span class="sxs-lookup"><span data-stu-id="6451e-115">This structure is not declared in an SDK header.</span></span> <span data-ttu-id="6451e-116">Para usar essa estrutura, adicione a declaração mostrada aqui ao seu código-fonte.</span><span class="sxs-lookup"><span data-stu-id="6451e-116">To use this structure, add the declaration shown here to your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6451e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6451e-117">Requirements</span></span>



| <span data-ttu-id="6451e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6451e-118">Requirement</span></span> | <span data-ttu-id="6451e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6451e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6451e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6451e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6451e-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6451e-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6451e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6451e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6451e-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6451e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6451e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="6451e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6451e-125">Revogação de certificado OPM</span><span class="sxs-lookup"><span data-stu-id="6451e-125">OPM Certificate Revocation</span></span>](opm-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="6451e-126">Estruturas OPM</span><span class="sxs-lookup"><span data-stu-id="6451e-126">OPM Structures</span></span>](opm-structures.md)
</dt> </dl>

 

 




