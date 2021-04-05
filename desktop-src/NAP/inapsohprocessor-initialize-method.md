---
title: Método de inicialização de INapSoHProcessor (NapProtocol. h)
description: Inicializa o pacote de protocolo e o sistema de processador SoH. Esse método deve ser chamado exatamente uma vez.
ms.assetid: 4fccc847-3c4d-4fc5-935d-28fb2964a9be
keywords:
- Inicializar método NAP
- Método Initialize NAP, interface INapSoHProcessor
- INapSoHProcessor interface NAP, método Initialize
topic_type:
- apiref
api_name:
- INapSoHProcessor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ff3a32bb213caf19964ccea8175a43e5016f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918449"
---
# <a name="inapsohprocessorinitialize-method"></a><span data-ttu-id="02bd3-107">Método INapSoHProcessor:: Initialize</span><span class="sxs-lookup"><span data-stu-id="02bd3-107">INapSoHProcessor::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="02bd3-108">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="02bd3-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="02bd3-109">O método **INapSoHProcessor:: Initialize** Inicializa o pacote de protocolo e o sistema de processador soh.</span><span class="sxs-lookup"><span data-stu-id="02bd3-109">The **INapSoHProcessor::Initialize** method initializes the protocol packet and SoH processor system.</span></span> <span data-ttu-id="02bd3-110">Esse método deve ser chamado exatamente uma vez.</span><span class="sxs-lookup"><span data-stu-id="02bd3-110">This method must be called exactly once.</span></span>

## <a name="syntax"></a><span data-ttu-id="02bd3-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02bd3-111">Syntax</span></span>


```C++
HRESULT Initialize(
  [in]  const SoH                  *soh,
  [in]        BOOL                 isRequest,
  [out]       SystemHealthEntityId *id
);
```



## <a name="parameters"></a><span data-ttu-id="02bd3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02bd3-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02bd3-113">*soh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02bd3-113">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02bd3-114">Um ponteiro para o pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) a ser processado.</span><span class="sxs-lookup"><span data-stu-id="02bd3-114">A pointer to the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="02bd3-115">*Isrequest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02bd3-115">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02bd3-116">Um **bool** que será **verdadeiro** se o pacote for um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** se for um **SoHResponse**.</span><span class="sxs-lookup"><span data-stu-id="02bd3-116">A **BOOL** that is **TRUE** if the packet is an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is an **SoHResponse**.</span></span>

</dd> <dt>

<span data-ttu-id="02bd3-117">saída da *ID* \[\]</span><span class="sxs-lookup"><span data-stu-id="02bd3-117">*id* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02bd3-118">Um [SystemHealthEntityId](nap-datatypes.md) exclusivo que contém a ID do SHA ou SHV que construiu o pacote.</span><span class="sxs-lookup"><span data-stu-id="02bd3-118">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA or SHV that constructed the packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02bd3-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02bd3-119">Return value</span></span>

<span data-ttu-id="02bd3-120">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="02bd3-120">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="02bd3-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="02bd3-121">Return code</span></span>                                                                                            | <span data-ttu-id="02bd3-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="02bd3-122">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="02bd3-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="02bd3-123"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="02bd3-124">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="02bd3-124">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="02bd3-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="02bd3-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="02bd3-126">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="02bd3-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="02bd3-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="02bd3-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="02bd3-128">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="02bd3-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="02bd3-129"><dt>**\_pacote NAP E \_ inválido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="02bd3-129"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="02bd3-130">O pacote SoH é inválido.</span><span class="sxs-lookup"><span data-stu-id="02bd3-130">The SoH packet is invalid.</span></span><br/>                              |



 

## <a name="requirements"></a><span data-ttu-id="02bd3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02bd3-131">Requirements</span></span>



| <span data-ttu-id="02bd3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="02bd3-132">Requirement</span></span> | <span data-ttu-id="02bd3-133">Valor</span><span class="sxs-lookup"><span data-stu-id="02bd3-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="02bd3-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02bd3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="02bd3-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="02bd3-135">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="02bd3-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02bd3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="02bd3-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="02bd3-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="02bd3-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="02bd3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="02bd3-139"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="02bd3-139"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="02bd3-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="02bd3-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="02bd3-141"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="02bd3-141"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="02bd3-142">DLL</span><span class="sxs-lookup"><span data-stu-id="02bd3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02bd3-143"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02bd3-143"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="02bd3-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="02bd3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02bd3-145">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="02bd3-145">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





