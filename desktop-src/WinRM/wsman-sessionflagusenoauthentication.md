---
title: Método WSMan. SessionFlagUseNoAuthentication (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagUseNoAuthentication para uso no parâmetro flags do método WSMan. CreateSession.
ms.assetid: 22a8107a-8e5e-4636-bf7d-a261f885e074
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagUseNoAuthentication
- Método SessionFlagUseNoAuthentication Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagUseNoAuthentication
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseNoAuthentication
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9676d3baa9a18ae8a3feb5eb4092c63586a94b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455833"
---
# <a name="wsmansessionflagusenoauthentication-method"></a><span data-ttu-id="ef65d-106">Método WSMan. SessionFlagUseNoAuthentication</span><span class="sxs-lookup"><span data-stu-id="ef65d-106">WSMan.SessionFlagUseNoAuthentication method</span></span>

<span data-ttu-id="ef65d-107">O método **WSMan. SessionFlagUseNoAuthentication** retorna o valor do sinalizador de autenticação **WSManFlagUseNoAuthentication** para uso no parâmetro *flags* do método [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="ef65d-107">The **WSMan.SessionFlagUseNoAuthentication** method returns the value of the **WSManFlagUseNoAuthentication** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="ef65d-108">Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante.</span><span class="sxs-lookup"><span data-stu-id="ef65d-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="ef65d-109">Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ef65d-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="ef65d-110">**WSManFlagUseNoAuthentication** é uma constante na enumeração **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="ef65d-110">**WSManFlagUseNoAuthentication** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="ef65d-111">Para obter mais informações, consulte//[constantes de autenticação](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ef65d-111">For more information, see //[Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef65d-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef65d-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseNoAuthentication( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="ef65d-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef65d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef65d-114">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="ef65d-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef65d-115">O valor da constante.</span><span class="sxs-lookup"><span data-stu-id="ef65d-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef65d-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ef65d-116">Return value</span></span>

<span data-ttu-id="ef65d-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ef65d-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ef65d-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ef65d-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef65d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef65d-119">Requirements</span></span>



| <span data-ttu-id="ef65d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef65d-120">Requirement</span></span> | <span data-ttu-id="ef65d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ef65d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef65d-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef65d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ef65d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef65d-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="ef65d-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef65d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ef65d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef65d-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ef65d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef65d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef65d-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef65d-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef65d-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="ef65d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ef65d-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ef65d-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="ef65d-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef65d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef65d-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ef65d-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ef65d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ef65d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef65d-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef65d-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ef65d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef65d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef65d-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="ef65d-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="ef65d-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="ef65d-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





