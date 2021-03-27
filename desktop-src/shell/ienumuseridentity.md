---
description: IEnumUserIdentity não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: df4b6235-e66a-4187-b1f9-33c042cae2f2
title: Interface IEnumUserIdentity (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 48abf182942f90ecd477a241be3bf45323bdbdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967888"
---
# <a name="ienumuseridentity-interface"></a><span data-ttu-id="3673b-104">Interface IEnumUserIdentity</span><span class="sxs-lookup"><span data-stu-id="3673b-104">IEnumUserIdentity interface</span></span>

<span data-ttu-id="3673b-105">\[**IEnumUserIdentity** não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="3673b-105">\[**IEnumUserIdentity** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="3673b-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="3673b-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="3673b-107">Fornece a enumeração de todas as identidades de usuário presentes no sistema.</span><span class="sxs-lookup"><span data-stu-id="3673b-107">Provides enumeration of all user identities present on the system.</span></span>

## <a name="members"></a><span data-ttu-id="3673b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="3673b-108">Members</span></span>

<span data-ttu-id="3673b-109">A interface **IEnumUserIdentity** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3673b-109">The **IEnumUserIdentity** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3673b-110">**IEnumUserIdentity** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3673b-110">**IEnumUserIdentity** also has these types of members:</span></span>

-   [<span data-ttu-id="3673b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="3673b-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3673b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3673b-112">Methods</span></span>

<span data-ttu-id="3673b-113">A interface **IEnumUserIdentity** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3673b-113">The **IEnumUserIdentity** interface has these methods.</span></span>



| <span data-ttu-id="3673b-114">Método</span><span class="sxs-lookup"><span data-stu-id="3673b-114">Method</span></span>                                         | <span data-ttu-id="3673b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="3673b-115">Description</span></span>                                                                                                                  |
|:-----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3673b-116">**8i**</span><span class="sxs-lookup"><span data-stu-id="3673b-116">**Clone**</span></span>](ienumuseridentity-clone.md)       | <span data-ttu-id="3673b-117">Preterido.</span><span class="sxs-lookup"><span data-stu-id="3673b-117">Deprecated.</span></span> <span data-ttu-id="3673b-118">Obtém uma cópia da enumeração atual.</span><span class="sxs-lookup"><span data-stu-id="3673b-118">Gets a copy of the current enumeration.</span></span><br/>                                                               |
| [<span data-ttu-id="3673b-119">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="3673b-119">**GetCount**</span></span>](ienumuseridentity-getcount.md) | <span data-ttu-id="3673b-120">Preterido.</span><span class="sxs-lookup"><span data-stu-id="3673b-120">Deprecated.</span></span> <span data-ttu-id="3673b-121">Obtém a contagem de identidades de usuário atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="3673b-121">Gets the count of user identities currently on the system.</span></span><br/>                                            |
| [<span data-ttu-id="3673b-122">**Avançar**</span><span class="sxs-lookup"><span data-stu-id="3673b-122">**Next**</span></span>](ienumuseridentity-next.md)         | <span data-ttu-id="3673b-123">Preterido.</span><span class="sxs-lookup"><span data-stu-id="3673b-123">Deprecated.</span></span> <span data-ttu-id="3673b-124">Recupera uma matriz de interfaces de identidade do usuário da enumeração.</span><span class="sxs-lookup"><span data-stu-id="3673b-124">Retrieves an array of user identity interfaces from the enumeration.</span></span><br/>                                  |
| [<span data-ttu-id="3673b-125">**Definido**</span><span class="sxs-lookup"><span data-stu-id="3673b-125">**Reset**</span></span>](ienumuseridentity-reset.md)       | <span data-ttu-id="3673b-126">Preterido.</span><span class="sxs-lookup"><span data-stu-id="3673b-126">Deprecated.</span></span> <span data-ttu-id="3673b-127">Redefine a contagem interna de interfaces recuperadas na enumeração.</span><span class="sxs-lookup"><span data-stu-id="3673b-127">Resets the internal count of retrieved interfaces in the enumeration.</span></span><br/>                                 |
| [<span data-ttu-id="3673b-128">**Ignorar**</span><span class="sxs-lookup"><span data-stu-id="3673b-128">**Skip**</span></span>](ienumuseridentity-skip.md)         | <span data-ttu-id="3673b-129">Preterido.</span><span class="sxs-lookup"><span data-stu-id="3673b-129">Deprecated.</span></span> <span data-ttu-id="3673b-130">Ignora um determinado número de interfaces de identidade de usuário na enumeração.</span><span class="sxs-lookup"><span data-stu-id="3673b-130">Skips a given number of user identity interfaces in the enumeration.</span></span> <span data-ttu-id="3673b-131">Usado ao recuperar interfaces.</span><span class="sxs-lookup"><span data-stu-id="3673b-131">Used when retrieving interfaces.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3673b-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="3673b-132">Remarks</span></span>

<span data-ttu-id="3673b-133">Para recuperar informações sobre as identidades de usuário presentes no sistema, você pode usar essa interface.</span><span class="sxs-lookup"><span data-stu-id="3673b-133">To retrieve information about user identities present on the system, you can use this interface.</span></span> <span data-ttu-id="3673b-134">Em uma interface [**IUserIdentityManager**](iuseridentitymanager.md) , você pode chamar [**IUserIdentityManager:: EnumIdentities**](iuseridentitymanager-enumidentities.md) para recuperar essa interface.</span><span class="sxs-lookup"><span data-stu-id="3673b-134">From a [**IUserIdentityManager**](iuseridentitymanager.md) interface, you can call [**IUserIdentityManager::EnumIdentities**](iuseridentitymanager-enumidentities.md) to retrieve this interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="3673b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3673b-135">Requirements</span></span>



| <span data-ttu-id="3673b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="3673b-136">Requirement</span></span> | <span data-ttu-id="3673b-137">Valor</span><span class="sxs-lookup"><span data-stu-id="3673b-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3673b-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3673b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3673b-139">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3673b-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3673b-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3673b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3673b-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3673b-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3673b-142">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3673b-142">End of client support</span></span><br/>    | <span data-ttu-id="3673b-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3673b-143">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="3673b-144">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="3673b-144">End of server support</span></span><br/>    | <span data-ttu-id="3673b-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3673b-145">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="3673b-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3673b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="3673b-147"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="3673b-147"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="3673b-148">INSERI</span><span class="sxs-lookup"><span data-stu-id="3673b-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3673b-149"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3673b-149"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="3673b-150">DLL</span><span class="sxs-lookup"><span data-stu-id="3673b-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3673b-151"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3673b-151"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3673b-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="3673b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3673b-153">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="3673b-153">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> </dl>

 

 
