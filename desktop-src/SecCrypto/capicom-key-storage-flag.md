---
description: A enumeração do sinalizador de armazenamento de chaves CAPICOM \_ \_ \_ Define sinalizadores de armazenamento de chaves.
ms.assetid: 326cef75-24a5-4dc9-a7e9-a63dd3d8de54
title: Enumeração de CAPICOM_KEY_STORAGE_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_STORAGE_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 9edbc3a5ac3396e528ebbb5390c4b07c24770e58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749886"
---
# <a name="capicom_key_storage_flag-enumeration"></a><span data-ttu-id="006f9-103">\_Enumeração de \_ sinalizador de armazenamento de chave CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="006f9-103">CAPICOM\_KEY\_STORAGE\_FLAG enumeration</span></span>

<span data-ttu-id="006f9-104">A enumeração do **\_ sinalizador de \_ armazenamento \_ de chaves CAPICOM** define sinalizadores de armazenamento de chaves.</span><span class="sxs-lookup"><span data-stu-id="006f9-104">The **CAPICOM\_KEY\_STORAGE\_FLAG** enumeration defines key storage flags.</span></span>

## <a name="members"></a><span data-ttu-id="006f9-105">Membros</span><span class="sxs-lookup"><span data-stu-id="006f9-105">Members</span></span>



| <span data-ttu-id="006f9-106">Membro</span><span class="sxs-lookup"><span data-stu-id="006f9-106">Member</span></span>                                     | <span data-ttu-id="006f9-107">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="006f9-107">Description</span></span>                           | <span data-ttu-id="006f9-108">Valor</span><span class="sxs-lookup"><span data-stu-id="006f9-108">Value</span></span> |
|--------------------------------------------|---------------------------------------|-------|
| <span data-ttu-id="006f9-109">**\_padrão de \_ armazenamento de chave CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="006f9-109">**CAPICOM\_KEY\_STORAGE\_DEFAULT**</span></span>         | <span data-ttu-id="006f9-110">Armazenamento de chaves padrão.</span><span class="sxs-lookup"><span data-stu-id="006f9-110">Default key storage.</span></span><br/>       | <span data-ttu-id="006f9-111">0</span><span class="sxs-lookup"><span data-stu-id="006f9-111">0</span></span>     |
| <span data-ttu-id="006f9-112">**o armazenamento de chaves capicor é \_ \_ \_ exportável**</span><span class="sxs-lookup"><span data-stu-id="006f9-112">**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</span></span>      | <span data-ttu-id="006f9-113">A chave é exportável.</span><span class="sxs-lookup"><span data-stu-id="006f9-113">The key is exportable.</span></span><br/>     | <span data-ttu-id="006f9-114">1</span><span class="sxs-lookup"><span data-stu-id="006f9-114">1</span></span>     |
| <span data-ttu-id="006f9-115">**CAPICOM de \_ armazenamento de chave \_ \_ \_ protegido pelo usuário**</span><span class="sxs-lookup"><span data-stu-id="006f9-115">**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</span></span> | <span data-ttu-id="006f9-116">A chave é protegida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="006f9-116">The key is user protected.</span></span><br/> | <span data-ttu-id="006f9-117">2</span><span class="sxs-lookup"><span data-stu-id="006f9-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="006f9-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="006f9-118">Remarks</span></span>

<span data-ttu-id="006f9-119">Essa enumeração é usada pelo seguinte método:</span><span class="sxs-lookup"><span data-stu-id="006f9-119">This enumeration is used by the following method:</span></span>

-   [<span data-ttu-id="006f9-120">**Certificado. Load**</span><span class="sxs-lookup"><span data-stu-id="006f9-120">**Certificate.Load**</span></span>](certificate-load.md)
-   [<span data-ttu-id="006f9-121">**Store. Load**</span><span class="sxs-lookup"><span data-stu-id="006f9-121">**Store.Load**</span></span>](store-load.md)

## <a name="requirements"></a><span data-ttu-id="006f9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="006f9-122">Requirements</span></span>



| <span data-ttu-id="006f9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="006f9-123">Requirement</span></span> | <span data-ttu-id="006f9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="006f9-124">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="006f9-125">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="006f9-125">Redistributable</span></span><br/> | <span data-ttu-id="006f9-126">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="006f9-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="006f9-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="006f9-127">Header</span></span><br/>          | <dl> <span data-ttu-id="006f9-128"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="006f9-128"><dt>Capicom.h</dt></span></span> </dl> |



 

 




