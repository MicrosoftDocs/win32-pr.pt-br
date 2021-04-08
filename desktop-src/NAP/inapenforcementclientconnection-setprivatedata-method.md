---
title: Método INapEnforcementClientConnection SetPrivateData (NapEnforcementClient. h)
description: É usado pelo NapAgent para definir dados privados.
ms.assetid: 2559a612-8857-4e60-b5bc-dd8235ff69f9
keywords:
- Método SetPrivateData NAP
- Método SetPrivateData NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método SetPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e73248e546b1f0e48438553877f0523bd30b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009160"
---
# <a name="inapenforcementclientconnectionsetprivatedata-method"></a><span data-ttu-id="010e3-106">Método INapEnforcementClientConnection:: SetPrivateData</span><span class="sxs-lookup"><span data-stu-id="010e3-106">INapEnforcementClientConnection::SetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="010e3-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="010e3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="010e3-108">O método **INapEnforcementClientConnection:: SetPrivateData** é usado pelo NapAgent para definir dados privados.</span><span class="sxs-lookup"><span data-stu-id="010e3-108">The **INapEnforcementClientConnection::SetPrivateData** method is used by the NapAgent to set private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="010e3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="010e3-109">Syntax</span></span>


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="010e3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="010e3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="010e3-111">*privateData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="010e3-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="010e3-112">Um ponteiro para um blob de dados [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que somente o NapAgent pode interpretar.</span><span class="sxs-lookup"><span data-stu-id="010e3-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data blob that only the NapAgent can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="010e3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="010e3-113">Return value</span></span>

<span data-ttu-id="010e3-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="010e3-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="010e3-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="010e3-115">Return code</span></span>                                                                                     | <span data-ttu-id="010e3-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="010e3-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="010e3-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="010e3-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="010e3-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="010e3-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="010e3-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="010e3-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="010e3-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="010e3-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="010e3-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="010e3-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="010e3-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="010e3-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="010e3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="010e3-123">Requirements</span></span>



| <span data-ttu-id="010e3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="010e3-124">Requirement</span></span> | <span data-ttu-id="010e3-125">Valor</span><span class="sxs-lookup"><span data-stu-id="010e3-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="010e3-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="010e3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="010e3-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="010e3-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="010e3-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="010e3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="010e3-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="010e3-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="010e3-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="010e3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="010e3-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="010e3-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="010e3-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="010e3-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="010e3-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="010e3-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="010e3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="010e3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="010e3-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="010e3-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="010e3-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="010e3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="010e3-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="010e3-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





