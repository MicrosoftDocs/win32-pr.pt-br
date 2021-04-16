---
title: Método INapComponentConfig IsUISupported (NapCommon. h)
description: Especifica se o componente dá suporte a uma interface do usuário personalizada.
ms.assetid: 044f8014-f041-4e9c-922a-2691b799ba84
keywords:
- Método IsUISupported NAP
- Método IsUISupported NAP, interface INapComponentConfig
- INapComponentConfig interface NAP, método IsUISupported
topic_type:
- apiref
api_name:
- INapComponentConfig.IsUISupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab7d3f6b87ba5e483b466e6746f0f63d039cb205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758602"
---
# <a name="inapcomponentconfigisuisupported-method"></a><span data-ttu-id="f1568-106">Método INapComponentConfig:: IsUISupported</span><span class="sxs-lookup"><span data-stu-id="f1568-106">INapComponentConfig::IsUISupported method</span></span>

> [!Note]  
> <span data-ttu-id="f1568-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="f1568-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f1568-108">O método **IsUISupported** especifica se o componente dá suporte a uma interface de usuário personalizada.</span><span class="sxs-lookup"><span data-stu-id="f1568-108">The **IsUISupported** method specifies whether the component supports a customized user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1568-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1568-109">Syntax</span></span>


```C++
HRESULT IsUISupported(
  [out] BOOL *isSupported
) const;
```



## <a name="parameters"></a><span data-ttu-id="f1568-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1568-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1568-111">*IsSupported* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f1568-111">*isSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1568-112">Um ponteiro para um BOOL que é definido como **true** se o componente dá suporte a uma interface do usuário personalizada; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="f1568-112">A pointer to a BOOL that is set to **TRUE** if the component supports a customized user interface and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1568-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1568-113">Return value</span></span>

<span data-ttu-id="f1568-114">Retorna um dos seguintes códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="f1568-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="f1568-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f1568-115">Return code</span></span>                                                                                     | <span data-ttu-id="f1568-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1568-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1568-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f1568-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f1568-118">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="f1568-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="f1568-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f1568-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f1568-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="f1568-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f1568-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f1568-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f1568-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="f1568-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f1568-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1568-123">Remarks</span></span>

<span data-ttu-id="f1568-124">A interface do usuário personalizada de um componente deve ser iniciada usando [**INapComponentConfig:: InvokeUI**](inapcomponentconfig-invokeui.md).</span><span class="sxs-lookup"><span data-stu-id="f1568-124">A component's customized user interface should be launched using [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1568-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1568-125">Requirements</span></span>



| <span data-ttu-id="f1568-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1568-126">Requirement</span></span> | <span data-ttu-id="f1568-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f1568-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1568-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1568-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f1568-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f1568-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f1568-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1568-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f1568-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f1568-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f1568-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1568-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1568-133"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1568-133"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1568-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="f1568-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f1568-135"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f1568-135"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1568-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1568-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1568-137">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="f1568-137">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="f1568-138">**INapComponentConfig::InvokeUI**</span><span class="sxs-lookup"><span data-stu-id="f1568-138">**INapComponentConfig::InvokeUI**</span></span>](inapcomponentconfig-invokeui.md)
</dt> </dl>

 

 





