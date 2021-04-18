---
description: O tipo de enumeração de sinalizador de exportação de CAPICOM \_ \_ define se erros de exportação de chave privada são ignorados.
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: Enumeração de CAPICOM_EXPORT_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EXPORT_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: fe99b1123ae35083e5c59df37234821efd2db208
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787462"
---
# <a name="capicom_export_flag-enumeration"></a><span data-ttu-id="859eb-103">Enumeração de sinalizador de \_ exportação de CApicom \_</span><span class="sxs-lookup"><span data-stu-id="859eb-103">CAPICOM\_EXPORT\_FLAG enumeration</span></span>

<span data-ttu-id="859eb-104">O tipo de enumeração de **\_ \_ sinalizador de exportação de CAPICOM** define se erros de exportação de chave privada são ignorados.</span><span class="sxs-lookup"><span data-stu-id="859eb-104">The **CAPICOM\_EXPORT\_FLAG** enumeration type defines whether any private key export errors are ignored.</span></span>

## <a name="members"></a><span data-ttu-id="859eb-105">Membros</span><span class="sxs-lookup"><span data-stu-id="859eb-105">Members</span></span>



| <span data-ttu-id="859eb-106">Membro</span><span class="sxs-lookup"><span data-stu-id="859eb-106">Member</span></span>                                                            | <span data-ttu-id="859eb-107">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="859eb-107">Description</span></span>                                               | <span data-ttu-id="859eb-108">Valor</span><span class="sxs-lookup"><span data-stu-id="859eb-108">Value</span></span> |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| <span data-ttu-id="859eb-109">**\_padrão de exportação de CApicom \_**</span><span class="sxs-lookup"><span data-stu-id="859eb-109">**CAPICOM\_EXPORT\_DEFAULT**</span></span>                                      | <span data-ttu-id="859eb-110">Os erros de exportação de chave privada não são ignorados.</span><span class="sxs-lookup"><span data-stu-id="859eb-110">Any private key export errors are not ignored.</span></span><br/> | <span data-ttu-id="859eb-111">0</span><span class="sxs-lookup"><span data-stu-id="859eb-111">0</span></span>     |
| <span data-ttu-id="859eb-112">**\_erro de exportação para \_ ignorar \_ \_ chave privada \_ não \_ exportável \_ do CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="859eb-112">**CAPICOM\_EXPORT\_IGNORE\_PRIVATE\_KEY\_NOT\_EXPORTABLE\_ERROR**</span></span> | <span data-ttu-id="859eb-113">Os erros de exportação de chave privada são ignorados.</span><span class="sxs-lookup"><span data-stu-id="859eb-113">Any private key export errors are ignored.</span></span><br/>     | <span data-ttu-id="859eb-114">1</span><span class="sxs-lookup"><span data-stu-id="859eb-114">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="859eb-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="859eb-115">Remarks</span></span>

<span data-ttu-id="859eb-116">O tipo de enumeração do sinalizador de exportação capicor \_ \_ é usado pelo seguinte método:</span><span class="sxs-lookup"><span data-stu-id="859eb-116">The CAPICOM\_EXPORT\_FLAG enumeration type is used by the following method:</span></span>

-   [<span data-ttu-id="859eb-117">**Certificados. salvar**</span><span class="sxs-lookup"><span data-stu-id="859eb-117">**Certificates.Save**</span></span>](certificates-save.md)

## <a name="requirements"></a><span data-ttu-id="859eb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="859eb-118">Requirements</span></span>



| <span data-ttu-id="859eb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="859eb-119">Requirement</span></span> | <span data-ttu-id="859eb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="859eb-120">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="859eb-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="859eb-121">Redistributable</span></span><br/> | <span data-ttu-id="859eb-122">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="859eb-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="859eb-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="859eb-123">Header</span></span><br/>          | <dl> <span data-ttu-id="859eb-124"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="859eb-124"><dt>Capicom.h</dt></span></span> </dl> |



 

 




