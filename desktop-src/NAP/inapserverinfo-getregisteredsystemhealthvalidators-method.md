---
title: Método INapServerInfo GetRegisteredSystemHealthValidators (NapServerManagement. h)
description: Recupera uma lista de SHVs registrados.
ms.assetid: 029c7d5c-b397-415c-a530-0096de1ef771
keywords:
- Método GetRegisteredSystemHealthValidators NAP
- Método GetRegisteredSystemHealthValidators NAP, interface INapServerInfo
- INapServerInfo interface NAP, método GetRegisteredSystemHealthValidators
topic_type:
- apiref
api_name:
- INapServerInfo.GetRegisteredSystemHealthValidators
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ffdd4d363c994efbecdb57fe4ad7203393fd1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009635"
---
# <a name="inapserverinfogetregisteredsystemhealthvalidators-method"></a><span data-ttu-id="d4bc8-106">Método INapServerInfo:: GetRegisteredSystemHealthValidators</span><span class="sxs-lookup"><span data-stu-id="d4bc8-106">INapServerInfo::GetRegisteredSystemHealthValidators method</span></span>

> [!Note]  
> <span data-ttu-id="d4bc8-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="d4bc8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d4bc8-108">O método **INapServerInfo:: GetRegisteredSystemHealthValidators** recupera uma lista de SHVs registrados.</span><span class="sxs-lookup"><span data-stu-id="d4bc8-108">The **INapServerInfo::GetRegisteredSystemHealthValidators** method retrieves a list of registered SHVs.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4bc8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4bc8-109">Syntax</span></span>


```C++
HRESULT GetRegisteredSystemHealthValidators(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **validators,
  [out] CLSID                        **validatorClsids
);
```



## <a name="parameters"></a><span data-ttu-id="d4bc8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4bc8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4bc8-111">*contagem* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="d4bc8-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4bc8-112">Um ponteiro para um [**SystemHealthEntityCount**](nap-type-constants.md) que contém o número de SHVs registrados.</span><span class="sxs-lookup"><span data-stu-id="d4bc8-112">A pointer to a [**SystemHealthEntityCount**](nap-type-constants.md) that contains the number of registered SHVs.</span></span>

</dd> <dt>

<span data-ttu-id="d4bc8-113">*validadores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d4bc8-113">*validators* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4bc8-114">Um ponteiro para um ponteiro para uma estrutura [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contém as informações de registro de SHV.</span><span class="sxs-lookup"><span data-stu-id="d4bc8-114">A pointer to a pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the SHV registration information.</span></span>

</dd> <dt>

<span data-ttu-id="d4bc8-115">*validatorClsids* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d4bc8-115">*validatorClsids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4bc8-116">Ponteiro para uma matriz de IDs para os SHVs registrados.</span><span class="sxs-lookup"><span data-stu-id="d4bc8-116">Pointer to an array of IDs for the registered SHVs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4bc8-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4bc8-117">Return value</span></span>

<span data-ttu-id="d4bc8-118">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="d4bc8-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="d4bc8-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d4bc8-119">Return code</span></span>                                                                                     | <span data-ttu-id="d4bc8-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4bc8-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d4bc8-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d4bc8-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="d4bc8-122">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d4bc8-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d4bc8-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d4bc8-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="d4bc8-124">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="d4bc8-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="d4bc8-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d4bc8-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="d4bc8-126">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="d4bc8-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d4bc8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4bc8-127">Requirements</span></span>



| <span data-ttu-id="d4bc8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4bc8-128">Requirement</span></span> | <span data-ttu-id="d4bc8-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d4bc8-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4bc8-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4bc8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d4bc8-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d4bc8-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="d4bc8-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4bc8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d4bc8-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d4bc8-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d4bc8-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4bc8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4bc8-135"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4bc8-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4bc8-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="d4bc8-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d4bc8-137"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4bc8-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="d4bc8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d4bc8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4bc8-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4bc8-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="d4bc8-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4bc8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4bc8-141">**NapComponentRegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="d4bc8-141">**NapComponentRegistrationInfo**</span></span>](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)
</dt> <dt>

[<span data-ttu-id="d4bc8-142">**INapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="d4bc8-142">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> </dl>

 

 





