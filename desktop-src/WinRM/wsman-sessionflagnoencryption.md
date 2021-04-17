---
title: Método WSMan. SessionFlagNoEncryption (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagNoEncryption para uso no parâmetro flags do método WSMan. CreateSession.
ms.assetid: 15c76f0e-85ae-4ee3-bf9f-ba32195d9adc
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagNoEncryption
- Método SessionFlagNoEncryption Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagNoEncryption
topic_type:
- apiref
api_name:
- WSMan.SessionFlagNoEncryption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4c7a85e97afd67ab6b1114248a9c4b3ee3ebbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813705"
---
# <a name="wsmansessionflagnoencryption-method"></a><span data-ttu-id="c192f-106">Método WSMan. SessionFlagNoEncryption</span><span class="sxs-lookup"><span data-stu-id="c192f-106">WSMan.SessionFlagNoEncryption method</span></span>

<span data-ttu-id="c192f-107">O método **WSMan. SessionFlagNoEncryption** retorna o valor do sinalizador de autenticação **WSManFlagNoEncryption** para uso no parâmetro *flags* do método [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="c192f-107">The **WSMan.SessionFlagNoEncryption** method returns the value of the **WSManFlagNoEncryption** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="c192f-108">Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante.</span><span class="sxs-lookup"><span data-stu-id="c192f-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="c192f-109">Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c192f-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="c192f-110">**WSManFlagNoEncryption** é uma constante na enumeração **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="c192f-110">**WSManFlagNoEncryption** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="c192f-111">Para obter mais informações, consulte [outras constantes de sessão](other-session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c192f-111">For more information, see [Other Session Constants](other-session-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c192f-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c192f-112">Syntax</span></span>


```VB
WSMan.SessionFlagNoEncryption( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="c192f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c192f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c192f-114">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="c192f-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c192f-115">O valor da constante.</span><span class="sxs-lookup"><span data-stu-id="c192f-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c192f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c192f-116">Return value</span></span>

<span data-ttu-id="c192f-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c192f-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c192f-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c192f-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c192f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c192f-119">Requirements</span></span>



| <span data-ttu-id="c192f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c192f-120">Requirement</span></span> | <span data-ttu-id="c192f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c192f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c192f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c192f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c192f-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c192f-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c192f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c192f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c192f-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c192f-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c192f-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c192f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c192f-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c192f-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c192f-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="c192f-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c192f-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c192f-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c192f-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c192f-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="c192f-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c192f-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c192f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c192f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c192f-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c192f-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c192f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="c192f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c192f-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="c192f-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="c192f-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="c192f-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





