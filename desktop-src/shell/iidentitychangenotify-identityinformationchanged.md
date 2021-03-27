---
description: IdentityInformationChanged não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: 3aca8a98-3d12-482d-9991-d6b53adde522
title: 'Método IIdentityChangeNotify:: IdentityInformationChanged (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.IdentityInformationChanged
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: c33f67a4def3312564ed943e2a3a917fe2843980
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828281"
---
# <a name="iidentitychangenotifyidentityinformationchanged-method"></a><span data-ttu-id="43ceb-104">Método IIdentityChangeNotify:: IdentityInformationChanged</span><span class="sxs-lookup"><span data-stu-id="43ceb-104">IIdentityChangeNotify::IdentityInformationChanged method</span></span>

<span data-ttu-id="43ceb-105">\[**IdentityInformationChanged** não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="43ceb-105">\[**IdentityInformationChanged** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="43ceb-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="43ceb-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="43ceb-107">Chamado quando informações sobre uma identidade de usuário são alteradas ou quando uma identidade de usuário é adicionada ou excluída.</span><span class="sxs-lookup"><span data-stu-id="43ceb-107">Called when information about a user identity has changed, or when a user identity has been added or deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="43ceb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43ceb-108">Syntax</span></span>


```C++
HRESULT IdentityInformationChanged(
   DWORD dwType
);
```



## <a name="parameters"></a><span data-ttu-id="43ceb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43ceb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43ceb-110">*dwType*</span><span class="sxs-lookup"><span data-stu-id="43ceb-110">*dwType*</span></span> 
</dt> <dd>

<span data-ttu-id="43ceb-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="43ceb-111">Type: **DWORD**</span></span>

<span data-ttu-id="43ceb-112">Um valor que especifica o tipo de informação alterado ou a operação executada em uma identidade.</span><span class="sxs-lookup"><span data-stu-id="43ceb-112">A value that specifies the type of information changed, or the operation performed on an identity.</span></span> <span data-ttu-id="43ceb-113">Pode ser uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="43ceb-113">Can be a combination of the following values.</span></span>

<dt>



 <span data-ttu-id="43ceb-114">(IIC \_ \_identidade atual \_ alterada)</span><span class="sxs-lookup"><span data-stu-id="43ceb-114">(IIC\_CURRENT\_IDENTITY\_CHANGED)</span></span>


</dt> <dd>

<span data-ttu-id="43ceb-115">A identidade atual foi modificada.</span><span class="sxs-lookup"><span data-stu-id="43ceb-115">The current identity has been modified.</span></span>

</dd> <dt>



 <span data-ttu-id="43ceb-116">(IIC \_ IDENTIDADE \_ alterada)</span><span class="sxs-lookup"><span data-stu-id="43ceb-116">(IIC\_IDENTITY\_CHANGED)</span></span>


</dt> <dd>

<span data-ttu-id="43ceb-117">Uma identidade foi modificada.</span><span class="sxs-lookup"><span data-stu-id="43ceb-117">An identity has been modified.</span></span>

</dd> <dt>



 <span data-ttu-id="43ceb-118">(IIC \_ IDENTIDADE \_ excluída)</span><span class="sxs-lookup"><span data-stu-id="43ceb-118">(IIC\_IDENTITY\_DELETED)</span></span>


</dt> <dd>

<span data-ttu-id="43ceb-119">Uma identidade foi excluída.</span><span class="sxs-lookup"><span data-stu-id="43ceb-119">An identity has been deleted.</span></span>

</dd> <dt>



 <span data-ttu-id="43ceb-120">(IIC \_ IDENTIDADE \_ adicionada)</span><span class="sxs-lookup"><span data-stu-id="43ceb-120">(IIC\_IDENTITY\_ADDED)</span></span>


</dt> <dd>

<span data-ttu-id="43ceb-121">Uma nova identidade foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="43ceb-121">A new identity has been added.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43ceb-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43ceb-122">Return value</span></span>

<span data-ttu-id="43ceb-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="43ceb-123">Type: **HRESULT**</span></span>

<span data-ttu-id="43ceb-124">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="43ceb-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="43ceb-125">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="43ceb-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="43ceb-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="43ceb-126">Remarks</span></span>

<span data-ttu-id="43ceb-127">Você pode implementar esse método para fornecer um comportamento personalizado para seu aplicativo quando a lista de identidades de usuário no sistema tiver sido modificada.</span><span class="sxs-lookup"><span data-stu-id="43ceb-127">You may implement this method to provide custom behavior for your application when the list of user identities on the system has been modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="43ceb-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43ceb-128">Requirements</span></span>



| <span data-ttu-id="43ceb-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="43ceb-129">Requirement</span></span> | <span data-ttu-id="43ceb-130">Valor</span><span class="sxs-lookup"><span data-stu-id="43ceb-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43ceb-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43ceb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="43ceb-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="43ceb-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="43ceb-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43ceb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="43ceb-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="43ceb-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="43ceb-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="43ceb-135">End of client support</span></span><br/>    | <span data-ttu-id="43ceb-136">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="43ceb-136">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="43ceb-137">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="43ceb-137">End of server support</span></span><br/>    | <span data-ttu-id="43ceb-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="43ceb-138">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="43ceb-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43ceb-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="43ceb-140"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="43ceb-140"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="43ceb-141">INSERI</span><span class="sxs-lookup"><span data-stu-id="43ceb-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="43ceb-142"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="43ceb-142"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="43ceb-143">DLL</span><span class="sxs-lookup"><span data-stu-id="43ceb-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43ceb-144"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43ceb-144"><dt>Msoe.dll</dt></span></span> </dl>    |



 

 




