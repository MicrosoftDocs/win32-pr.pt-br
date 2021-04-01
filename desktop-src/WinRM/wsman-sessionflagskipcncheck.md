---
title: Método WSMan. SessionFlagSkipCNCheck (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagSkipCNCheck para uso no parâmetro flags de WSMan. CreateSession.
ms.assetid: 44884a9d-ec5f-4822-945d-2681d214a902
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagSkipCNCheck
- Método SessionFlagSkipCNCheck Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagSkipCNCheck
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCNCheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c98981ac166ea7b1b76f1ab322db6c48679a4bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918725"
---
# <a name="wsmansessionflagskipcncheck-method"></a><span data-ttu-id="5dbc2-106">Método WSMan. SessionFlagSkipCNCheck</span><span class="sxs-lookup"><span data-stu-id="5dbc2-106">WSMan.SessionFlagSkipCNCheck method</span></span>

<span data-ttu-id="5dbc2-107">O método **WSMan. SessionFlagSkipCNCheck** retorna o valor do sinalizador de autenticação **WSManFlagSkipCNCheck** para uso no parâmetro *flags* de [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="5dbc2-107">The **WSMan.SessionFlagSkipCNCheck** method returns the value of the **WSManFlagSkipCNCheck** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="5dbc2-108">Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante.</span><span class="sxs-lookup"><span data-stu-id="5dbc2-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="5dbc2-109">Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5dbc2-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="5dbc2-110">**WSManFlagSkipCNCheck** é uma constante na enumeração **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="5dbc2-110">**WSManFlagSkipCNCheck** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="5dbc2-111">Para obter mais informações, consulte [**constantes de autenticação**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5dbc2-111">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5dbc2-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5dbc2-112">Syntax</span></span>


```VB
WSMan.SessionFlagSkipCNCheck( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="5dbc2-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5dbc2-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dbc2-114">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="5dbc2-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5dbc2-115">O valor da constante.</span><span class="sxs-lookup"><span data-stu-id="5dbc2-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dbc2-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5dbc2-116">Return value</span></span>

<span data-ttu-id="5dbc2-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5dbc2-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5dbc2-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5dbc2-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dbc2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dbc2-119">Requirements</span></span>



| <span data-ttu-id="5dbc2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dbc2-120">Requirement</span></span> | <span data-ttu-id="5dbc2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5dbc2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dbc2-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5dbc2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5dbc2-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5dbc2-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="5dbc2-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5dbc2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5dbc2-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5dbc2-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5dbc2-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5dbc2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dbc2-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dbc2-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5dbc2-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="5dbc2-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5dbc2-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5dbc2-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="5dbc2-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5dbc2-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="5dbc2-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5dbc2-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5dbc2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5dbc2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dbc2-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dbc2-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5dbc2-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="5dbc2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dbc2-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="5dbc2-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="5dbc2-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="5dbc2-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





