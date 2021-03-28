---
description: IUserIdentity não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: c2f11f8b-f944-445b-b4fc-ac57b0fe3a74
title: Interface IUserIdentity (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 068d806086aff44db172a4a7b09f55b600204478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967883"
---
# <a name="iuseridentity-interface"></a><span data-ttu-id="a2e22-104">Interface IUserIdentity</span><span class="sxs-lookup"><span data-stu-id="a2e22-104">IUserIdentity interface</span></span>

<span data-ttu-id="a2e22-105">\[**IUserIdentity** não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="a2e22-105">\[**IUserIdentity** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="a2e22-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="a2e22-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="a2e22-107">Expõe métodos que fornecem dados de identificação, registro e pasta para uma identidade de usuário específica.</span><span class="sxs-lookup"><span data-stu-id="a2e22-107">Exposes methods that provide identification, registry, and folder data for a specific user identity.</span></span>

## <a name="members"></a><span data-ttu-id="a2e22-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a2e22-108">Members</span></span>

<span data-ttu-id="a2e22-109">A interface **IUserIdentity** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a2e22-109">The **IUserIdentity** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a2e22-110">**IUserIdentity** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a2e22-110">**IUserIdentity** also has these types of members:</span></span>

-   [<span data-ttu-id="a2e22-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a2e22-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a2e22-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a2e22-112">Methods</span></span>

<span data-ttu-id="a2e22-113">A interface **IUserIdentity** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a2e22-113">The **IUserIdentity** interface has these methods.</span></span>



| <span data-ttu-id="a2e22-114">Método</span><span class="sxs-lookup"><span data-stu-id="a2e22-114">Method</span></span>                                                         | <span data-ttu-id="a2e22-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2e22-115">Description</span></span>                                                                                      |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2e22-116">**GetCookie**</span><span class="sxs-lookup"><span data-stu-id="a2e22-116">**GetCookie**</span></span>](iuseridentity-getcookie.md)                   | <span data-ttu-id="a2e22-117">Preterido.</span><span class="sxs-lookup"><span data-stu-id="a2e22-117">Deprecated.</span></span> <span data-ttu-id="a2e22-118">Obtém o cookie usado para identificar exclusivamente essa identidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="a2e22-118">Gets the cookie used to uniquely identify this user identity.</span></span><br/>             |
| [<span data-ttu-id="a2e22-119">**GetIdentityFolder**</span><span class="sxs-lookup"><span data-stu-id="a2e22-119">**GetIdentityFolder**</span></span>](iuseridentity-getidentityfolder.md)   | <span data-ttu-id="a2e22-120">Preterido.</span><span class="sxs-lookup"><span data-stu-id="a2e22-120">Deprecated.</span></span> <span data-ttu-id="a2e22-121">Obtém a pasta de arquivos associada a essa identidade.</span><span class="sxs-lookup"><span data-stu-id="a2e22-121">Gets the file folder associated with this identity.</span></span><br/>                       |
| [<span data-ttu-id="a2e22-122">**GetName**</span><span class="sxs-lookup"><span data-stu-id="a2e22-122">**GetName**</span></span>](iuseridentity-getname.md)                       | <span data-ttu-id="a2e22-123">Preterido.</span><span class="sxs-lookup"><span data-stu-id="a2e22-123">Deprecated.</span></span> <span data-ttu-id="a2e22-124">Obtém o nome associado a esta identidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="a2e22-124">Gets the name associated with this user identity.</span></span><br/>                         |
| [<span data-ttu-id="a2e22-125">**OpenIdentityRegKey**</span><span class="sxs-lookup"><span data-stu-id="a2e22-125">**OpenIdentityRegKey**</span></span>](iuseridentity-openidentityregkey.md) | <span data-ttu-id="a2e22-126">Preterido.</span><span class="sxs-lookup"><span data-stu-id="a2e22-126">Deprecated.</span></span> <span data-ttu-id="a2e22-127">Recupera a chave no registro que corresponde a essa identidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="a2e22-127">Retrieves the key in the registry that corresponds to this user identity.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a2e22-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2e22-128">Remarks</span></span>

<span data-ttu-id="a2e22-129">Essa interface fornece informações que correspondem a uma identidade de usuário específica presente no sistema.</span><span class="sxs-lookup"><span data-stu-id="a2e22-129">This interface provides information that corresponds to a specific user identity present on the system.</span></span> <span data-ttu-id="a2e22-130">Você pode acessar a pasta Identity da identidade do usuário, sua chave do registro e seu cookie de identificação, bem como recuperar o nome associado à identidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="a2e22-130">You can access this user identity's identity folder, its registry key, and its identification cookie, as well as retrieve the name associated with the user identity.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2e22-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2e22-131">Requirements</span></span>



| <span data-ttu-id="a2e22-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2e22-132">Requirement</span></span> | <span data-ttu-id="a2e22-133">Valor</span><span class="sxs-lookup"><span data-stu-id="a2e22-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2e22-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2e22-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a2e22-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a2e22-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a2e22-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2e22-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a2e22-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a2e22-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a2e22-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a2e22-138">End of client support</span></span><br/>    | <span data-ttu-id="a2e22-139">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a2e22-139">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="a2e22-140">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a2e22-140">End of server support</span></span><br/>    | <span data-ttu-id="a2e22-141">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a2e22-141">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="a2e22-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2e22-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2e22-143"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2e22-143"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2e22-144">INSERI</span><span class="sxs-lookup"><span data-stu-id="a2e22-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a2e22-145"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a2e22-145"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="a2e22-146">DLL</span><span class="sxs-lookup"><span data-stu-id="a2e22-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2e22-147"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2e22-147"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2e22-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2e22-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2e22-149">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="a2e22-149">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="a2e22-150">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="a2e22-150">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="a2e22-151">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="a2e22-151">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> </dl>

 

 
