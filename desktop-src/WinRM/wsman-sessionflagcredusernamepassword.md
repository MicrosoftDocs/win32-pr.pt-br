---
title: Método WSMan. SessionFlagCredUsernamePassword (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagCredUsernamePassword para uso no parâmetro flags do método WSMan. CreateSession.
ms.assetid: 70d12df4-f0ac-499a-8b2f-6ba83b77869e
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagCredUsernamePassword
- Método SessionFlagCredUsernamePassword Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagCredUsernamePassword
topic_type:
- apiref
api_name:
- WSMan.SessionFlagCredUsernamePassword
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84827f342f70b13f1a2f0192289b34e347f26045
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009537"
---
# <a name="wsmansessionflagcredusernamepassword-method"></a><span data-ttu-id="2a591-106">Método WSMan. SessionFlagCredUsernamePassword</span><span class="sxs-lookup"><span data-stu-id="2a591-106">WSMan.SessionFlagCredUsernamePassword method</span></span>

<span data-ttu-id="2a591-107">O método **WSMan. SessionFlagCredUsernamePassword** retorna o valor do sinalizador de autenticação **WSManFlagCredUsernamePassword** para uso no parâmetro *flags* do método [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="2a591-107">The **WSMan.SessionFlagCredUsernamePassword** method returns the value of the authentication flag **WSManFlagCredUsernamePassword** for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="2a591-108">Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante.</span><span class="sxs-lookup"><span data-stu-id="2a591-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="2a591-109">Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2a591-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="2a591-110">**WSManFlagCredUsernamePassword** é uma constante na enumeração **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="2a591-110">**WSManFlagCredUsernamePassword** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="2a591-111">Para obter mais informações, consulte [constantes de autenticação](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2a591-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2a591-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a591-112">Syntax</span></span>


```VB
WSMan.SessionFlagCredUsernamePassword( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="2a591-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a591-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a591-114">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="2a591-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a591-115">O valor da constante.</span><span class="sxs-lookup"><span data-stu-id="2a591-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a591-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2a591-116">Return value</span></span>

<span data-ttu-id="2a591-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2a591-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2a591-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2a591-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a591-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a591-119">Requirements</span></span>



| <span data-ttu-id="2a591-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a591-120">Requirement</span></span> | <span data-ttu-id="2a591-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2a591-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a591-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a591-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2a591-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a591-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2a591-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a591-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2a591-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a591-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2a591-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2a591-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a591-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a591-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a591-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="2a591-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2a591-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2a591-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="2a591-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2a591-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="2a591-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2a591-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2a591-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2a591-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a591-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a591-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2a591-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a591-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a591-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="2a591-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="2a591-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="2a591-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





