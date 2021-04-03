---
title: Método WSMan. EnumerationFlagNonXmlText (WSManDisp. h)
description: Retorna o valor da constante de enumeração WSManFlagNonXmlText para uso no parâmetro flags do método Session. Enumerate.
ms.assetid: 5e062e73-f833-4090-ba5a-48ca374724e7
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método EnumerationFlagNonXmlText
- Método EnumerationFlagNonXmlText Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método EnumerationFlagNonXmlText
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagNonXmlText
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26a9547f85a07702dc3735129842e5bc286ee9b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644864"
---
# <a name="wsmanenumerationflagnonxmltext-method"></a><span data-ttu-id="f096d-106">Método WSMan. EnumerationFlagNonXmlText</span><span class="sxs-lookup"><span data-stu-id="f096d-106">WSMan.EnumerationFlagNonXmlText method</span></span>

<span data-ttu-id="f096d-107">O **WSMan. EnumerationFlagNonXmlText** retorna o valor da constante de enumeração **WSManFlagNonXmlText** para uso no parâmetro *flags* do método [**Session. Enumerate**](session-enumerate.md) .</span><span class="sxs-lookup"><span data-stu-id="f096d-107">The **WSMan.EnumerationFlagNonXmlText** returns the value of the enumeration constant **WSManFlagNonXmlText** for use in the *flags* parameter of the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="f096d-108">Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante.</span><span class="sxs-lookup"><span data-stu-id="f096d-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="f096d-109">Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f096d-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="f096d-110">**WSManFlagNonXmlText** é uma constante na enumeração **\_ \_ WSManEnumFlags** .</span><span class="sxs-lookup"><span data-stu-id="f096d-110">**WSManFlagNonXmlText** is a constant in the **\_\_WSManEnumFlags** enumeration.</span></span> <span data-ttu-id="f096d-111">Para obter mais informações, consulte [**constantes de enumeração**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f096d-111">For more information, see [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f096d-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f096d-112">Syntax</span></span>


```VB
WSMan.EnumerationFlagNonXmlText( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="f096d-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f096d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f096d-114">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="f096d-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f096d-115">O valor da constante.</span><span class="sxs-lookup"><span data-stu-id="f096d-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f096d-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f096d-116">Return value</span></span>

<span data-ttu-id="f096d-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f096d-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f096d-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f096d-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f096d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f096d-119">Requirements</span></span>



| <span data-ttu-id="f096d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f096d-120">Requirement</span></span> | <span data-ttu-id="f096d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f096d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f096d-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f096d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f096d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f096d-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="f096d-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f096d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f096d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f096d-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f096d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f096d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f096d-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f096d-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f096d-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="f096d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f096d-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f096d-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="f096d-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f096d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="f096d-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f096d-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f096d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f096d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f096d-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f096d-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f096d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="f096d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f096d-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="f096d-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="f096d-136">**IWSManEx**</span><span class="sxs-lookup"><span data-stu-id="f096d-136">**IWSManEx**</span></span>](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)
</dt> <dt>

[<span data-ttu-id="f096d-137">**IWSManSession**</span><span class="sxs-lookup"><span data-stu-id="f096d-137">**IWSManSession**</span></span>](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> </dl>

 

 





