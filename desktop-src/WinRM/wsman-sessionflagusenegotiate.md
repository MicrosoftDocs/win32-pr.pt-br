---
title: Método WSMan. SessionFlagUseNegotiate (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagUseNegotiate para uso no parâmetro flags do método WSMan. CreateSession.
ms.assetid: 86d8ed13-5eae-4a06-8ceb-b0ec067f4a4c
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagUseNegotiate
- Método SessionFlagUseNegotiate Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagUseNegotiate
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseNegotiate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b57e463ccf71f22f12a964b1e1de72f426963c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789336"
---
# <a name="wsmansessionflagusenegotiate-method"></a><span data-ttu-id="33448-106">Método WSMan. SessionFlagUseNegotiate</span><span class="sxs-lookup"><span data-stu-id="33448-106">WSMan.SessionFlagUseNegotiate method</span></span>

<span data-ttu-id="33448-107">O método **WSMan. SessionFlagUseNegotiate** retorna o valor do sinalizador de autenticação **WSManFlagUseNegotiate** para uso no parâmetro *flags* do método [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="33448-107">The **WSMan.SessionFlagUseNegotiate** method returns the value of the **WSManFlagUseNegotiate** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="33448-108">Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante.</span><span class="sxs-lookup"><span data-stu-id="33448-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="33448-109">Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="33448-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="33448-110">**WSManFlagUseNegotiate** é uma constante na enumeração **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="33448-110">**WSManFlagUseNegotiate** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="33448-111">Para obter mais informações, consulte [constantes de autenticação](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="33448-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="33448-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33448-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseNegotiate( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="33448-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33448-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33448-114">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="33448-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33448-115">O valor da constante.</span><span class="sxs-lookup"><span data-stu-id="33448-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33448-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33448-116">Return value</span></span>

<span data-ttu-id="33448-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="33448-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="33448-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33448-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="33448-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33448-119">Requirements</span></span>



| <span data-ttu-id="33448-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="33448-120">Requirement</span></span> | <span data-ttu-id="33448-121">Valor</span><span class="sxs-lookup"><span data-stu-id="33448-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33448-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33448-122">Minimum supported client</span></span><br/> | <span data-ttu-id="33448-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33448-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="33448-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33448-124">Minimum supported server</span></span><br/> | <span data-ttu-id="33448-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33448-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="33448-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33448-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="33448-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="33448-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="33448-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="33448-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="33448-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="33448-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="33448-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33448-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="33448-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="33448-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="33448-132">DLL</span><span class="sxs-lookup"><span data-stu-id="33448-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33448-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33448-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="33448-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="33448-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33448-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="33448-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="33448-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="33448-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





