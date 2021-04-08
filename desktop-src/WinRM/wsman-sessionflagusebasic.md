---
title: Método WSMan. SessionFlagUseBasic (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagUseBasic para uso no parâmetro flags do método WSMan. CreateSession.
ms.assetid: 789ecef9-7871-43af-9d63-018f1d99bd09
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagUseBasic
- Método SessionFlagUseBasic Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagUseBasic
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseBasic
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41641e0398791ab46c81f71f967f2d43700a2984
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009016"
---
# <a name="wsmansessionflagusebasic-method"></a><span data-ttu-id="d46e3-106">Método WSMan. SessionFlagUseBasic</span><span class="sxs-lookup"><span data-stu-id="d46e3-106">WSMan.SessionFlagUseBasic method</span></span>

<span data-ttu-id="d46e3-107">O método **WSMan. SessionFlagUseBasic** retorna o valor do sinalizador de autenticação **WSManFlagUseBasic** para uso no parâmetro *flags* do método [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="d46e3-107">The **WSMan.SessionFlagUseBasic** method returns the value of the authentication flag **WSManFlagUseBasic** for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="d46e3-108">Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante.</span><span class="sxs-lookup"><span data-stu-id="d46e3-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="d46e3-109">Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d46e3-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="d46e3-110">**WSManFlagUseBasic** é uma constante na enumeração **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="d46e3-110">**WSManFlagUseBasic** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="d46e3-111">Para obter mais informações, consulte [**constantes de autenticação**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d46e3-111">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d46e3-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d46e3-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseBasic( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="d46e3-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d46e3-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d46e3-114">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="d46e3-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d46e3-115">O valor da constante.</span><span class="sxs-lookup"><span data-stu-id="d46e3-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d46e3-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d46e3-116">Return value</span></span>

<span data-ttu-id="d46e3-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d46e3-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d46e3-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d46e3-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d46e3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d46e3-119">Requirements</span></span>



| <span data-ttu-id="d46e3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d46e3-120">Requirement</span></span> | <span data-ttu-id="d46e3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d46e3-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d46e3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d46e3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d46e3-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d46e3-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="d46e3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d46e3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d46e3-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d46e3-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d46e3-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d46e3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d46e3-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d46e3-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d46e3-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="d46e3-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d46e3-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d46e3-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="d46e3-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d46e3-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="d46e3-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d46e3-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d46e3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d46e3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d46e3-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d46e3-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d46e3-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d46e3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d46e3-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="d46e3-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="d46e3-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="d46e3-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





