---
description: Define o formato de um arquivo que contém informações de certificados.
ms.assetid: 2118746a-9fa4-4e6a-82ce-e57f154f4a94
title: Enumeração de CAPICOM_CERTIFICATES_SAVE_AS_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATES_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 3cbde0e8a64fa931ce50d2277d33b5fd5c27ee68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756562"
---
# <a name="capicom_certificates_save_as_type-enumeration"></a><span data-ttu-id="b89ef-103">\_Enumeração de certificados de CApicom \_ \_ de gravação como \_ tipo</span><span class="sxs-lookup"><span data-stu-id="b89ef-103">CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE enumeration</span></span>

<span data-ttu-id="b89ef-104">O tipo de enumeração **\_ \_ Salvar \_ \_ como certificado de CAPICOM certificados** define o formato de um arquivo que contém informações de certificados.</span><span class="sxs-lookup"><span data-stu-id="b89ef-104">The **CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE** enumeration type defines the format of a file containing certificates information.</span></span> <span data-ttu-id="b89ef-105">Esse tipo de enumeração foi introduzido pelo CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="b89ef-105">This enumeration type was introduced by CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="b89ef-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b89ef-106">Members</span></span>



| <span data-ttu-id="b89ef-107">Membro</span><span class="sxs-lookup"><span data-stu-id="b89ef-107">Member</span></span>                                          | <span data-ttu-id="b89ef-108">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="b89ef-108">Description</span></span>                                          | <span data-ttu-id="b89ef-109">Valor</span><span class="sxs-lookup"><span data-stu-id="b89ef-109">Value</span></span> |
|-------------------------------------------------|------------------------------------------------------|-------|
| <span data-ttu-id="b89ef-110">**os certificados CAPICOM \_ \_ Salvar \_ como \_ serializado**</span><span class="sxs-lookup"><span data-stu-id="b89ef-110">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_SERIALIZED**</span></span> | <span data-ttu-id="b89ef-111">Os certificados salvos são serializados.</span><span class="sxs-lookup"><span data-stu-id="b89ef-111">The saved certificates are serialized.</span></span><br/>    | <span data-ttu-id="b89ef-112">0</span><span class="sxs-lookup"><span data-stu-id="b89ef-112">0</span></span>     |
| <span data-ttu-id="b89ef-113">**Os certificados CAPICOM \_ \_ Save \_ as \_ PKCS7**</span><span class="sxs-lookup"><span data-stu-id="b89ef-113">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PKCS7**</span></span>      | <span data-ttu-id="b89ef-114">Os certificados são salvos como um PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="b89ef-114">The certificates are saved as a PKCS \#7.</span></span><br/> | <span data-ttu-id="b89ef-115">1</span><span class="sxs-lookup"><span data-stu-id="b89ef-115">1</span></span>     |
| <span data-ttu-id="b89ef-116">**os certificados CAPICOM \_ \_ Salvar \_ como \_ pfx**</span><span class="sxs-lookup"><span data-stu-id="b89ef-116">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX**</span></span>        | <span data-ttu-id="b89ef-117">Os certificados são salvos como um PFX.</span><span class="sxs-lookup"><span data-stu-id="b89ef-117">The certificates are saved as a PFX.</span></span><br/>      | <span data-ttu-id="b89ef-118">2</span><span class="sxs-lookup"><span data-stu-id="b89ef-118">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="b89ef-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b89ef-119">Remarks</span></span>

<span data-ttu-id="b89ef-120">O \_ tipo de enumeração ' salvar como tipo ' certificados CApicor \_ \_ \_ é usado pelo método [**Certificates. Save**](certificates-save.md) .</span><span class="sxs-lookup"><span data-stu-id="b89ef-120">The CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE enumeration type is used by the [**Certificates.Save**](certificates-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b89ef-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b89ef-121">Requirements</span></span>



| <span data-ttu-id="b89ef-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b89ef-122">Requirement</span></span> | <span data-ttu-id="b89ef-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b89ef-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b89ef-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="b89ef-124">Redistributable</span></span><br/> | <span data-ttu-id="b89ef-125">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="b89ef-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="b89ef-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b89ef-126">Header</span></span><br/>          | <dl> <span data-ttu-id="b89ef-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b89ef-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 




