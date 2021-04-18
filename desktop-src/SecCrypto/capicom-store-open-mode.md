---
description: Usado com o método Store. Open para indicar como um repositório de certificados deve ser aberto.
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: Enumeração de CAPICOM_STORE_OPEN_MODE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_OPEN_MODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 61fe8be0bdf75db5204066563ca07f8225678f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752743"
---
# <a name="capicom_store_open_mode-enumeration"></a><span data-ttu-id="038a9-103">\_Enumeração do \_ modo de abertura do armazenamento CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="038a9-103">CAPICOM\_STORE\_OPEN\_MODE enumeration</span></span>

<span data-ttu-id="038a9-104">O tipo de enumeração do modo de armazenamento CAPICOM \_ \_ \_ é usado com o método [**Store. Open**](store-open.md) para indicar como um repositório de certificados deve ser aberto.</span><span class="sxs-lookup"><span data-stu-id="038a9-104">The CAPICOM\_STORE\_OPEN\_MODE enumeration type is used with the [**Store.Open**](store-open.md) method to indicate how a certificate store is to be opened.</span></span>

## <a name="members"></a><span data-ttu-id="038a9-105">Membros</span><span class="sxs-lookup"><span data-stu-id="038a9-105">Members</span></span>



| <span data-ttu-id="038a9-106">Membro</span><span class="sxs-lookup"><span data-stu-id="038a9-106">Member</span></span>                                      | <span data-ttu-id="038a9-107">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="038a9-107">Description</span></span>                                                                                                                                                              | <span data-ttu-id="038a9-108">Valor</span><span class="sxs-lookup"><span data-stu-id="038a9-108">Value</span></span> |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="038a9-109">**CAPICOM de \_ leitura do armazenamento \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="038a9-109">**CAPICOM\_STORE\_OPEN\_READ\_ONLY**</span></span>        | <span data-ttu-id="038a9-110">Abra o repositório no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="038a9-110">Open the store in read-only mode.</span></span><br/>                                                                                                                             | <span data-ttu-id="038a9-111">0</span><span class="sxs-lookup"><span data-stu-id="038a9-111">0</span></span>     |
| <span data-ttu-id="038a9-112">**o CAPICOM de \_ \_ leitura e \_ \_ gravação aberta**</span><span class="sxs-lookup"><span data-stu-id="038a9-112">**CAPICOM\_STORE\_OPEN\_READ\_WRITE**</span></span>       | <span data-ttu-id="038a9-113">Abra o repositório no modo de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="038a9-113">Open the store in read/write mode.</span></span><br/>                                                                                                                            | <span data-ttu-id="038a9-114">1</span><span class="sxs-lookup"><span data-stu-id="038a9-114">1</span></span>     |
| <span data-ttu-id="038a9-115">**\_ \_ \_ máximo permitido de armazenamento \_ de CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="038a9-115">**CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED**</span></span>  | <span data-ttu-id="038a9-116">Abra o repositório no modo de leitura/gravação se o usuário tiver permissões de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="038a9-116">Open the store in read/write mode if the user has read/write permissions.</span></span> <span data-ttu-id="038a9-117">Se o usuário não tiver permissões de leitura/gravação, abra o repositório no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="038a9-117">If the user does not have read/write permissions, open the store in read-only mode.</span></span><br/> | <span data-ttu-id="038a9-118">2</span><span class="sxs-lookup"><span data-stu-id="038a9-118">2</span></span>     |
| <span data-ttu-id="038a9-119">**CAPICOM \_ Store \_ abrir \_ \_ somente existente**</span><span class="sxs-lookup"><span data-stu-id="038a9-119">**CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY**</span></span>    | <span data-ttu-id="038a9-120">Abrir somente repositórios existentes; Não crie um novo repositório.</span><span class="sxs-lookup"><span data-stu-id="038a9-120">Open existing stores only; do not create a new store.</span></span> <span data-ttu-id="038a9-121">Introduzido por CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="038a9-121">Introduced by CAPICOM 2.0.</span></span><br/>                                                                              | <span data-ttu-id="038a9-122">128</span><span class="sxs-lookup"><span data-stu-id="038a9-122">128</span></span>   |
| <span data-ttu-id="038a9-123">**o CAPICOM de \_ Store \_ aberto \_ incluem \_ arquivados**</span><span class="sxs-lookup"><span data-stu-id="038a9-123">**CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED**</span></span> | <span data-ttu-id="038a9-124">Inclua certificados arquivados ao usar o repositório.</span><span class="sxs-lookup"><span data-stu-id="038a9-124">Include archived certificates when using the store.</span></span> <span data-ttu-id="038a9-125">Introduzido por CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="038a9-125">Introduced by CAPICOM 2.0.</span></span><br/>                                                                                | <span data-ttu-id="038a9-126">256</span><span class="sxs-lookup"><span data-stu-id="038a9-126">256</span></span>   |



## <a name="remarks"></a><span data-ttu-id="038a9-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="038a9-127">Remarks</span></span>

<span data-ttu-id="038a9-128">Ao usar a enumeração do modo de abertura do armazenamento CAPICOM \_ \_ \_ , somente uma das seguintes configurações pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="038a9-128">When using the CAPICOM\_STORE\_OPEN\_MODE enumeration, only one of the following settings can be used.</span></span>

-   <span data-ttu-id="038a9-129">CAPICOM de \_ leitura do armazenamento \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="038a9-129">CAPICOM\_STORE\_OPEN\_READ\_ONLY</span></span>
-   <span data-ttu-id="038a9-130">o CAPICOM de \_ \_ leitura e \_ \_ gravação aberta</span><span class="sxs-lookup"><span data-stu-id="038a9-130">CAPICOM\_STORE\_OPEN\_READ\_WRITE</span></span>
-   <span data-ttu-id="038a9-131">\_ \_ \_ máximo permitido de armazenamento \_ de CAPICOM</span><span class="sxs-lookup"><span data-stu-id="038a9-131">CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED</span></span>

## <a name="requirements"></a><span data-ttu-id="038a9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="038a9-132">Requirements</span></span>



| <span data-ttu-id="038a9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="038a9-133">Requirement</span></span> | <span data-ttu-id="038a9-134">Valor</span><span class="sxs-lookup"><span data-stu-id="038a9-134">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="038a9-135">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="038a9-135">Redistributable</span></span><br/> | <span data-ttu-id="038a9-136">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="038a9-136">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="038a9-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="038a9-137">Header</span></span><br/>          | <dl> <span data-ttu-id="038a9-138"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="038a9-138"><dt>Capicom.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="038a9-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="038a9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="038a9-140">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="038a9-140">**Store.Open**</span></span>](store-open.md)
</dt> </dl>

 

 




