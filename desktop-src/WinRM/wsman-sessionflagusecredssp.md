---
title: Método WSMan. SessionFlagUseCredSsp (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagUseCredSsp para uso no parâmetro flags do método WSMan. CreateSession.
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagUseCredSsp
- Método SessionFlagUseCredSsp Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagUseCredSsp
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseCredSsp
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed5dfbaba3e705f100cdd373e194174f4654a7d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455195"
---
# <a name="wsmansessionflagusecredssp-method"></a><span data-ttu-id="b892e-106">Método WSMan. SessionFlagUseCredSsp</span><span class="sxs-lookup"><span data-stu-id="b892e-106">WSMan.SessionFlagUseCredSsp method</span></span>

<span data-ttu-id="b892e-107">Retorna o valor do sinalizador de autenticação **WSManFlagUseCredSsp** para uso no parâmetro *flags* do método [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="b892e-107">Returns the value of the **WSManFlagUseCredSsp** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="b892e-108">Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante.</span><span class="sxs-lookup"><span data-stu-id="b892e-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="b892e-109">Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b892e-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="b892e-110">**WSManFlagUseCredSsp** é uma constante na enumeração **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="b892e-110">**WSManFlagUseCredSsp** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="b892e-111">Para obter mais informações, consulte [constantes de autenticação](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b892e-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b892e-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b892e-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseCredSsp( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="b892e-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b892e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b892e-114">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="b892e-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b892e-115">O valor da constante.</span><span class="sxs-lookup"><span data-stu-id="b892e-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b892e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b892e-116">Return value</span></span>

<span data-ttu-id="b892e-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b892e-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b892e-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b892e-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b892e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b892e-119">Requirements</span></span>



| <span data-ttu-id="b892e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b892e-120">Requirement</span></span> | <span data-ttu-id="b892e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b892e-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b892e-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b892e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b892e-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b892e-123">Windows 7</span></span><br/>                                                                                                        |
| <span data-ttu-id="b892e-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b892e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b892e-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b892e-125">Windows Server 2008 R2</span></span><br/>                                                                                           |
| <span data-ttu-id="b892e-126">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="b892e-126">Redistributable</span></span><br/>          | <span data-ttu-id="b892e-127">Windows Management Framework no Windows Server 2008 com SP2, Windows Vista com SP1 e Windows Vista com SP2</span><span class="sxs-lookup"><span data-stu-id="b892e-127">Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2</span></span><br/> |
| <span data-ttu-id="b892e-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b892e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b892e-129"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b892e-129"><dt>WSManDisp.h</dt></span></span> </dl>                                      |
| <span data-ttu-id="b892e-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="b892e-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b892e-131"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b892e-131"><dt>WSManDisp.idl</dt></span></span> </dl>                                    |
| <span data-ttu-id="b892e-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b892e-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="b892e-133"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b892e-133"><dt>WSManDisp.tlb</dt></span></span> </dl>                                    |
| <span data-ttu-id="b892e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b892e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b892e-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b892e-135"><dt>WSMAuto.dll</dt></span></span> </dl>                                      |



## <a name="see-also"></a><span data-ttu-id="b892e-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="b892e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b892e-137">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="b892e-137">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="b892e-138">**Session**</span><span class="sxs-lookup"><span data-stu-id="b892e-138">**Session**</span></span>](session.md)
</dt> </dl>

 

 





