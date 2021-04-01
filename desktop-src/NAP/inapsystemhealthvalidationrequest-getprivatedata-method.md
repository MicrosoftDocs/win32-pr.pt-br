---
title: Método INapSystemHealthValidationRequest GetPrivateData (NapSystemHealthValidator. h)
description: Permite que o NapServer recupere informações de estado.
ms.assetid: f85026ca-852b-4eb1-9a8c-7e03cd1765f2
keywords:
- Método GetPrivateData NAP
- Método GetPrivateData NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, método GetPrivateData
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d78cceba42cd503ef8a875ece8f4ed196eaeff8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645111"
---
# <a name="inapsystemhealthvalidationrequestgetprivatedata-method"></a><span data-ttu-id="b40c0-106">Método INapSystemHealthValidationRequest:: GetPrivateData</span><span class="sxs-lookup"><span data-stu-id="b40c0-106">INapSystemHealthValidationRequest::GetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="b40c0-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="b40c0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b40c0-108">O método **INapSystemHealthValidationRequest:: GetPrivateData** permite que o NapServer recupere informações de estado.</span><span class="sxs-lookup"><span data-stu-id="b40c0-108">The **INapSystemHealthValidationRequest::GetPrivateData** method allows the NapServer to retrieve state information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b40c0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b40c0-109">Syntax</span></span>


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="b40c0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b40c0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b40c0-111">*privateData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b40c0-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b40c0-112">Um ponteiro para um ponteiro para [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) blob de dados opaco que contém informações de estado.</span><span class="sxs-lookup"><span data-stu-id="b40c0-112">A pointer to a pointer to [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that contains state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b40c0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b40c0-113">Return value</span></span>

<span data-ttu-id="b40c0-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="b40c0-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b40c0-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b40c0-115">Return code</span></span>                                                                                     | <span data-ttu-id="b40c0-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b40c0-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b40c0-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b40c0-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="b40c0-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b40c0-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b40c0-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b40c0-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="b40c0-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="b40c0-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b40c0-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b40c0-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="b40c0-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="b40c0-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b40c0-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="b40c0-123">Remarks</span></span>

<span data-ttu-id="b40c0-124">Somente o NapServer pode interpretar o blob de dados.</span><span class="sxs-lookup"><span data-stu-id="b40c0-124">Only the NapServer can interpret the data blob.</span></span>

## <a name="requirements"></a><span data-ttu-id="b40c0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b40c0-125">Requirements</span></span>



| <span data-ttu-id="b40c0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b40c0-126">Requirement</span></span> | <span data-ttu-id="b40c0-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b40c0-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b40c0-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b40c0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b40c0-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b40c0-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="b40c0-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b40c0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b40c0-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b40c0-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b40c0-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b40c0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b40c0-133"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="b40c0-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="b40c0-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="b40c0-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b40c0-135"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b40c0-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="b40c0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b40c0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b40c0-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b40c0-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="b40c0-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="b40c0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b40c0-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="b40c0-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





