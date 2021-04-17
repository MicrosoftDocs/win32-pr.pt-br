---
description: Notifica um objeto de que ele deve exibir seu construtor para a propriedade especificada.
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: 'Método IProvidePropertyBuilder:: ExecuteBuilder'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.ExecuteBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: c37c2a4ca1003bd701ea141f1723f4ca16aa69c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749929"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a><span data-ttu-id="45bcc-103">Método IProvidePropertyBuilder:: ExecuteBuilder</span><span class="sxs-lookup"><span data-stu-id="45bcc-103">IProvidePropertyBuilder::ExecuteBuilder method</span></span>

<span data-ttu-id="45bcc-104">Notifica um objeto de que ele deve exibir seu construtor para a propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="45bcc-104">Notifies an object that it should display its builder for the specified property.</span></span>

## <a name="syntax"></a><span data-ttu-id="45bcc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45bcc-105">Syntax</span></span>


```C++
void ExecuteBuilder(
  [in]          LONG      dispid,
  [in]          BSTR      bstrGuidBldr,
  [in]          IDispatch *pdispApp,
  [in]          LONG_PTR  hwndBldrOwner,
  [in, out]     LPVARIANT pvarValue,
  [out, retval] LPBOOL    pbActionCommitted
);
```



## <a name="parameters"></a><span data-ttu-id="45bcc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45bcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45bcc-107">*DISPID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45bcc-107">*dispid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45bcc-108">O DISPID da propriedade para a qual o Construtor exibe.</span><span class="sxs-lookup"><span data-stu-id="45bcc-108">The DISPID of the property for which the builder displays.</span></span>

</dd> <dt>

<span data-ttu-id="45bcc-109">*bstrGuidBldr* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45bcc-109">*bstrGuidBldr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45bcc-110">O **BSTR** do GUID do Construtor a ser invocado.</span><span class="sxs-lookup"><span data-stu-id="45bcc-110">The **BSTR** of the builder GUID to invoke.</span></span> <span data-ttu-id="45bcc-111">Isso é retornado de [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span><span class="sxs-lookup"><span data-stu-id="45bcc-111">This is returned from [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span></span>

</dd> <dt>

<span data-ttu-id="45bcc-112">*pdispApp* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45bcc-112">*pdispApp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45bcc-113">Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="45bcc-113">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="45bcc-114">*hwndBldrOwner* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45bcc-114">*hwndBldrOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45bcc-115">Um identificador para a janela do construtor pop-up pai.</span><span class="sxs-lookup"><span data-stu-id="45bcc-115">A handle to the parent pop-up builder window.</span></span>

</dd> <dt>

<span data-ttu-id="45bcc-116">*pvarValue* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="45bcc-116">*pvarValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="45bcc-117">O valor atual da propriedade.</span><span class="sxs-lookup"><span data-stu-id="45bcc-117">The current value of the property.</span></span> <span data-ttu-id="45bcc-118">Esse valor pode ser modificado pelo objeto e alterado para o novo valor se *pbActionCommitted* for **true**.</span><span class="sxs-lookup"><span data-stu-id="45bcc-118">This value can be modified by the object and changes to the new value if *pbActionCommitted* is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="45bcc-119">*pbActionCommitted* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="45bcc-119">*pbActionCommitted* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="45bcc-120">Um valor que indica se o Construtor executou uma ação no objeto.</span><span class="sxs-lookup"><span data-stu-id="45bcc-120">A value that indicates whether the builder performed an action on the object.</span></span> <span data-ttu-id="45bcc-121">Pode ser usado quando um usuário modifica algo e, em seguida, pressiona OK na caixa de diálogo Construtor de pop-ups.</span><span class="sxs-lookup"><span data-stu-id="45bcc-121">Can be used when a user modifies something, then presses OK on the pop-up builder dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45bcc-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45bcc-122">Return value</span></span>

<span data-ttu-id="45bcc-123">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="45bcc-123">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="45bcc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45bcc-124">Requirements</span></span>



| <span data-ttu-id="45bcc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="45bcc-125">Requirement</span></span> | <span data-ttu-id="45bcc-126">Valor</span><span class="sxs-lookup"><span data-stu-id="45bcc-126">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="45bcc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="45bcc-127">DLL</span></span><br/> | <dl> <span data-ttu-id="45bcc-128"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45bcc-128"><dt>Vsp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45bcc-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="45bcc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45bcc-130">**IProvidePropertyBuilder**</span><span class="sxs-lookup"><span data-stu-id="45bcc-130">**IProvidePropertyBuilder**</span></span>](iprovidepropertybuilder.md)
</dt> </dl>

 

 




