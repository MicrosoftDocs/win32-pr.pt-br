---
description: 'IUserIdentityManager:: EnumIdentities não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.'
ms.assetid: 8111fbcd-dc4d-45cb-83e0-3c2cd7c4df27
title: 'Método IUserIdentityManager:: EnumIdentities (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.EnumIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3109867651b69e311639d8b2e70e5f02e33a3dc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089713"
---
# <a name="iuseridentitymanagerenumidentities-method"></a><span data-ttu-id="43271-104">Método IUserIdentityManager:: EnumIdentities</span><span class="sxs-lookup"><span data-stu-id="43271-104">IUserIdentityManager::EnumIdentities method</span></span>

<span data-ttu-id="43271-105">\[**IUserIdentityManager:: EnumIdentities** não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="43271-105">\[**IUserIdentityManager::EnumIdentities** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="43271-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="43271-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="43271-107">Obtém um objeto [**IEnumUserIdentity**](ienumuseridentity.md) , que pode ser usado para enumerar as identidades de usuário presentes no sistema.</span><span class="sxs-lookup"><span data-stu-id="43271-107">Gets an [**IEnumUserIdentity**](ienumuseridentity.md) object, which can be used to enumerate through the user identities present on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="43271-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43271-108">Syntax</span></span>


```C++
HRESULT EnumIdentities(
  [out] IEnumUserIdentity **ppEnumUser
);
```



## <a name="parameters"></a><span data-ttu-id="43271-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43271-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43271-110">*ppEnumUser* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="43271-110">*ppEnumUser* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43271-111">Tipo: **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="43271-111">Type: **[**IEnumUserIdentity**](ienumuseridentity.md)\*\***</span></span>

<span data-ttu-id="43271-112">O endereço do ponteiro para o novo objeto de enumeração de identidade.</span><span class="sxs-lookup"><span data-stu-id="43271-112">The address of the pointer to the new identity enumeration object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43271-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43271-113">Return value</span></span>

<span data-ttu-id="43271-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="43271-114">Type: **HRESULT**</span></span>

<span data-ttu-id="43271-115">O resultado da operação de recuperação.</span><span class="sxs-lookup"><span data-stu-id="43271-115">The result of the retrieval operation.</span></span> <span data-ttu-id="43271-116">Se for bem-sucedido, retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="43271-116">If successful, it returns S\_OK.</span></span> <span data-ttu-id="43271-117">Se o objeto de enumeração não puder ser criado, ele retornará E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="43271-117">If the enumeration object could not be created, it returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="43271-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="43271-118">Remarks</span></span>

<span data-ttu-id="43271-119">Esse método é útil para iteração na lista de identidades no sistema.</span><span class="sxs-lookup"><span data-stu-id="43271-119">This method is useful for iteration over the list of identities on the system.</span></span> <span data-ttu-id="43271-120">Para recuperar uma única identidade por seu cookie sem acessar a lista, chame [**IUserIdentityManager:: GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md).</span><span class="sxs-lookup"><span data-stu-id="43271-120">To retrieve a single identity by its cookie without accessing the list, call [**IUserIdentityManager::GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43271-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43271-121">Requirements</span></span>



| <span data-ttu-id="43271-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="43271-122">Requirement</span></span> | <span data-ttu-id="43271-123">Valor</span><span class="sxs-lookup"><span data-stu-id="43271-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43271-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43271-124">Minimum supported client</span></span><br/> | <span data-ttu-id="43271-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="43271-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="43271-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43271-126">Minimum supported server</span></span><br/> | <span data-ttu-id="43271-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="43271-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="43271-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="43271-128">End of client support</span></span><br/>    | <span data-ttu-id="43271-129">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="43271-129">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="43271-130">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="43271-130">End of server support</span></span><br/>    | <span data-ttu-id="43271-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="43271-131">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="43271-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43271-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="43271-133"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="43271-133"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="43271-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="43271-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="43271-135"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="43271-135"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="43271-136">DLL</span><span class="sxs-lookup"><span data-stu-id="43271-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43271-137"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43271-137"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43271-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="43271-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43271-139">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="43271-139">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="43271-140">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="43271-140">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="43271-141">**IUserIdentityManager::GetIdentityByCookie**</span><span class="sxs-lookup"><span data-stu-id="43271-141">**IUserIdentityManager::GetIdentityByCookie**</span></span>](iuseridentitymanager-getidentitybycookie.md)
</dt> </dl>

 

 




