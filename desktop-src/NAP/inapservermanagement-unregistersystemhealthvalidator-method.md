---
title: Método INapServerManagement UnregisterSystemHealthValidator (NapServerManagement. h)
description: É usado para cancelar o registro de um SHV com o servidor NAP.
ms.assetid: f4148df1-a230-4845-ac8b-9e04be9e0d6c
keywords:
- Método UnregisterSystemHealthValidator NAP
- Método UnregisterSystemHealthValidator NAP, interface INapServerManagement
- INapServerManagement interface NAP, método UnregisterSystemHealthValidator
topic_type:
- apiref
api_name:
- INapServerManagement.UnregisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0715445504b862d9ae9e8478b543f8e80378f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499658"
---
# <a name="inapservermanagementunregistersystemhealthvalidator-method"></a><span data-ttu-id="42d4c-106">Método INapServerManagement:: UnregisterSystemHealthValidator</span><span class="sxs-lookup"><span data-stu-id="42d4c-106">INapServerManagement::UnregisterSystemHealthValidator method</span></span>

> [!Note]  
> <span data-ttu-id="42d4c-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="42d4c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="42d4c-108">O método **INapServerManagement:: UnregisterSystemHealthValidator** é usado para cancelar o registro de um SHV com o servidor NAP.</span><span class="sxs-lookup"><span data-stu-id="42d4c-108">The **INapServerManagement::UnregisterSystemHealthValidator** method is used to unregister an SHV with the NAP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="42d4c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42d4c-109">Syntax</span></span>


```C++
HRESULT UnregisterSystemHealthValidator(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="42d4c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42d4c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42d4c-111">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="42d4c-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d4c-112">Um [**SystemHealthEntityId**](nap-type-constants.md) que contém o identificador exclusivo do SHV para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="42d4c-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHV to unregister.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42d4c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42d4c-113">Return value</span></span>

<span data-ttu-id="42d4c-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="42d4c-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="42d4c-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="42d4c-115">Return code</span></span>                                                                                     | <span data-ttu-id="42d4c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="42d4c-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="42d4c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="42d4c-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="42d4c-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="42d4c-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="42d4c-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="42d4c-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="42d4c-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="42d4c-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="42d4c-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="42d4c-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="42d4c-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="42d4c-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="42d4c-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="42d4c-123">Remarks</span></span>

<span data-ttu-id="42d4c-124">Se houver qualquer chamada assíncrona pendente no SHV, elas serão concluídas posteriormente e serão descartadas.</span><span class="sxs-lookup"><span data-stu-id="42d4c-124">If there are any asynchronous calls pending on the SHV, they will complete at a later time and will be discarded.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d4c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42d4c-125">Requirements</span></span>



| <span data-ttu-id="42d4c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="42d4c-126">Requirement</span></span> | <span data-ttu-id="42d4c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="42d4c-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42d4c-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42d4c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="42d4c-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="42d4c-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="42d4c-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42d4c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="42d4c-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="42d4c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="42d4c-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42d4c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="42d4c-133"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="42d4c-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="42d4c-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="42d4c-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42d4c-135"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42d4c-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="42d4c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="42d4c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42d4c-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42d4c-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="42d4c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="42d4c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d4c-139">**INapServerManagement**</span><span class="sxs-lookup"><span data-stu-id="42d4c-139">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





