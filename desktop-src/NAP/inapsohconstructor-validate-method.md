---
title: Método de validação de INapSoHConstructor (NapProtocol. h)
description: Verifica a validade do pacote SoH.
ms.assetid: 66338213-43c0-461a-a794-5f18d56bd505
keywords:
- Validar método NAP
- Validar método NAP, interface INapSoHConstructor
- INapSoHConstructor interface NAP, método Validate
topic_type:
- apiref
api_name:
- INapSoHConstructor.Validate
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7db8a52d7986348e85c724171b6d417996c7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644926"
---
# <a name="inapsohconstructorvalidate-method"></a><span data-ttu-id="f9049-106">Método INapSoHConstructor:: Validate</span><span class="sxs-lookup"><span data-stu-id="f9049-106">INapSoHConstructor::Validate method</span></span>

> [!Note]  
> <span data-ttu-id="f9049-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="f9049-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f9049-108">O método **INapSoHConstructor:: Validate** verifica a validade do pacote soh.</span><span class="sxs-lookup"><span data-stu-id="f9049-108">The **INapSoHConstructor::Validate** method checks the validity of the SoH packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9049-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9049-109">Syntax</span></span>


```C++
HRESULT Validate(
  [in] const SoH  *soh,
  [in]       BOOL isRequest
);
```



## <a name="parameters"></a><span data-ttu-id="f9049-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9049-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9049-111">*soh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9049-111">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9049-112">Um ponteiro para o pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) construído.</span><span class="sxs-lookup"><span data-stu-id="f9049-112">A pointer to the constructed [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="f9049-113">*Isrequest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9049-113">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9049-114">Um **bool** que será **verdadeiro** se o pacote for um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** se for um **SoHResponse**.</span><span class="sxs-lookup"><span data-stu-id="f9049-114">A **BOOL** that is **TRUE** if the packet is an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is an **SoHResponse**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9049-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9049-115">Return value</span></span>

<span data-ttu-id="f9049-116">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="f9049-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f9049-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f9049-117">Return code</span></span>                                                                                            | <span data-ttu-id="f9049-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9049-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9049-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9049-119"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="f9049-120">O pacote SoH é válido.</span><span class="sxs-lookup"><span data-stu-id="f9049-120">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="f9049-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f9049-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="f9049-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="f9049-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f9049-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f9049-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="f9049-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="f9049-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f9049-125"><dt>**\_pacote NAP E \_ inválido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9049-125"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="f9049-126">O pacote SoH é inválido.</span><span class="sxs-lookup"><span data-stu-id="f9049-126">The SoH packet is invalid.</span></span><br/>                              |



 

## <a name="requirements"></a><span data-ttu-id="f9049-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9049-127">Requirements</span></span>



| <span data-ttu-id="f9049-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9049-128">Requirement</span></span> | <span data-ttu-id="f9049-129">Valor</span><span class="sxs-lookup"><span data-stu-id="f9049-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9049-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9049-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f9049-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9049-131">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f9049-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9049-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f9049-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f9049-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f9049-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9049-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9049-135"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9049-135"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9049-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="f9049-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9049-137"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9049-137"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="f9049-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f9049-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9049-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9049-139"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="f9049-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9049-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9049-141">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="f9049-141">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





