---
title: Método INapSoHConstructor GetSoH (NapProtocol. h)
description: Recupera o pacote SoHRequest ou SoHResponse construído.
ms.assetid: 402c72fd-9e23-453a-8c95-57615295e056
keywords:
- Método GetSoH NAP
- Método GetSoH NAP, interface INapSoHConstructor
- INapSoHConstructor interface NAP, método GetSoH
topic_type:
- apiref
api_name:
- INapSoHConstructor.GetSoH
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066257aadf0ed14816efec06936d4b070087159f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085492"
---
# <a name="inapsohconstructorgetsoh-method"></a><span data-ttu-id="7cee0-106">Método INapSoHConstructor:: GetSoH</span><span class="sxs-lookup"><span data-stu-id="7cee0-106">INapSoHConstructor::GetSoH method</span></span>

> [!Note]  
> <span data-ttu-id="7cee0-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="7cee0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7cee0-108">O método **INapSoHConstructor:: GetSoH** recupera o pacote SoHRequest ou SoHResponse construído.</span><span class="sxs-lookup"><span data-stu-id="7cee0-108">The **INapSoHConstructor::GetSoH** method retrieves the constructed SoHRequest or SoHResponse packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cee0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7cee0-109">Syntax</span></span>


```C++
HRESULT GetSoH(
  [out] SoH **soh
);
```



## <a name="parameters"></a><span data-ttu-id="7cee0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7cee0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cee0-111">*soh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7cee0-111">*soh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cee0-112">Um ponteiro para um ponteiro para o pacote [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ou **SoHResponse** construído.</span><span class="sxs-lookup"><span data-stu-id="7cee0-112">A pointer to a pointer to the constructed [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) or **SoHResponse** packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cee0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7cee0-113">Return value</span></span>

<span data-ttu-id="7cee0-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="7cee0-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="7cee0-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7cee0-115">Return code</span></span>                                                                                     | <span data-ttu-id="7cee0-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cee0-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7cee0-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7cee0-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="7cee0-118">Operação concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="7cee0-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7cee0-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="7cee0-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="7cee0-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="7cee0-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="7cee0-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7cee0-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="7cee0-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="7cee0-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7cee0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cee0-123">Requirements</span></span>



| <span data-ttu-id="7cee0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cee0-124">Requirement</span></span> | <span data-ttu-id="7cee0-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7cee0-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cee0-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cee0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7cee0-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7cee0-127">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7cee0-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cee0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7cee0-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7cee0-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7cee0-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7cee0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cee0-131"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cee0-131"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="7cee0-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="7cee0-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7cee0-133"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7cee0-133"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="7cee0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7cee0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cee0-135"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cee0-135"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7cee0-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="7cee0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cee0-137">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="7cee0-137">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





