---
title: Método WSMan. EnumerationFlagHierarchyDeep (WSManDisp. h)
description: Retorna o valor do sinalizador de enumeração EnumerationFlagHierarchyDeep para uso no parâmetro flags de Session. Enumerate.
ms.assetid: b84b82fa-0b2e-418e-850f-6d7a4749fdc1
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método EnumerationFlagHierarchyDeep
- Método EnumerationFlagHierarchyDeep Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método EnumerationFlagHierarchyDeep
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyDeep
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61982c6117d0a91ec253af35657f0cbbf5af12c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919030"
---
# <a name="wsmanenumerationflaghierarchydeep-method"></a><span data-ttu-id="f7170-106">Método WSMan. EnumerationFlagHierarchyDeep</span><span class="sxs-lookup"><span data-stu-id="f7170-106">WSMan.EnumerationFlagHierarchyDeep method</span></span>

<span data-ttu-id="f7170-107">O método **EnumerationFlagHierarchyDeep** retorna o valor do sinalizador de enumeração **EnumerationFlagHierarchyDeep** para uso no parâmetro *flags* de [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="f7170-107">The **EnumerationFlagHierarchyDeep** method returns the value of the enumeration flag **EnumerationFlagHierarchyDeep** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="f7170-108">Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante.</span><span class="sxs-lookup"><span data-stu-id="f7170-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="f7170-109">Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f7170-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="f7170-110">**EnumerationFlagHierarchyDeep** é uma constante na enumeração **\_ WSManEnumFlags** e é descrita em [**constantes de enumeração**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f7170-110">**EnumerationFlagHierarchyDeep** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f7170-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7170-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagHierarchyDeep( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="f7170-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7170-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7170-113">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="f7170-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7170-114">O valor da constante.</span><span class="sxs-lookup"><span data-stu-id="f7170-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7170-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f7170-115">Return value</span></span>

<span data-ttu-id="f7170-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f7170-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f7170-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f7170-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7170-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7170-118">Requirements</span></span>



| <span data-ttu-id="f7170-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7170-119">Requirement</span></span> | <span data-ttu-id="f7170-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f7170-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7170-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7170-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f7170-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7170-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="f7170-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7170-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f7170-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7170-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f7170-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f7170-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7170-126"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7170-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7170-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="f7170-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f7170-128"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f7170-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="f7170-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f7170-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="f7170-130"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f7170-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f7170-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f7170-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7170-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7170-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f7170-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7170-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7170-134">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="f7170-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="f7170-135">**Session**</span><span class="sxs-lookup"><span data-stu-id="f7170-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





