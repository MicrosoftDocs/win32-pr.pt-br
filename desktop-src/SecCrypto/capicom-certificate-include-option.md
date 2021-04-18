---
description: Define quais certificados em uma cadeia são salvos.
ms.assetid: 6f9e28e6-b01f-4803-8259-8ab73abeecf8
title: Enumeração de CAPICOM_CERTIFICATE_INCLUDE_OPTION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_INCLUDE_OPTION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 45ea9ccf7d3a43e325073f04e28bbd392fa34998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771815"
---
# <a name="capicom_certificate_include_option-enumeration"></a><span data-ttu-id="0c2a2-103">O certificado CAPICOM \_ \_ inclui a enumeração de \_ opção</span><span class="sxs-lookup"><span data-stu-id="0c2a2-103">CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION enumeration</span></span>

<span data-ttu-id="0c2a2-104">O tipo de enumeração de **\_ \_ \_ opção do certificado CAPICOM** define quais certificados em uma cadeia são salvos.</span><span class="sxs-lookup"><span data-stu-id="0c2a2-104">The **CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION** enumeration type defines which certificates in a chain are saved.</span></span> <span data-ttu-id="0c2a2-105">Esse tipo de enumeração foi introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="0c2a2-105">This enumeration type was introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="0c2a2-106">Membros</span><span class="sxs-lookup"><span data-stu-id="0c2a2-106">Members</span></span>



| <span data-ttu-id="0c2a2-107">Membro</span><span class="sxs-lookup"><span data-stu-id="0c2a2-107">Member</span></span>                                                 | <span data-ttu-id="0c2a2-108">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="0c2a2-108">Description</span></span>                                                                           | <span data-ttu-id="0c2a2-109">Valor</span><span class="sxs-lookup"><span data-stu-id="0c2a2-109">Value</span></span> |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="0c2a2-110">**CAPICOM de certificado de caissor \_ \_ \_ \_ , exceto \_ raiz**</span><span class="sxs-lookup"><span data-stu-id="0c2a2-110">**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</span></span> | <span data-ttu-id="0c2a2-111">Salva todos os certificados na cadeia com a exceção da entidade raiz.</span><span class="sxs-lookup"><span data-stu-id="0c2a2-111">Saves all certificates in the chain with the exception of the root entity.</span></span><br/> | <span data-ttu-id="0c2a2-112">0</span><span class="sxs-lookup"><span data-stu-id="0c2a2-112">0</span></span>     |
| <span data-ttu-id="0c2a2-113">**certificado CAPICOM \_ \_ incluir \_ \_ cadeia inteira**</span><span class="sxs-lookup"><span data-stu-id="0c2a2-113">**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</span></span>        | <span data-ttu-id="0c2a2-114">Salva a cadeia de certificados completa.</span><span class="sxs-lookup"><span data-stu-id="0c2a2-114">Saves the complete certificate chain.</span></span><br/>                                      | <span data-ttu-id="0c2a2-115">1</span><span class="sxs-lookup"><span data-stu-id="0c2a2-115">1</span></span>     |
| <span data-ttu-id="0c2a2-116">**o certificado CAPICOM \_ \_ inclui \_ \_ somente entidade final \_**</span><span class="sxs-lookup"><span data-stu-id="0c2a2-116">**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</span></span>   | <span data-ttu-id="0c2a2-117">Salva apenas o certificado de entidade final.</span><span class="sxs-lookup"><span data-stu-id="0c2a2-117">Saves only the end entity certificate.</span></span><br/>                                     | <span data-ttu-id="0c2a2-118">2</span><span class="sxs-lookup"><span data-stu-id="0c2a2-118">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="0c2a2-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c2a2-119">Remarks</span></span>

<span data-ttu-id="0c2a2-120">O tipo de enumeração de **\_ \_ \_ opção do certificado CAPICOM** é usado pelo método [**Certificate. Save**](certificate-save.md) .</span><span class="sxs-lookup"><span data-stu-id="0c2a2-120">The **CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION** enumeration type is used by the [**Certificate.Save**](certificate-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c2a2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c2a2-121">Requirements</span></span>



| <span data-ttu-id="0c2a2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c2a2-122">Requirement</span></span> | <span data-ttu-id="0c2a2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0c2a2-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0c2a2-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="0c2a2-124">Redistributable</span></span><br/> | <span data-ttu-id="0c2a2-125">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c2a2-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="0c2a2-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c2a2-126">Header</span></span><br/>          | <dl> <span data-ttu-id="0c2a2-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c2a2-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 




