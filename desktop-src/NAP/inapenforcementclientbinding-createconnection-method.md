---
title: Método CreateConnection INapEnforcementClientBinding (NapEnforcementClient. h)
description: É usado por imforcers para criar objetos de conexão.
ms.assetid: 4d31928f-1a10-4168-a53c-256cbbf3e5c9
keywords:
- Método CreateConnection NAP
- Método CreateConnection NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, Método CreateConnection
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.CreateConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf530b9fefd0e5b361f4f86ef2421712c750be9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009164"
---
# <a name="inapenforcementclientbindingcreateconnection-method"></a><span data-ttu-id="13b9f-106">Método INapEnforcementClientBinding:: CreateConnection</span><span class="sxs-lookup"><span data-stu-id="13b9f-106">INapEnforcementClientBinding::CreateConnection method</span></span>

> [!Note]  
> <span data-ttu-id="13b9f-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="13b9f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="13b9f-108">O método de fábrica **INapEnforcementClientBinding:: CreateConnection** é usado por imforcers para criar objetos de conexão.</span><span class="sxs-lookup"><span data-stu-id="13b9f-108">The **INapEnforcementClientBinding::CreateConnection** factory method is used by enforcers to create connection objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="13b9f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13b9f-109">Syntax</span></span>


```C++
HRESULT CreateConnection(
  [out] INapEnforcementClientConnection **connection
);
```



## <a name="parameters"></a><span data-ttu-id="13b9f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13b9f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13b9f-111">*conexão* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="13b9f-111">*connection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13b9f-112">Um ponteiro COM para uma nova interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) retornada pelo sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="13b9f-112">A COM pointer to a new [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface returned by the NAP system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13b9f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="13b9f-113">Return value</span></span>

<span data-ttu-id="13b9f-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="13b9f-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="13b9f-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="13b9f-115">Return code</span></span>                                                                                     | <span data-ttu-id="13b9f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="13b9f-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="13b9f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="13b9f-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="13b9f-118">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="13b9f-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="13b9f-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="13b9f-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="13b9f-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="13b9f-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="13b9f-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="13b9f-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="13b9f-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="13b9f-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="13b9f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="13b9f-123">Remarks</span></span>

<span data-ttu-id="13b9f-124">O cliente de imposição deve chamar o método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de chamar este ou qualquer outro método da interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="13b9f-124">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="13b9f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13b9f-125">Requirements</span></span>



| <span data-ttu-id="13b9f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="13b9f-126">Requirement</span></span> | <span data-ttu-id="13b9f-127">Valor</span><span class="sxs-lookup"><span data-stu-id="13b9f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13b9f-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13b9f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="13b9f-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="13b9f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="13b9f-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13b9f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="13b9f-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="13b9f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="13b9f-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="13b9f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="13b9f-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="13b9f-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="13b9f-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="13b9f-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="13b9f-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="13b9f-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="13b9f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="13b9f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13b9f-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13b9f-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="13b9f-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="13b9f-138">See also</span></span>

<dl> <span data-ttu-id="13b9f-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="13b9f-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="13b9f-140">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="13b9f-140">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="13b9f-141">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="13b9f-141">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





