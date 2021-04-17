---
title: Interface INapSystemHealthValidationRequest2 (NapSystemHealthValidator. h)
description: Fornece métodos que são usados para dar suporte a validadores de integridade do sistema que são definidos pelo desenvolvedor do aplicativo.
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- INapSystemHealthValidationRequest2 da interface NAP
- INapSystemHealthValidationRequest2 interface NAP, descrita
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12fdbfc46578a4e64a92accc46f6b910a44dd946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769428"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a><span data-ttu-id="20341-105">Interface INapSystemHealthValidationRequest2</span><span class="sxs-lookup"><span data-stu-id="20341-105">INapSystemHealthValidationRequest2 interface</span></span>

> [!Note]  
> <span data-ttu-id="20341-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="20341-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="20341-107">A interface **INapSystemHealthValidationRequest2** fornece métodos que são usados para dar suporte a validadores de integridade do sistema que são definidos pelo desenvolvedor do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="20341-107">The **INapSystemHealthValidationRequest2** interface provides methods that are used to support system health validators which are defined by the application developer.</span></span>

> [!Note]  
> <span data-ttu-id="20341-108">Essa interface herda todos os métodos de [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) e deve ser usada em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="20341-108">This interface inherits all the methods of [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="20341-109">Membros</span><span class="sxs-lookup"><span data-stu-id="20341-109">Members</span></span>

<span data-ttu-id="20341-110">A interface **INapSystemHealthValidationRequest2** herda de [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).</span><span class="sxs-lookup"><span data-stu-id="20341-110">The **INapSystemHealthValidationRequest2** interface inherits from [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).</span></span> <span data-ttu-id="20341-111">**INapSystemHealthValidationRequest2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="20341-111">**INapSystemHealthValidationRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="20341-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="20341-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="20341-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="20341-113">Methods</span></span>

<span data-ttu-id="20341-114">A interface **INapSystemHealthValidationRequest2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="20341-114">The **INapSystemHealthValidationRequest2** interface has these methods.</span></span>



| <span data-ttu-id="20341-115">Método</span><span class="sxs-lookup"><span data-stu-id="20341-115">Method</span></span>                                                                                                    | <span data-ttu-id="20341-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="20341-116">Description</span></span>                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="20341-117">**INapSystemHealthValidationRequest2:: getconfigid**</span><span class="sxs-lookup"><span data-stu-id="20341-117">**INapSystemHealthValidationRequest2::GetConfigId**</span></span>](inapsystemhealthvalidationrequest2-getconfigid.md) | <span data-ttu-id="20341-118">Recupera a ID de configuração em uma solicitação de validação.</span><span class="sxs-lookup"><span data-stu-id="20341-118">Retrieves the configuration id in a validation request.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="20341-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="20341-119">Remarks</span></span>

<span data-ttu-id="20341-120">Se um SHV não oferecer suporte a [**INapComponentConfig3**](inapcomponentconfig3.md), essa interface não se aplicará.</span><span class="sxs-lookup"><span data-stu-id="20341-120">If an SHV doesn t support [**INapComponentConfig3**](inapcomponentconfig3.md), this interface doesn t apply.</span></span>

## <a name="requirements"></a><span data-ttu-id="20341-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20341-121">Requirements</span></span>



| <span data-ttu-id="20341-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="20341-122">Requirement</span></span> | <span data-ttu-id="20341-123">Valor</span><span class="sxs-lookup"><span data-stu-id="20341-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20341-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20341-124">Minimum supported client</span></span><br/> | <span data-ttu-id="20341-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="20341-125">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="20341-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20341-126">Minimum supported server</span></span><br/> | <span data-ttu-id="20341-127">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="20341-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="20341-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20341-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="20341-129"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="20341-129"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="20341-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="20341-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="20341-131"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="20341-131"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="20341-132">DLL</span><span class="sxs-lookup"><span data-stu-id="20341-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20341-133"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20341-133"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="20341-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="20341-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20341-135">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="20341-135">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[<span data-ttu-id="20341-136">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="20341-136">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="20341-137">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="20341-137">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





