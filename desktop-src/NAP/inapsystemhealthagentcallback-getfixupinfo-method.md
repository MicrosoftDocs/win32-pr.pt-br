---
title: Método INapSystemHealthAgentCallback GetFixupInfo (NapSystemHealthAgent. h)
description: É chamado pelo NapAgent para determinar o estado do agente de integridade do sistema, enquanto ele está processando um SoHResponse.
ms.assetid: cf919b56-3d40-4c49-9c91-25c20ae5ccda
keywords:
- Método GetFixupInfo NAP
- Método GetFixupInfo NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, método GetFixupInfo
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetFixupInfo
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227cbe870c722189c995bff0c967eb187548cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085709"
---
# <a name="inapsystemhealthagentcallbackgetfixupinfo-method"></a><span data-ttu-id="478c7-106">Método INapSystemHealthAgentCallback:: GetFixupInfo</span><span class="sxs-lookup"><span data-stu-id="478c7-106">INapSystemHealthAgentCallback::GetFixupInfo method</span></span>

> [!Note]  
> <span data-ttu-id="478c7-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="478c7-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="478c7-108">O método **INapSystemHealthAgentCallback:: GetFixupInfo** é chamado pelo NapAgent para determinar o estado do agente de integridade do sistema, enquanto ele está processando um [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="478c7-108">The **INapSystemHealthAgentCallback::GetFixupInfo** method is called by the NapAgent to determine the state of the system health agent, while it is processing a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="syntax"></a><span data-ttu-id="478c7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="478c7-109">Syntax</span></span>


```C++
HRESULT GetFixupInfo(
  [out] FixupInfo **info
);
```



## <a name="parameters"></a><span data-ttu-id="478c7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="478c7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="478c7-111">*informações* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="478c7-111">*info* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="478c7-112">Um ponteiro para um ponteiro para uma estrutura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) que contém o status de correção do agente.</span><span class="sxs-lookup"><span data-stu-id="478c7-112">A pointer to a pointer to a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure that contains the fix-up status of the agent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="478c7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="478c7-113">Return value</span></span>

<span data-ttu-id="478c7-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="478c7-114">This method can return one of these values.</span></span>



| <span data-ttu-id="478c7-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="478c7-115">Return code</span></span>                                                                          | <span data-ttu-id="478c7-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="478c7-116">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="478c7-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="478c7-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="478c7-118">Indica êxito.</span><span class="sxs-lookup"><span data-stu-id="478c7-118">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="478c7-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="478c7-119">Remarks</span></span>

<span data-ttu-id="478c7-120">Esse método de retorno de chamada é declarado pelo sistema NAP e deve ser implementado pelo gravador SHA.</span><span class="sxs-lookup"><span data-stu-id="478c7-120">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="478c7-121">O agente de integridade do sistema deve retornar **S \_ OK** imediatamente sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="478c7-121">The system health agent must return **S\_OK** immediately without blocking.</span></span>

## <a name="requirements"></a><span data-ttu-id="478c7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="478c7-122">Requirements</span></span>



| <span data-ttu-id="478c7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="478c7-123">Requirement</span></span> | <span data-ttu-id="478c7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="478c7-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="478c7-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="478c7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="478c7-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="478c7-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="478c7-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="478c7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="478c7-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="478c7-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="478c7-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="478c7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="478c7-130"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="478c7-130"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="478c7-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="478c7-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="478c7-132"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="478c7-132"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="478c7-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="478c7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="478c7-134">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="478c7-134">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





