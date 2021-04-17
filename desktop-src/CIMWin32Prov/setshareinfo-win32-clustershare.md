---
description: Define os parâmetros do recurso compartilhado.
ms.assetid: 592d0fa6-c865-4f70-89c3-b58204a8c5a6
ms.tgt_platform: multiple
title: Método SetShareInfo da classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bda6fe36d1168045ea9f8d331ff334920ed1dd19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755433"
---
# <a name="setshareinfo-method-of-the-win32_clustershare-class"></a><span data-ttu-id="7df8d-103">Método SetShareInfo da classe Win32 \_ ClusterShare</span><span class="sxs-lookup"><span data-stu-id="7df8d-103">SetShareInfo method of the Win32\_ClusterShare class</span></span>

<span data-ttu-id="7df8d-104">Define os parâmetros do recurso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="7df8d-104">Sets the parameters of the shared resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="7df8d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7df8d-105">Syntax</span></span>


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="7df8d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7df8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7df8d-107">*MaximumAllowed* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7df8d-107">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7df8d-108">Limite do número máximo de usuários com permissão para usar este recurso simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="7df8d-108">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="7df8d-109">*Descrição* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7df8d-109">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7df8d-110">Descreve o recurso que está sendo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="7df8d-110">Describes the resource being shared.</span></span>

</dd> <dt>

<span data-ttu-id="7df8d-111">*Acesso* \[ ao em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7df8d-111">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7df8d-112">Descritor de segurança para permissões de nível de usuário.</span><span class="sxs-lookup"><span data-stu-id="7df8d-112">Security descriptor for user-level permissions.</span></span> <span data-ttu-id="7df8d-113">Um descritor de segurança contém informações sobre a permissão, o proprietário e os recursos de acesso do recurso.</span><span class="sxs-lookup"><span data-stu-id="7df8d-113">A security descriptor contains information about the permission, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="7df8d-114">Para obter mais informações, consulte [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="7df8d-114">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7df8d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7df8d-115">Requirements</span></span>



| <span data-ttu-id="7df8d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7df8d-116">Requirement</span></span> | <span data-ttu-id="7df8d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7df8d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7df8d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7df8d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7df8d-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7df8d-119">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="7df8d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7df8d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7df8d-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7df8d-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="7df8d-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="7df8d-122">Namespace</span></span><br/>                | <span data-ttu-id="7df8d-123">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7df8d-123">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7df8d-124">MOF</span><span class="sxs-lookup"><span data-stu-id="7df8d-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7df8d-125"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7df8d-125"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7df8d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7df8d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7df8d-127"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7df8d-127"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7df8d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7df8d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df8d-129">**\_ClusterShare Win32**</span><span class="sxs-lookup"><span data-stu-id="7df8d-129">**Win32\_ClusterShare**</span></span>](win32-clustershare.md)
</dt> </dl>

 

