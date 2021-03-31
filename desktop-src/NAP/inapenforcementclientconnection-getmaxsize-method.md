---
title: Método getmaxsize INapEnforcementClientConnection (NapEnforcementClient. h)
description: Obtém o tamanho máximo do pacote SoH para este cliente.
ms.assetid: 054bc783-db5d-4801-8984-6b8a131744a2
keywords:
- Método getmaxsize NAP
- Método getmaxsize NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método getmaxsize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3d86cc71cd5da906146ab1577d58311d167d484
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644508"
---
# <a name="inapenforcementclientconnectiongetmaxsize-method"></a><span data-ttu-id="abc05-106">Método INapEnforcementClientConnection:: getmaxsize</span><span class="sxs-lookup"><span data-stu-id="abc05-106">INapEnforcementClientConnection::GetMaxSize method</span></span>

> [!Note]  
> <span data-ttu-id="abc05-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="abc05-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="abc05-108">O método **INapEnforcementClientConnection:: getmaxsize** Obtém o tamanho máximo do pacote soh para esse cliente.</span><span class="sxs-lookup"><span data-stu-id="abc05-108">The **INapEnforcementClientConnection::GetMaxSize** method gets the maximum size of the SoH packet for this client.</span></span>

## <a name="syntax"></a><span data-ttu-id="abc05-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abc05-109">Syntax</span></span>


```C++
HRESULT GetMaxSize(
  [out] ProtocolMaxSize *maxSize
);
```



## <a name="parameters"></a><span data-ttu-id="abc05-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abc05-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abc05-111">*MaxSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="abc05-111">*maxSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abc05-112">Um ponteiro para um [**ProtocolMaxSize**](nap-datatypes.md) que indica o tamanho máximo, em bytes, do pacote soh.</span><span class="sxs-lookup"><span data-stu-id="abc05-112">A pointer to a [**ProtocolMaxSize**](nap-datatypes.md) that indicates the maximum size, in bytes, of the SoH packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abc05-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="abc05-113">Return value</span></span>

<span data-ttu-id="abc05-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="abc05-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="abc05-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="abc05-115">Return code</span></span>                                                                                     | <span data-ttu-id="abc05-116">Description</span><span class="sxs-lookup"><span data-stu-id="abc05-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="abc05-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="abc05-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="abc05-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="abc05-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="abc05-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="abc05-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="abc05-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="abc05-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="abc05-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="abc05-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="abc05-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="abc05-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="abc05-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abc05-123">Requirements</span></span>



| <span data-ttu-id="abc05-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="abc05-124">Requirement</span></span> | <span data-ttu-id="abc05-125">Valor</span><span class="sxs-lookup"><span data-stu-id="abc05-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abc05-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abc05-126">Minimum supported client</span></span><br/> | <span data-ttu-id="abc05-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="abc05-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="abc05-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abc05-128">Minimum supported server</span></span><br/> | <span data-ttu-id="abc05-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="abc05-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="abc05-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="abc05-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="abc05-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="abc05-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="abc05-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="abc05-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="abc05-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="abc05-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="abc05-134">DLL</span><span class="sxs-lookup"><span data-stu-id="abc05-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abc05-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abc05-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="abc05-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="abc05-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abc05-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="abc05-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





