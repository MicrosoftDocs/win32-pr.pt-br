---
title: Método INapEnforcementClientConnection SetIsolationInfo (NapEnforcementClient. h)
description: É usado pelo NapAgent para definir as informações de isolamento do cliente.
ms.assetid: e92d8762-4ae9-40e5-a18e-7da757aa6f9e
keywords:
- Método SetIsolationInfo NAP
- Método SetIsolationInfo NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método SetIsolationInfo
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1cfd7ad227fec6942e0660769f52b3d4f12201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644506"
---
# <a name="inapenforcementclientconnectionsetisolationinfo-method"></a><span data-ttu-id="bbb60-106">Método INapEnforcementClientConnection:: SetIsolationInfo</span><span class="sxs-lookup"><span data-stu-id="bbb60-106">INapEnforcementClientConnection::SetIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="bbb60-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="bbb60-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bbb60-108">O método **INapEnforcementClientConnection:: SetIsolationInfo** é usado pelo NapAgent para definir as informações de isolamento do cliente.</span><span class="sxs-lookup"><span data-stu-id="bbb60-108">The **INapEnforcementClientConnection::SetIsolationInfo** method is used by the NapAgent to set the isolation information of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbb60-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbb60-109">Syntax</span></span>


```C++
HRESULT SetIsolationInfo(
  [in] const IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="bbb60-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbb60-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbb60-111">*isolationInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bbb60-111">*isolationInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbb60-112">Um ponteiro para uma estrutura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que contém o estado de conectividade do cliente.</span><span class="sxs-lookup"><span data-stu-id="bbb60-112">A pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbb60-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bbb60-113">Return value</span></span>

<span data-ttu-id="bbb60-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="bbb60-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="bbb60-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bbb60-115">Return code</span></span>                                                                                     | <span data-ttu-id="bbb60-116">Description</span><span class="sxs-lookup"><span data-stu-id="bbb60-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="bbb60-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bbb60-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="bbb60-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bbb60-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bbb60-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="bbb60-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="bbb60-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="bbb60-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="bbb60-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bbb60-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="bbb60-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="bbb60-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bbb60-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbb60-123">Remarks</span></span>

<span data-ttu-id="bbb60-124">Essas informações são definidas pelo NapAgent após o processamento de um SoHResponse e não devem ser definidas pelo aplicador.</span><span class="sxs-lookup"><span data-stu-id="bbb60-124">This information is set by NapAgent after processing an SoHResponse and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbb60-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbb60-125">Requirements</span></span>



| <span data-ttu-id="bbb60-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbb60-126">Requirement</span></span> | <span data-ttu-id="bbb60-127">Valor</span><span class="sxs-lookup"><span data-stu-id="bbb60-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbb60-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbb60-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bbb60-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bbb60-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bbb60-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbb60-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bbb60-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bbb60-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bbb60-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bbb60-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbb60-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbb60-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="bbb60-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="bbb60-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bbb60-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bbb60-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="bbb60-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bbb60-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbb60-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbb60-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="bbb60-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bbb60-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbb60-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="bbb60-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





