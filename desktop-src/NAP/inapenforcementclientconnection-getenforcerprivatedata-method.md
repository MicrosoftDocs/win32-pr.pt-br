---
title: Método INapEnforcementClientConnection GetEnforcerPrivateData (NapEnforcementClient. h)
description: É usado pelo imforcer para obter dados privados.
ms.assetid: a1f5b5a7-c862-4e5b-bf9c-b137f99f6165
keywords:
- Método GetEnforcerPrivateData NAP
- Método GetEnforcerPrivateData NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método GetEnforcerPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592ad0b11abf2b349b0810d67b05f2ee4086060
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086469"
---
# <a name="inapenforcementclientconnectiongetenforcerprivatedata-method"></a><span data-ttu-id="0978b-106">Método INapEnforcementClientConnection:: GetEnforcerPrivateData</span><span class="sxs-lookup"><span data-stu-id="0978b-106">INapEnforcementClientConnection::GetEnforcerPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="0978b-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="0978b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0978b-108">O método **INapEnforcementClientConnection:: GetEnforcerPrivateData** é usado pelo imforcer para obter dados privados.</span><span class="sxs-lookup"><span data-stu-id="0978b-108">The **INapEnforcementClientConnection::GetEnforcerPrivateData** method is used by the enforcer to get private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0978b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0978b-109">Syntax</span></span>


```C++
HRESULT GetEnforcerPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="0978b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0978b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0978b-111">*privateData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0978b-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0978b-112">Um ponteiro para um ponteiro para um blob de dados opaco [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que apenas o imforcer pode interpretar.</span><span class="sxs-lookup"><span data-stu-id="0978b-112">A pointer to a pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the enforcer can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0978b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0978b-113">Return value</span></span>

<span data-ttu-id="0978b-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="0978b-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="0978b-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0978b-115">Return code</span></span>                                                                                     | <span data-ttu-id="0978b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="0978b-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0978b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0978b-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="0978b-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0978b-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0978b-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0978b-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="0978b-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="0978b-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0978b-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0978b-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="0978b-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="0978b-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0978b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0978b-123">Requirements</span></span>



| <span data-ttu-id="0978b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0978b-124">Requirement</span></span> | <span data-ttu-id="0978b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0978b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0978b-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0978b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0978b-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0978b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0978b-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0978b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0978b-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0978b-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0978b-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0978b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0978b-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0978b-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="0978b-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="0978b-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0978b-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0978b-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="0978b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0978b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0978b-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0978b-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="0978b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="0978b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0978b-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="0978b-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





