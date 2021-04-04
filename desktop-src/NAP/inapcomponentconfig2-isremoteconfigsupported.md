---
title: Método INapComponentConfig2 IsRemoteConfigSupported (NapCommon. h)
description: É implementado por SHVs (validadores da integridade do sistema) para indicar se há suporte para a configuração remota.
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- Método IsRemoteConfigSupported NAP
- Método IsRemoteConfigSupported NAP, interface INapComponentConfig2
- INapComponentConfig2 interface NAP, método IsRemoteConfigSupported
topic_type:
- apiref
api_name:
- INapComponentConfig2.IsRemoteConfigSupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d144926aafff6f5ad7e243efe2a81a2955f497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918244"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a><span data-ttu-id="d3c6d-106">Método INapComponentConfig2:: IsRemoteConfigSupported</span><span class="sxs-lookup"><span data-stu-id="d3c6d-106">INapComponentConfig2::IsRemoteConfigSupported method</span></span>

> [!Note]  
> <span data-ttu-id="d3c6d-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="d3c6d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d3c6d-108">O método **IsRemoteConfigSupported** é implementado por SHVs (validadores da integridade do sistema) para indicar se há suporte para a configuração remota.</span><span class="sxs-lookup"><span data-stu-id="d3c6d-108">The **IsRemoteConfigSupported** method is implemented by system health validators (SHVs) to indicate whether remote configuration is supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c6d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3c6d-109">Syntax</span></span>


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a><span data-ttu-id="d3c6d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3c6d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3c6d-111">*IsSupported* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d3c6d-111">*isSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c6d-112">Um ponteiro para um BOOL que será definido como **true** se o componente oferecer suporte à configuração remota e **false** se não tiver.</span><span class="sxs-lookup"><span data-stu-id="d3c6d-112">A pointer to a BOOL that is set to **TRUE** if the component supports remote configuration, and **FALSE** if it does not.</span></span>

</dd> <dt>

<span data-ttu-id="d3c6d-113">*remoteConfigType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d3c6d-113">*remoteConfigType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c6d-114">Indica o tipo de configuração remota com suporte usando o valor da enumeração [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) :</span><span class="sxs-lookup"><span data-stu-id="d3c6d-114">Indicates the type of remote configuration supported using value from the [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) enumeration:</span></span>



| <span data-ttu-id="d3c6d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d3c6d-115">Value</span></span>                                                                                                 | <span data-ttu-id="d3c6d-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d3c6d-116">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d3c6d-117"><dt>remoteConfigTypeMachine</dt></span><span class="sxs-lookup"><span data-stu-id="d3c6d-117"><dt>remoteConfigTypeMachine</dt></span></span> </dl>    | <span data-ttu-id="d3c6d-118">[**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) é implementado.</span><span class="sxs-lookup"><span data-stu-id="d3c6d-118">[**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) is implemented.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="d3c6d-119"><dt>remoteConfigTypeConfigBlob</dt></span><span class="sxs-lookup"><span data-stu-id="d3c6d-119"><dt>remoteConfigTypeConfigBlob</dt></span></span> </dl> | <span data-ttu-id="d3c6d-120">[**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) é implementado.</span><span class="sxs-lookup"><span data-stu-id="d3c6d-120">[**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) is implemented.</span></span> <span data-ttu-id="d3c6d-121">[**INapComponentConfig:: GetConfig**](inapcomponentconfig-getconfig.md) e [**INapComponentConfig:: setconfig**](inapcomponentconfig-setconfig.md) podem ser chamados remotamente usando DCOM.</span><span class="sxs-lookup"><span data-stu-id="d3c6d-121">[**INapComponentConfig::GetConfig**](inapcomponentconfig-getconfig.md) and [**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md) can be called remotely using DCOM.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3c6d-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3c6d-122">Return value</span></span>

<span data-ttu-id="d3c6d-123">Retorna S \_ OK se for bem-sucedido ou um dos códigos de erro padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="d3c6d-123">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3c6d-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3c6d-124">Remarks</span></span>

<span data-ttu-id="d3c6d-125">Se nem [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) nem [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) forem implementados, a configuração remota do SHV não será possível.</span><span class="sxs-lookup"><span data-stu-id="d3c6d-125">If neither [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) nor [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) are implemented, remote configuration of the SHV is not possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3c6d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3c6d-126">Requirements</span></span>



| <span data-ttu-id="d3c6d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3c6d-127">Requirement</span></span> | <span data-ttu-id="d3c6d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d3c6d-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c6d-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3c6d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d3c6d-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d3c6d-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d3c6d-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3c6d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d3c6d-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d3c6d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d3c6d-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3c6d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3c6d-134"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3c6d-134"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3c6d-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="d3c6d-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d3c6d-136"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3c6d-136"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3c6d-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3c6d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c6d-138">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="d3c6d-138">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





