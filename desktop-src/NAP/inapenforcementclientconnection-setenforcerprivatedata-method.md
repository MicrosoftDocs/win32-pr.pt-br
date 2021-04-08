---
title: Método INapEnforcementClientConnection SetEnforcerPrivateData (NapEnforcementClient. h)
description: É usado pelo imforcer para definir dados privados.
ms.assetid: 56f6fec7-47ec-4b2c-b8c8-a4d519ba0f91
keywords:
- Método SetEnforcerPrivateData NAP
- Método SetEnforcerPrivateData NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método SetEnforcerPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5773294e229a59ff07db8ef546d9d691b369b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009162"
---
# <a name="inapenforcementclientconnectionsetenforcerprivatedata-method"></a><span data-ttu-id="a7183-106">Método INapEnforcementClientConnection:: SetEnforcerPrivateData</span><span class="sxs-lookup"><span data-stu-id="a7183-106">INapEnforcementClientConnection::SetEnforcerPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="a7183-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="a7183-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a7183-108">O método **INapEnforcementClientConnection:: SetEnforcerPrivateData** é usado pelo imforcer para definir dados privados.</span><span class="sxs-lookup"><span data-stu-id="a7183-108">The **INapEnforcementClientConnection::SetEnforcerPrivateData** method is used by the enforcer to set private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7183-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7183-109">Syntax</span></span>


```C++
HRESULT SetEnforcerPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="a7183-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7183-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7183-111">*privateData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a7183-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7183-112">Um ponteiro para um blob de dados opaco [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que apenas o imforcer pode interpretar.</span><span class="sxs-lookup"><span data-stu-id="a7183-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the enforcer can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7183-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a7183-113">Return value</span></span>

<span data-ttu-id="a7183-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="a7183-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a7183-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a7183-115">Return code</span></span>                                                                                     | <span data-ttu-id="a7183-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7183-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a7183-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a7183-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a7183-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a7183-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a7183-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a7183-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a7183-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="a7183-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a7183-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a7183-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a7183-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="a7183-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a7183-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7183-123">Requirements</span></span>



| <span data-ttu-id="a7183-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7183-124">Requirement</span></span> | <span data-ttu-id="a7183-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a7183-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7183-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7183-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a7183-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a7183-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a7183-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7183-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a7183-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a7183-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a7183-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7183-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7183-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7183-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7183-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="a7183-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7183-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7183-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="a7183-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a7183-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7183-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7183-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a7183-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7183-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7183-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="a7183-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





