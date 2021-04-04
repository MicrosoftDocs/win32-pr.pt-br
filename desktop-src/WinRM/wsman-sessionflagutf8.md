---
title: Método WSMan. SessionFlagUTF8 (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagUTF8 para uso no parâmetro flags de WSMan. CreateSession.
ms.assetid: a79e292a-364b-4bf3-ae66-6a15ad51524f
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagUTF8
- Método SessionFlagUTF8 Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagUTF8
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUTF8
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 985763131c2f3d4227f1a24af612ea3141237832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645078"
---
# <a name="wsmansessionflagutf8-method"></a><span data-ttu-id="33d55-106">Método WSMan. SessionFlagUTF8</span><span class="sxs-lookup"><span data-stu-id="33d55-106">WSMan.SessionFlagUTF8 method</span></span>

<span data-ttu-id="33d55-107">O método **WSMan. SessionFlagUTF8** retorna o valor do sinalizador de autenticação **WSManFlagUTF8** para uso no parâmetro *flags* de [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="33d55-107">The **WSMan.SessionFlagUTF8** method returns the value of the **WSManFlagUTF8** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="33d55-108">Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante.</span><span class="sxs-lookup"><span data-stu-id="33d55-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="33d55-109">Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="33d55-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="33d55-110">**WSManFlagUTF8** é uma constante na enumeração **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="33d55-110">**WSManFlagUTF8** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="33d55-111">Para obter mais informações, consulte [outras constantes de sessão](other-session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="33d55-111">For more information, see [Other Session Constants](other-session-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="33d55-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33d55-112">Syntax</span></span>


```VB
WSMan.SessionFlagUTF8( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="33d55-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33d55-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33d55-114">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="33d55-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33d55-115">O valor da constante.</span><span class="sxs-lookup"><span data-stu-id="33d55-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33d55-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33d55-116">Return value</span></span>

<span data-ttu-id="33d55-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="33d55-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="33d55-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33d55-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="33d55-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33d55-119">Requirements</span></span>



| <span data-ttu-id="33d55-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="33d55-120">Requirement</span></span> | <span data-ttu-id="33d55-121">Valor</span><span class="sxs-lookup"><span data-stu-id="33d55-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33d55-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33d55-122">Minimum supported client</span></span><br/> | <span data-ttu-id="33d55-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33d55-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="33d55-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33d55-124">Minimum supported server</span></span><br/> | <span data-ttu-id="33d55-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33d55-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="33d55-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33d55-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="33d55-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="33d55-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="33d55-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="33d55-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="33d55-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="33d55-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="33d55-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33d55-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="33d55-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="33d55-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="33d55-132">DLL</span><span class="sxs-lookup"><span data-stu-id="33d55-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33d55-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33d55-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="33d55-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="33d55-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33d55-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="33d55-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="33d55-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="33d55-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





