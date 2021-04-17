---
description: Indica o que é verificado quando uma assinatura digital é verificada.
ms.assetid: e6259c3f-caed-42f4-832c-250365caa0d7
title: Enumeração de CAPICOM_SIGNED_DATA_VERIFY_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_SIGNED_DATA_VERIFY_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bc8db48ee067e8d12bffa9dbff433384058013b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769290"
---
# <a name="capicom_signed_data_verify_flag-enumeration"></a><span data-ttu-id="b0b99-103">\_Enumeração de \_ \_ sinalizador de verificação de dados ASSINADOs CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="b0b99-103">CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG enumeration</span></span>

<span data-ttu-id="b0b99-104">A **enumeração \_ \_ sinalizador de \_ verificação \_ de dados assinados de capicor** indica o que é verificado quando uma [*assinatura digital*](../secgloss/d-gly.md) é verificada.</span><span class="sxs-lookup"><span data-stu-id="b0b99-104">The **CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG** enumeration indicates what is checked when a [*digital signature*](../secgloss/d-gly.md) is verified.</span></span>

## <a name="members"></a><span data-ttu-id="b0b99-105">Membros</span><span class="sxs-lookup"><span data-stu-id="b0b99-105">Members</span></span>



| <span data-ttu-id="b0b99-106">Membro</span><span class="sxs-lookup"><span data-stu-id="b0b99-106">Member</span></span>                                           | <span data-ttu-id="b0b99-107">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="b0b99-107">Description</span></span>                                                                                                 | <span data-ttu-id="b0b99-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b0b99-108">Value</span></span> |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="b0b99-109">**CAPICOM \_ verificar \_ \_ somente assinatura**</span><span class="sxs-lookup"><span data-stu-id="b0b99-109">**CAPICOM\_VERIFY\_SIGNATURE\_ONLY**</span></span>             | <span data-ttu-id="b0b99-110">Somente a assinatura é verificada.</span><span class="sxs-lookup"><span data-stu-id="b0b99-110">Only the signature is checked.</span></span><br/>                                                                   | <span data-ttu-id="b0b99-111">0</span><span class="sxs-lookup"><span data-stu-id="b0b99-111">0</span></span>     |
| <span data-ttu-id="b0b99-112">**CAPICOM \_ verificar \_ assinatura \_ e \_ certificado**</span><span class="sxs-lookup"><span data-stu-id="b0b99-112">**CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE**</span></span> | <span data-ttu-id="b0b99-113">A assinatura e a validade do certificado usado para criar a assinatura são verificadas.</span><span class="sxs-lookup"><span data-stu-id="b0b99-113">Both the signature and the validity of the certificate used to create the signature are checked.</span></span><br/> | <span data-ttu-id="b0b99-114">1</span><span class="sxs-lookup"><span data-stu-id="b0b99-114">1</span></span>     |



## <a name="requirements"></a><span data-ttu-id="b0b99-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0b99-115">Requirements</span></span>



| <span data-ttu-id="b0b99-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0b99-116">Requirement</span></span> | <span data-ttu-id="b0b99-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b0b99-117">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b99-118">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="b0b99-118">Redistributable</span></span><br/> | <span data-ttu-id="b0b99-119">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="b0b99-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="b0b99-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0b99-120">Header</span></span><br/>          | <dl> <span data-ttu-id="b0b99-121"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0b99-121"><dt>Capicom.h</dt></span></span> </dl> |



 

 
