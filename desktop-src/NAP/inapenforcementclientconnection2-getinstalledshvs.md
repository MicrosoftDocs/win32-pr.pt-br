---
title: Método INapEnforcementClientConnection2 GetInstalledShvs (NapEnforcementClient. h)
description: Usado pelo agente NAP para consultar os SHVs (validadores da integridade do sistema) instalados no cliente.
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- Método GetInstalledShvs NAP
- Método GetInstalledShvs NAP, interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP, método GetInstalledShvs
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa54d09a0c3d3c524262231982f662c497920a0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456026"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a><span data-ttu-id="8de0e-106">Método INapEnforcementClientConnection2:: GetInstalledShvs</span><span class="sxs-lookup"><span data-stu-id="8de0e-106">INapEnforcementClientConnection2::GetInstalledShvs method</span></span>

> [!Note]  
> <span data-ttu-id="8de0e-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="8de0e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8de0e-108">O método **GetInstalledShvs** é usado pelo agente NAP para consultar os SHVs (validadores da integridade do sistema) instalados no cliente.</span><span class="sxs-lookup"><span data-stu-id="8de0e-108">The **GetInstalledShvs** method is used by the NAP Agent to query the installed System Health Validators (SHVs) on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="8de0e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8de0e-109">Syntax</span></span>


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a><span data-ttu-id="8de0e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8de0e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8de0e-111">*contagem* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="8de0e-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8de0e-112">Um ponteiro para um valor de [SystemHealthEntityCount](nap-datatypes.md) que especifica o número de SHVs instalados em *IDs*.</span><span class="sxs-lookup"><span data-stu-id="8de0e-112">A pointer to a [SystemHealthEntityCount](nap-datatypes.md) value that specifies the number of installed SHVs in *ids*.</span></span>

</dd> <dt>

<span data-ttu-id="8de0e-113">*IDs* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="8de0e-113">*ids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8de0e-114">Um ponteiro para uma matriz de valores [SystemHealthEntityId](nap-datatypes.md) que contêm as IDs SHV instaladas.</span><span class="sxs-lookup"><span data-stu-id="8de0e-114">A pointer to an array of [SystemHealthEntityId](nap-datatypes.md) values that contain the installed SHV IDs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8de0e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8de0e-115">Return value</span></span>

<span data-ttu-id="8de0e-116">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="8de0e-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="8de0e-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8de0e-117">Return code</span></span>                                                                                   | <span data-ttu-id="8de0e-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="8de0e-118">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="8de0e-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8de0e-119"><dt>**S\_OK** </dt></span></span> </dl>         | <span data-ttu-id="8de0e-120">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8de0e-120">Operation succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="8de0e-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8de0e-121"><dt>**E\_INVALIDARG** </dt></span></span> </dl> | <span data-ttu-id="8de0e-122">Um argumento inválido foi passado para o método.</span><span class="sxs-lookup"><span data-stu-id="8de0e-122">An invalid argument was passed to the method.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8de0e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8de0e-123">Requirements</span></span>



| <span data-ttu-id="8de0e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8de0e-124">Requirement</span></span> | <span data-ttu-id="8de0e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8de0e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8de0e-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8de0e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8de0e-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8de0e-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8de0e-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8de0e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8de0e-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8de0e-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8de0e-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8de0e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8de0e-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="8de0e-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="8de0e-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="8de0e-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8de0e-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8de0e-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="8de0e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8de0e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8de0e-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8de0e-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="8de0e-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="8de0e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8de0e-137">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="8de0e-137">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





