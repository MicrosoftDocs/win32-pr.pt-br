---
title: Método INapEnforcementClientConnection2 SetInstalledShvs (NapEnforcementClient. h)
description: Usado pelo agente NAP para definir os SHVs (validadores da integridade do sistema) instalados no cliente.
ms.assetid: 38aa99b9-a15a-414d-91fc-128de8f5a654
keywords:
- Método SetInstalledShvs NAP
- Método SetInstalledShvs NAP, interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP, método SetInstalledShvs
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6651cd5248094f82d9faa1862492f82648e94125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086500"
---
# <a name="inapenforcementclientconnection2setinstalledshvs-method"></a><span data-ttu-id="7a86b-106">Método INapEnforcementClientConnection2:: SetInstalledShvs</span><span class="sxs-lookup"><span data-stu-id="7a86b-106">INapEnforcementClientConnection2::SetInstalledShvs method</span></span>

> [!Note]  
> <span data-ttu-id="7a86b-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="7a86b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7a86b-108">O método **SetInstalledShvs** é usado pelo agente NAP para definir os SHVs (validadores da integridade do sistema) instalados no cliente.</span><span class="sxs-lookup"><span data-stu-id="7a86b-108">The **SetInstalledShvs** method is used by the NAP Agent to set the installed System Health Validators (SHVs) on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a86b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a86b-109">Syntax</span></span>


```C++
HRESULT SetInstalledShvs(
  [in] SystemHealthEntityCount count,
  [in] SystemHealthEntityId    *ids
);
```



## <a name="parameters"></a><span data-ttu-id="7a86b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a86b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a86b-111">*contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="7a86b-111">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a86b-112">Um valor de [SystemHealthEntityCount](nap-datatypes.md) que especifica o número de SHVs a serem instalados em *IDs*.</span><span class="sxs-lookup"><span data-stu-id="7a86b-112">A [SystemHealthEntityCount](nap-datatypes.md) value that specifies the number of SHVs to install in *ids*.</span></span>

</dd> <dt>

<span data-ttu-id="7a86b-113">*IDs* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7a86b-113">*ids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a86b-114">Um ponteiro para um valor de [SystemHealthEntityId](nap-datatypes.md) que contém uma lista de IDs de SHV a serem instaladas.</span><span class="sxs-lookup"><span data-stu-id="7a86b-114">A pointer to a [SystemHealthEntityId](nap-datatypes.md) value that contains a list of SHV IDs to install.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a86b-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a86b-115">Return value</span></span>

<span data-ttu-id="7a86b-116">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="7a86b-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="7a86b-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7a86b-117">Return code</span></span>                                                                                  | <span data-ttu-id="7a86b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="7a86b-118">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="7a86b-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7a86b-119"><dt>**S\_OK** </dt></span></span> </dl>        | <span data-ttu-id="7a86b-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7a86b-120">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="7a86b-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7a86b-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="7a86b-122">O parâmetro de *contagem* era 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="7a86b-122">The *count* parameter was 0 (zero).</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7a86b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a86b-123">Requirements</span></span>



| <span data-ttu-id="7a86b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a86b-124">Requirement</span></span> | <span data-ttu-id="7a86b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7a86b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a86b-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a86b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7a86b-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a86b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7a86b-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a86b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7a86b-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7a86b-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7a86b-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a86b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a86b-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a86b-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a86b-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="7a86b-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7a86b-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7a86b-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="7a86b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7a86b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a86b-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a86b-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="7a86b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a86b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a86b-137">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="7a86b-137">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





