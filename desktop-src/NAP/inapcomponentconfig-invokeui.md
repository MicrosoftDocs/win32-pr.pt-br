---
title: Método INapComponentConfig InvokeUI (NapCommon. h)
description: Inicia uma interface do usuário personalizada para um componente do validador da integridade do sistema (SHV).
ms.assetid: da2a5e3e-bc17-4984-bdbe-b72e9e710a9d
keywords:
- Método InvokeUI NAP
- Método InvokeUI NAP, interface INapComponentConfig
- INapComponentConfig interface NAP, método InvokeUI
topic_type:
- apiref
api_name:
- INapComponentConfig.InvokeUI
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd86d683365286fc2130c1ac9edf21ff075d61a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918245"
---
# <a name="inapcomponentconfiginvokeui-method"></a><span data-ttu-id="298de-106">Método INapComponentConfig:: InvokeUI</span><span class="sxs-lookup"><span data-stu-id="298de-106">INapComponentConfig::InvokeUI method</span></span>

> [!Note]  
> <span data-ttu-id="298de-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="298de-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="298de-108">O método **InvokeUI** inicia uma interface do usuário personalizada para um componente do validador da integridade do sistema (SHV).</span><span class="sxs-lookup"><span data-stu-id="298de-108">The **InvokeUI** method launches a customized user interface for a system health validator (SHV) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="298de-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="298de-109">Syntax</span></span>


```C++
HRESULT InvokeUI(
  [in] HWND hwndParent
) const;
```



## <a name="parameters"></a><span data-ttu-id="298de-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="298de-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="298de-111">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="298de-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="298de-112">Um identificador para a janela pai ou proprietário.</span><span class="sxs-lookup"><span data-stu-id="298de-112">A handle to the parent or owner window.</span></span> <span data-ttu-id="298de-113">Um identificador de janela válido deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="298de-113">A valid window handle must be supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="298de-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="298de-114">Return value</span></span>

<span data-ttu-id="298de-115">Retorna um dos seguintes códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="298de-115">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="298de-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="298de-116">Return code</span></span>                                                                                     | <span data-ttu-id="298de-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="298de-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="298de-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="298de-118"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="298de-119">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="298de-119">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="298de-120"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="298de-120"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="298de-121">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="298de-121">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="298de-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="298de-122"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="298de-123">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="298de-123">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="298de-124"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="298de-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>       | <span data-ttu-id="298de-125">O SHV não oferece suporte a uma interface do usuário personalizada.</span><span class="sxs-lookup"><span data-stu-id="298de-125">The SHV does not support a customized UI.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="298de-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="298de-126">Remarks</span></span>

<span data-ttu-id="298de-127">Essa chamada de método deve ser bloqueada até que a interface do usuário do SHV saia.</span><span class="sxs-lookup"><span data-stu-id="298de-127">This method call should block until the SHV user interface exits.</span></span>

## <a name="requirements"></a><span data-ttu-id="298de-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="298de-128">Requirements</span></span>



| <span data-ttu-id="298de-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="298de-129">Requirement</span></span> | <span data-ttu-id="298de-130">Valor</span><span class="sxs-lookup"><span data-stu-id="298de-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="298de-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="298de-131">Minimum supported client</span></span><br/> | <span data-ttu-id="298de-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="298de-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="298de-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="298de-133">Minimum supported server</span></span><br/> | <span data-ttu-id="298de-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="298de-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="298de-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="298de-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="298de-136"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="298de-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="298de-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="298de-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="298de-138"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="298de-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="298de-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="298de-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="298de-140">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="298de-140">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="298de-141">**INapComponentConfig::IsUISupported**</span><span class="sxs-lookup"><span data-stu-id="298de-141">**INapComponentConfig::IsUISupported**</span></span>](inapcomponentconfig-isuisupported.md)
</dt> </dl>

 

 





