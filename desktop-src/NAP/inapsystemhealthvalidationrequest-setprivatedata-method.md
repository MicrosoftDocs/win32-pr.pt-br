---
title: Método INapSystemHealthValidationRequest SetPrivateData (NapSystemHealthValidator. h)
description: Permite que o NapServer armazene informações de estado.
ms.assetid: 128f9beb-e5da-4b20-bf5e-fcf064209da3
keywords:
- Método SetPrivateData NAP
- Método SetPrivateData NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, método SetPrivateData
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da50ca236c08388632e17916decee162b3b71743
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644830"
---
# <a name="inapsystemhealthvalidationrequestsetprivatedata-method"></a><span data-ttu-id="78f54-106">Método INapSystemHealthValidationRequest:: SetPrivateData</span><span class="sxs-lookup"><span data-stu-id="78f54-106">INapSystemHealthValidationRequest::SetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="78f54-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="78f54-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="78f54-108">O método **INapSystemHealthValidationRequest:: SetPrivateData** permite que o NapServer armazene informações de estado.</span><span class="sxs-lookup"><span data-stu-id="78f54-108">The **INapSystemHealthValidationRequest::SetPrivateData** method allows the NapServer to store state information.</span></span>

## <a name="syntax"></a><span data-ttu-id="78f54-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78f54-109">Syntax</span></span>


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="78f54-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78f54-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78f54-111">*privateData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78f54-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78f54-112">Um ponteiro para um blob de dados [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que contém as informações de estado opaco.</span><span class="sxs-lookup"><span data-stu-id="78f54-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data blob that contains the opaque state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78f54-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78f54-113">Return value</span></span>

<span data-ttu-id="78f54-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="78f54-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="78f54-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="78f54-115">Return code</span></span>                                                                                     | <span data-ttu-id="78f54-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="78f54-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="78f54-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="78f54-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="78f54-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="78f54-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="78f54-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="78f54-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="78f54-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="78f54-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="78f54-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="78f54-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="78f54-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="78f54-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="78f54-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="78f54-123">Remarks</span></span>

<span data-ttu-id="78f54-124">Somente o NapServer pode interpretar o blob de dados.</span><span class="sxs-lookup"><span data-stu-id="78f54-124">Only the NapServer can interpret the data blob.</span></span>

## <a name="requirements"></a><span data-ttu-id="78f54-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78f54-125">Requirements</span></span>



| <span data-ttu-id="78f54-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="78f54-126">Requirement</span></span> | <span data-ttu-id="78f54-127">Valor</span><span class="sxs-lookup"><span data-stu-id="78f54-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78f54-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78f54-128">Minimum supported client</span></span><br/> | <span data-ttu-id="78f54-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="78f54-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="78f54-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78f54-130">Minimum supported server</span></span><br/> | <span data-ttu-id="78f54-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="78f54-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="78f54-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78f54-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="78f54-133"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="78f54-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="78f54-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="78f54-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="78f54-135"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="78f54-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="78f54-136">DLL</span><span class="sxs-lookup"><span data-stu-id="78f54-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78f54-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78f54-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="78f54-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="78f54-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78f54-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="78f54-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





