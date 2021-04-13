---
title: Método INapEnforcementClientConnection SetSoHResponse (NapEnforcementClient. h)
description: Define o SoH-Response e é usado pelo cliente de imposição no recebimento de um pacote.
ms.assetid: 718669c7-73cf-44f4-8463-c59fdbe215cc
keywords:
- Método SetSoHResponse NAP
- Método SetSoHResponse NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método SetSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdc403a1ff68e28f7d262e64ebe558226741b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455585"
---
# <a name="inapenforcementclientconnectionsetsohresponse-method"></a><span data-ttu-id="fe3fa-106">Método INapEnforcementClientConnection:: SetSoHResponse</span><span class="sxs-lookup"><span data-stu-id="fe3fa-106">INapEnforcementClientConnection::SetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="fe3fa-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="fe3fa-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fe3fa-108">O método **INapEnforcementClientConnection:: SetSoHResponse** define o SoH-Response e é usado pelo cliente de imposição no recebimento de um pacote.</span><span class="sxs-lookup"><span data-stu-id="fe3fa-108">The **INapEnforcementClientConnection::SetSoHResponse** method sets the SoH-Response and is used by the enforcement client on receiving a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe3fa-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe3fa-109">Syntax</span></span>


```C++
HRESULT SetSoHResponse(
  [in] const NetworkSoHResponse *sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="fe3fa-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe3fa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe3fa-111">*sohResponse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe3fa-111">*sohResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe3fa-112">Um ponteiro para uma estrutura [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) exclusiva, que é um blob de dados opaco para o aplicador.</span><span class="sxs-lookup"><span data-stu-id="fe3fa-112">A pointer to a unique [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe3fa-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe3fa-113">Return value</span></span>

<span data-ttu-id="fe3fa-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="fe3fa-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="fe3fa-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fe3fa-115">Return code</span></span>                                                                                     | <span data-ttu-id="fe3fa-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe3fa-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe3fa-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fe3fa-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="fe3fa-118">O pacote SoH é válido.</span><span class="sxs-lookup"><span data-stu-id="fe3fa-118">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="fe3fa-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="fe3fa-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="fe3fa-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="fe3fa-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="fe3fa-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fe3fa-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="fe3fa-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="fe3fa-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fe3fa-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe3fa-123">Remarks</span></span>

<span data-ttu-id="fe3fa-124">Um pacote de tamanho zero é válido.</span><span class="sxs-lookup"><span data-stu-id="fe3fa-124">A zero-sized packet is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe3fa-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe3fa-125">Requirements</span></span>



| <span data-ttu-id="fe3fa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe3fa-126">Requirement</span></span> | <span data-ttu-id="fe3fa-127">Valor</span><span class="sxs-lookup"><span data-stu-id="fe3fa-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3fa-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe3fa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fe3fa-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe3fa-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fe3fa-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe3fa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fe3fa-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe3fa-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fe3fa-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe3fa-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe3fa-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe3fa-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe3fa-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="fe3fa-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fe3fa-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fe3fa-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="fe3fa-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fe3fa-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe3fa-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe3fa-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="fe3fa-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe3fa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe3fa-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="fe3fa-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





