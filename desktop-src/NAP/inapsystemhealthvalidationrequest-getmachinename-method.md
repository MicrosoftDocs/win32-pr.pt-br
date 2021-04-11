---
title: Método GetMachineName de INapSystemHealthValidationRequest (NapSystemHealthValidator. h)
description: É usado por SHVs (validadores da integridade do sistema) para recuperar o nome do computador do cliente NAP. Em seguida, o SHV registra essas informações.
ms.assetid: 2ea6a65d-1579-4a05-b5bc-aebf6421e46a
keywords:
- Método GetMachineName NAP
- Método GetMachineName NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, método GetMachineName
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetMachineName
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1c3e264d7d2d6e4d93e3ad71d7f3adc92ff8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086498"
---
# <a name="inapsystemhealthvalidationrequestgetmachinename-method"></a><span data-ttu-id="2f918-107">Método INapSystemHealthValidationRequest:: GetMachineName</span><span class="sxs-lookup"><span data-stu-id="2f918-107">INapSystemHealthValidationRequest::GetMachineName method</span></span>

> [!Note]  
> <span data-ttu-id="2f918-108">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="2f918-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2f918-109">O método **INapSystemHealthValidationRequest:: GetMachineName** é usado pelos SHVs (validadores da integridade do sistema) para recuperar o nome do computador do cliente NAP.</span><span class="sxs-lookup"><span data-stu-id="2f918-109">The **INapSystemHealthValidationRequest::GetMachineName** method is used by System Health Validators (SHVs) to retrieve the machine name of the NAP client.</span></span> <span data-ttu-id="2f918-110">Em seguida, o SHV registra essas informações.</span><span class="sxs-lookup"><span data-stu-id="2f918-110">The SHV then logs this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f918-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f918-111">Syntax</span></span>


```C++
HRESULT GetMachineName(
  [out] CountedString **machineName
);
```



## <a name="parameters"></a><span data-ttu-id="2f918-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f918-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f918-113">*MachineName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2f918-113">*machineName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f918-114">Um ponteiro para um ponteiro para uma estrutura de [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém o nome do computador do cliente NAP.</span><span class="sxs-lookup"><span data-stu-id="2f918-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the machine name of the NAP client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f918-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f918-115">Return value</span></span>

<span data-ttu-id="2f918-116">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="2f918-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="2f918-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2f918-117">Return code</span></span>                                                                                     | <span data-ttu-id="2f918-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f918-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f918-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2f918-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="2f918-120">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2f918-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2f918-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="2f918-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="2f918-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="2f918-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="2f918-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2f918-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="2f918-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="2f918-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2f918-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f918-125">Requirements</span></span>



| <span data-ttu-id="2f918-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f918-126">Requirement</span></span> | <span data-ttu-id="2f918-127">Valor</span><span class="sxs-lookup"><span data-stu-id="2f918-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f918-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f918-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2f918-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2f918-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="2f918-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f918-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2f918-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2f918-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f918-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f918-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f918-133"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f918-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f918-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="2f918-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2f918-135"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2f918-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="2f918-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2f918-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f918-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f918-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="2f918-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f918-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f918-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="2f918-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





