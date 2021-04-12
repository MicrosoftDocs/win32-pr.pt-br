---
title: Método INapClientManagement GetNapClientInfo (NapManagement. h)
description: Recupera informações sobre o cliente NAP.
ms.assetid: c0b57cab-729b-40b2-81d2-32a961e377a5
keywords:
- Método GetNapClientInfo NAP
- Método GetNapClientInfo NAP, interface INapClientManagement
- INapClientManagement interface NAP, método GetNapClientInfo
topic_type:
- apiref
api_name:
- INapClientManagement.GetNapClientInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11fc496374f2a7f0b7842e22212013149f44f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499530"
---
# <a name="inapclientmanagementgetnapclientinfo-method"></a><span data-ttu-id="38f80-106">Método INapClientManagement:: GetNapClientInfo</span><span class="sxs-lookup"><span data-stu-id="38f80-106">INapClientManagement::GetNapClientInfo method</span></span>

> [!Note]  
> <span data-ttu-id="38f80-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="38f80-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="38f80-108">O método **GetNapClientInfo** recupera informações sobre o cliente NAP.</span><span class="sxs-lookup"><span data-stu-id="38f80-108">The **GetNapClientInfo** method retrieves information about the NAP client.</span></span>

## <a name="syntax"></a><span data-ttu-id="38f80-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38f80-109">Syntax</span></span>


```C++
HRESULT GetNapClientInfo(
  [out] BOOL          *isNapEnabled,
  [out] CountedString **clientName,
  [out] CountedString **clientDescription,
  [out] CountedString **protocolVersion
) const;
```



## <a name="parameters"></a><span data-ttu-id="38f80-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38f80-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38f80-111">*isNapEnabled* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38f80-111">*isNapEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38f80-112">Um ponteiro para um BOOL que é definido como **true** se a NAP estiver habilitada; caso contrário, ele será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="38f80-112">A pointer to a BOOL that is set to **TRUE** if NAP is enabled; otherwise it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="38f80-113">*clientename* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38f80-113">*clientName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38f80-114">Um ponteiro para um ponteiro para uma estrutura de [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém o nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="38f80-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the client name.</span></span>

</dd> <dt>

<span data-ttu-id="38f80-115">*clientDescription* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38f80-115">*clientDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38f80-116">Um ponteiro para um ponteiro para uma estrutura de [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém a descrição do cliente.</span><span class="sxs-lookup"><span data-stu-id="38f80-116">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the client description.</span></span>

</dd> <dt>

<span data-ttu-id="38f80-117">*protocolVersion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38f80-117">*protocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38f80-118">Um ponteiro para um ponteiro para uma estrutura de [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém a versão do protocolo.</span><span class="sxs-lookup"><span data-stu-id="38f80-118">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38f80-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38f80-119">Return value</span></span>

<span data-ttu-id="38f80-120">O método retorna um código de status HRESULT, incluindo, mas não se limitando a um dos itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="38f80-120">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="38f80-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="38f80-121">Return code</span></span>                                                                                         | <span data-ttu-id="38f80-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="38f80-122">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="38f80-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="38f80-123"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="38f80-124">Operação concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="38f80-124">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="38f80-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="38f80-125"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="38f80-126">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="38f80-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="38f80-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="38f80-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="38f80-128">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="38f80-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="38f80-129"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="38f80-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="38f80-130">O NapAgent não está em execução.</span><span class="sxs-lookup"><span data-stu-id="38f80-130">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="38f80-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38f80-131">Requirements</span></span>



| <span data-ttu-id="38f80-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="38f80-132">Requirement</span></span> | <span data-ttu-id="38f80-133">Valor</span><span class="sxs-lookup"><span data-stu-id="38f80-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="38f80-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38f80-134">Minimum supported client</span></span><br/> | <span data-ttu-id="38f80-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38f80-135">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="38f80-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38f80-136">Minimum supported server</span></span><br/> | <span data-ttu-id="38f80-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="38f80-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="38f80-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38f80-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="38f80-139"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="38f80-139"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="38f80-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="38f80-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="38f80-141"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="38f80-141"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="38f80-142">DLL</span><span class="sxs-lookup"><span data-stu-id="38f80-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38f80-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38f80-143"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="38f80-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="38f80-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f80-145">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="38f80-145">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





