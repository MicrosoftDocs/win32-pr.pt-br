---
title: Método WSMan. EnumerationFlagReturnObjectAndEPR (WSManDisp. h)
description: Retorna o valor do sinalizador de enumeração EnumerationFlagReturnObjectAndEPR para uso no parâmetro flags de Session. Enumerate.
ms.assetid: 052b93df-8a83-4b5e-8325-1ad500b43a88
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método EnumerationFlagReturnObjectAndEPR
- Método EnumerationFlagReturnObjectAndEPR Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método EnumerationFlagReturnObjectAndEPR
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnObjectAndEPR
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187f8c029d0392ad9ac1a909e1e45de165815e2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455793"
---
# <a name="wsmanenumerationflagreturnobjectandepr-method"></a><span data-ttu-id="96c1b-106">Método WSMan. EnumerationFlagReturnObjectAndEPR</span><span class="sxs-lookup"><span data-stu-id="96c1b-106">WSMan.EnumerationFlagReturnObjectAndEPR method</span></span>

<span data-ttu-id="96c1b-107">O método **EnumerationFlagReturnObjectAndEPR** retorna o valor do sinalizador de enumeração **EnumerationFlagReturnObjectAndEPR** para uso no parâmetro *flags* de [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="96c1b-107">The **EnumerationFlagReturnObjectAndEPR** method returns the value of the enumeration flag **EnumerationFlagReturnObjectAndEPR** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="96c1b-108">Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante.</span><span class="sxs-lookup"><span data-stu-id="96c1b-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="96c1b-109">Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="96c1b-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="96c1b-110">**EnumerationFlagReturnObjectAndEPR** é uma constante na enumeração **\_ WSManEnumFlags** e é descrita em [**constantes de enumeração**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="96c1b-110">**EnumerationFlagReturnObjectAndEPR** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="96c1b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96c1b-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagReturnObjectAndEPR( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="96c1b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96c1b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96c1b-113">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="96c1b-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96c1b-114">O valor da constante.</span><span class="sxs-lookup"><span data-stu-id="96c1b-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96c1b-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96c1b-115">Return value</span></span>

<span data-ttu-id="96c1b-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="96c1b-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="96c1b-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="96c1b-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="96c1b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96c1b-118">Requirements</span></span>



| <span data-ttu-id="96c1b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="96c1b-119">Requirement</span></span> | <span data-ttu-id="96c1b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="96c1b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="96c1b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96c1b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="96c1b-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96c1b-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="96c1b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96c1b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="96c1b-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96c1b-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="96c1b-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96c1b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="96c1b-126"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="96c1b-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="96c1b-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="96c1b-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96c1b-128"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="96c1b-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="96c1b-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96c1b-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="96c1b-130"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="96c1b-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="96c1b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="96c1b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96c1b-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96c1b-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="96c1b-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="96c1b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c1b-134">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="96c1b-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="96c1b-135">**Session**</span><span class="sxs-lookup"><span data-stu-id="96c1b-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





