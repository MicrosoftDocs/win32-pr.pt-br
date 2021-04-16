---
title: Método getconfigid de INapSystemHealthValidationRequest2 (NapSystemHealthValidator. h)
description: Usado pelos SHVs (validadores da integridade do sistema) para recuperar a ID de configuração em uma solicitação de validação.
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- Método getconfigid NAP
- Método getconfigid NAP, interface INapSystemHealthValidationRequest2
- INapSystemHealthValidationRequest2 interface NAP, método getconfigid
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2.GetConfigID
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3b41d2f08dc117fd28e704d607c628ec73e6ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757766"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a><span data-ttu-id="8980a-106">Método INapSystemHealthValidationRequest2:: getconfigid</span><span class="sxs-lookup"><span data-stu-id="8980a-106">INapSystemHealthValidationRequest2::GetConfigID method</span></span>

> [!Note]  
> <span data-ttu-id="8980a-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="8980a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8980a-108">O método **INapSystemHealthValidationRequest2:: Getconfigid** é usado pelos SHVs (validadores da integridade do sistema) para recuperar a ID de configuração em uma solicitação de validação.</span><span class="sxs-lookup"><span data-stu-id="8980a-108">The **INapSystemHealthValidationRequest2::GetConfigId** method is used by the System Health Validators (SHVs) to retrieve the configuration ID in a validation request.</span></span>

## <a name="syntax"></a><span data-ttu-id="8980a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8980a-109">Syntax</span></span>


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a><span data-ttu-id="8980a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8980a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8980a-111">*configid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8980a-111">*configID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8980a-112">No retorno, um ponteiro para UINT32 que contém uma ID de configuração do SHV.</span><span class="sxs-lookup"><span data-stu-id="8980a-112">On return, a pointer to UINT32 that contains a configuration ID of the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8980a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8980a-113">Return value</span></span>

<span data-ttu-id="8980a-114">Retorna um dos seguintes códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="8980a-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="8980a-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8980a-115">Return code</span></span>                                                                                  | <span data-ttu-id="8980a-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8980a-116">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="8980a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8980a-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="8980a-118">Operação concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="8980a-118">Operation successful.</span></span><br/>                |
| <dl> <span data-ttu-id="8980a-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8980a-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="8980a-120">O parâmetro configid era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="8980a-120">The configID parameter was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8980a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8980a-121">Requirements</span></span>



| <span data-ttu-id="8980a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8980a-122">Requirement</span></span> | <span data-ttu-id="8980a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8980a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8980a-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8980a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8980a-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8980a-125">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="8980a-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8980a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8980a-127">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="8980a-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8980a-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8980a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8980a-129"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="8980a-129"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="8980a-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="8980a-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8980a-131"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8980a-131"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="8980a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8980a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8980a-133"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8980a-133"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="8980a-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="8980a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8980a-135">**INapSystemHealthValidationRequest2**</span><span class="sxs-lookup"><span data-stu-id="8980a-135">**INapSystemHealthValidationRequest2**</span></span>](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





