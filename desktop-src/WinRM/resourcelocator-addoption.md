---
title: Método ResourceLocator. AddOption (WSManDisp. h)
description: Adiciona dados adicionais necessários para processar a solicitação. Por exemplo, alguns provedores WMI podem exigir um objeto IWbemContext ou SWbemNamedValueSet com informações específicas do provedor.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- Método AddOption Gerenciamento Remoto do Windows
- Método AddOption Gerenciamento Remoto do Windows, objeto ResourceLocator
- Objeto ResourceLocator Gerenciamento Remoto do Windows, método AddOption
topic_type:
- apiref
api_name:
- ResourceLocator.AddOption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 882f400dd2c59d2395dd2755846245f4e4ad385e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009017"
---
# <a name="resourcelocatoraddoption-method"></a><span data-ttu-id="6b3c4-107">Método ResourceLocator. AddOption</span><span class="sxs-lookup"><span data-stu-id="6b3c4-107">ResourceLocator.AddOption method</span></span>

<span data-ttu-id="6b3c4-108">Adiciona dados adicionais necessários para processar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="6b3c4-108">Adds additional data required to process the request.</span></span> <span data-ttu-id="6b3c4-109">Por exemplo, alguns provedores WMI podem exigir um objeto [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) ou [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) com informações específicas do provedor.</span><span class="sxs-lookup"><span data-stu-id="6b3c4-109">For example, some WMI providers may require an [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) or [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) object with provider-specific information.</span></span> <span data-ttu-id="6b3c4-110">Você pode fornecer um objeto [**ResourceLocator**](resourcelocator.md) em vez de especificar um URI de recurso em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="6b3c4-110">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6b3c4-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b3c4-111">Syntax</span></span>


```VB
ResourceLocator.AddOption( _
  ByVal OptionName, _
  ByVal OptionValue, _
  ByVal mustComply _
)
```



## <a name="parameters"></a><span data-ttu-id="6b3c4-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b3c4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b3c4-113">*OptionName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b3c4-113">*OptionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b3c4-114">O nome (chave) do objeto de dados opcional.</span><span class="sxs-lookup"><span data-stu-id="6b3c4-114">The name (key) of the optional data object.</span></span>

</dd> <dt>

<span data-ttu-id="6b3c4-115">*Opçãovalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b3c4-115">*OptionValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b3c4-116">Um valor fornecido para o objeto de dados opcional.</span><span class="sxs-lookup"><span data-stu-id="6b3c4-116">A value supplied for the optional data object.</span></span>

</dd> <dt>

<span data-ttu-id="6b3c4-117">*mustComply* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b3c4-117">*mustComply* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b3c4-118">Um sinalizador que indica que a opção deve ser processada.</span><span class="sxs-lookup"><span data-stu-id="6b3c4-118">A flag that indicates the option must be processed.</span></span> <span data-ttu-id="6b3c4-119">O padrão é **false** (0).</span><span class="sxs-lookup"><span data-stu-id="6b3c4-119">The default is **False** (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b3c4-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6b3c4-120">Return value</span></span>

<span data-ttu-id="6b3c4-121">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6b3c4-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b3c4-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b3c4-122">Remarks</span></span>

<span data-ttu-id="6b3c4-123">**IWSManResourceLocator:: AddOption** é o método C++ correspondente.</span><span class="sxs-lookup"><span data-stu-id="6b3c4-123">**IWSManResourceLocator::AddOption** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b3c4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b3c4-124">Requirements</span></span>



| <span data-ttu-id="6b3c4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b3c4-125">Requirement</span></span> | <span data-ttu-id="6b3c4-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6b3c4-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b3c4-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b3c4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6b3c4-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b3c4-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="6b3c4-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b3c4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6b3c4-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b3c4-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6b3c4-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b3c4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b3c4-132"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b3c4-132"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b3c4-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="6b3c4-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6b3c4-134"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6b3c4-134"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="6b3c4-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6b3c4-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="6b3c4-136"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6b3c4-136"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6b3c4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6b3c4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b3c4-138"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b3c4-138"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6b3c4-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b3c4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b3c4-140">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="6b3c4-140">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

