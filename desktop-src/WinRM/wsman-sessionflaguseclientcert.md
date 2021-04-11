---
title: Método WSMan. SessionFlagUseClientCertificate (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagUseClientCertificate para uso no parâmetro flags do método WSMan. CreateSession.
ms.assetid: b0ec4dbb-3a98-45e8-8f6b-74b858d6c3fc
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagUseClientCertificate
- Método SessionFlagUseClientCertificate Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagUseClientCertificate
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseClientCertificate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbbcbc1a920cbd7ce2b58e29c52fc08245b8aa35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294756"
---
# <a name="wsmansessionflaguseclientcertificate-method"></a><span data-ttu-id="6dcbb-106">Método WSMan. SessionFlagUseClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6dcbb-106">WSMan.SessionFlagUseClientCertificate method</span></span>

<span data-ttu-id="6dcbb-107">O método **WSMan. SessionFlagUseClientCertificate** retorna o valor do sinalizador de autenticação **WSManFlagUseClientCertificate** para uso no parâmetro *flags* do método [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="6dcbb-107">The **WSMan.SessionFlagUseClientCertificate** method returns the value of the **WSManFlagUseClientCertificate** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="6dcbb-108">Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante.</span><span class="sxs-lookup"><span data-stu-id="6dcbb-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="6dcbb-109">Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6dcbb-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="6dcbb-110">**WSManFlagUseClientCertificate** é uma constante na enumeração **\_ \_ WSManAuthenticationFlags** .</span><span class="sxs-lookup"><span data-stu-id="6dcbb-110">**WSManFlagUseClientCertificate** is a constant in the **\_\_WSManAuthenticationFlags** enumeration.</span></span> <span data-ttu-id="6dcbb-111">Para obter mais informações, consulte [constantes de autenticação](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6dcbb-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6dcbb-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6dcbb-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseClientCertificate( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="6dcbb-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6dcbb-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dcbb-114">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="6dcbb-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dcbb-115">O valor da constante.</span><span class="sxs-lookup"><span data-stu-id="6dcbb-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dcbb-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6dcbb-116">Return value</span></span>

<span data-ttu-id="6dcbb-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6dcbb-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6dcbb-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6dcbb-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dcbb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6dcbb-119">Requirements</span></span>



| <span data-ttu-id="6dcbb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dcbb-120">Requirement</span></span> | <span data-ttu-id="6dcbb-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6dcbb-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dcbb-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6dcbb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6dcbb-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6dcbb-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="6dcbb-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6dcbb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6dcbb-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6dcbb-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6dcbb-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6dcbb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dcbb-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6dcbb-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6dcbb-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="6dcbb-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6dcbb-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6dcbb-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="6dcbb-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6dcbb-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="6dcbb-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6dcbb-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6dcbb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6dcbb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dcbb-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dcbb-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6dcbb-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6dcbb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dcbb-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="6dcbb-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="6dcbb-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="6dcbb-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





