---
description: Indica o local de um repositório de certificados.
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: Enumeração de CAPICOM_STORE_LOCATION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 24b2e786e2821c39c6ff67f5919dca2ac0c6bfe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758280"
---
# <a name="capicom_store_location-enumeration"></a><span data-ttu-id="d754c-103">Enumeração do local de \_ armazenamento CApicom \_</span><span class="sxs-lookup"><span data-stu-id="d754c-103">CAPICOM\_STORE\_LOCATION enumeration</span></span>

<span data-ttu-id="d754c-104">O tipo de enumeração do **\_ \_ local de armazenamento capicor** indica o local de um [*repositório de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d754c-104">The **CAPICOM\_STORE\_LOCATION** enumeration type indicates the location of a [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="d754c-105">Membros</span><span class="sxs-lookup"><span data-stu-id="d754c-105">Members</span></span>



| <span data-ttu-id="d754c-106">Membro</span><span class="sxs-lookup"><span data-stu-id="d754c-106">Member</span></span>                                      | <span data-ttu-id="d754c-107">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="d754c-107">Description</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="d754c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="d754c-108">Value</span></span> |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="d754c-109">**\_armazenamento de memória CApicom \_**</span><span class="sxs-lookup"><span data-stu-id="d754c-109">**CAPICOM\_MEMORY\_STORE**</span></span>                  | <span data-ttu-id="d754c-110">O repositório é um repositório de memória.</span><span class="sxs-lookup"><span data-stu-id="d754c-110">The store is a memory store.</span></span> <span data-ttu-id="d754c-111">As alterações no conteúdo da loja não são persistentes.</span><span class="sxs-lookup"><span data-stu-id="d754c-111">Any changes in the contents of the store are not persisted.</span></span><br/>                                                                                                                                                                              | <span data-ttu-id="d754c-112">0</span><span class="sxs-lookup"><span data-stu-id="d754c-112">0</span></span>     |
| <span data-ttu-id="d754c-113">**CAPICOM do \_ \_ armazenamento do computador local \_**</span><span class="sxs-lookup"><span data-stu-id="d754c-113">**CAPICOM\_LOCAL\_MACHINE\_STORE**</span></span>          | <span data-ttu-id="d754c-114">O repositório é um repositório do computador local.</span><span class="sxs-lookup"><span data-stu-id="d754c-114">The store is a local machine store.</span></span> <span data-ttu-id="d754c-115">Os repositórios do computador local poderão ser armazenamentos de leitura/gravação somente se o usuário tiver permissões de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d754c-115">Local machine stores can be read/write stores only if the user has read/write permissions.</span></span> <span data-ttu-id="d754c-116">Se o usuário tiver permissões de leitura/gravação e se o repositório for aberto como leitura/gravação, as alterações no conteúdo do repositório serão persistidas.</span><span class="sxs-lookup"><span data-stu-id="d754c-116">If the user has read/write permissions and if the store is opened read/write, then changes in the contents of the store are persisted.</span></span><br/> | <span data-ttu-id="d754c-117">1</span><span class="sxs-lookup"><span data-stu-id="d754c-117">1</span></span>     |
| <span data-ttu-id="d754c-118">**\_armazenamento de \_ usuário \_ atual do CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="d754c-118">**CAPICOM\_CURRENT\_USER\_STORE**</span></span>           | <span data-ttu-id="d754c-119">O repositório é um armazenamento de usuário atual.</span><span class="sxs-lookup"><span data-stu-id="d754c-119">The store is a current user store.</span></span> <span data-ttu-id="d754c-120">Um armazenamento de usuário atual pode ser um repositório de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d754c-120">A current user store may be a read/write store.</span></span> <span data-ttu-id="d754c-121">Se for, as alterações no conteúdo do repositório serão persistidas.</span><span class="sxs-lookup"><span data-stu-id="d754c-121">If it is, changes in the contents of the store are persisted.</span></span><br/>                                                                                                                      | <span data-ttu-id="d754c-122">2</span><span class="sxs-lookup"><span data-stu-id="d754c-122">2</span></span>     |
| <span data-ttu-id="d754c-123">**armazenamento de usuários do CAPICOM \_ \_ do Active Directory \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d754c-123">**CAPICOM\_ACTIVE\_DIRECTORY\_USER\_STORE**</span></span> | <span data-ttu-id="d754c-124">O repositório é um repositório Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d754c-124">The store is an Active Directory store.</span></span> <span data-ttu-id="d754c-125">Active Directory armazenamentos só podem ser abertos no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d754c-125">Active Directory stores can be opened only in read-only mode.</span></span> <span data-ttu-id="d754c-126">Os certificados não podem ser adicionados ou removidos de repositórios Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d754c-126">Certificates cannot be added to or removed from Active Directory stores.</span></span><br/>                                                                                        | <span data-ttu-id="d754c-127">3</span><span class="sxs-lookup"><span data-stu-id="d754c-127">3</span></span>     |
| <span data-ttu-id="d754c-128">**\_armazenamento de \_ usuário do cartão inteligente \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="d754c-128">**CAPICOM\_SMART\_CARD\_USER\_STORE**</span></span>       | <span data-ttu-id="d754c-129">Os repositórios dão suporte a repositórios de certificados baseados em cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="d754c-129">Stores support smart card–based certificate stores.</span></span> <span data-ttu-id="d754c-130">O repositório é o grupo de cartões inteligentes presentes.</span><span class="sxs-lookup"><span data-stu-id="d754c-130">The store is the group of present smart cards.</span></span> <span data-ttu-id="d754c-131">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="d754c-131">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                                                                         | <span data-ttu-id="d754c-132">4</span><span class="sxs-lookup"><span data-stu-id="d754c-132">4</span></span>     |



## <a name="remarks"></a><span data-ttu-id="d754c-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="d754c-133">Remarks</span></span>

<span data-ttu-id="d754c-134">O tipo de enumeração do **\_ \_ local de armazenamento CAPICOM** é usado pelos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="d754c-134">The **CAPICOM\_STORE\_LOCATION** enumeration type is used by the following methods:</span></span>

-   [<span data-ttu-id="d754c-135">**PrivateKey. Open**</span><span class="sxs-lookup"><span data-stu-id="d754c-135">**PrivateKey.Open**</span></span>](privatekey-open.md)
-   [<span data-ttu-id="d754c-136">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="d754c-136">**Store.Open**</span></span>](store-open.md)

## <a name="requirements"></a><span data-ttu-id="d754c-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d754c-137">Requirements</span></span>



| <span data-ttu-id="d754c-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="d754c-138">Requirement</span></span> | <span data-ttu-id="d754c-139">Valor</span><span class="sxs-lookup"><span data-stu-id="d754c-139">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d754c-140">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d754c-140">Redistributable</span></span><br/> | <span data-ttu-id="d754c-141">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="d754c-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="d754c-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d754c-142">Header</span></span><br/>          | <dl> <span data-ttu-id="d754c-143"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="d754c-143"><dt>Capicom.h</dt></span></span> </dl> |



 

 
