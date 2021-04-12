---
title: Método WSMan. SessionFlagEnableSPNServerPort (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagEnableSPNServerPort para uso no parâmetro flags do método WSMan. CreateSession.
ms.assetid: a18a87e6-dcee-4e9f-8e8c-262fef36ab1a
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagEnableSPNServerPort
- Método SessionFlagEnableSPNServerPort Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagEnableSPNServerPort
topic_type:
- apiref
api_name:
- WSMan.SessionFlagEnableSPNServerPort
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4153f088079b58b3b0e048f2cd8f38b3524754a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499494"
---
# <a name="wsmansessionflagenablespnserverport-method"></a><span data-ttu-id="760c7-106">Método WSMan. SessionFlagEnableSPNServerPort</span><span class="sxs-lookup"><span data-stu-id="760c7-106">WSMan.SessionFlagEnableSPNServerPort method</span></span>

<span data-ttu-id="760c7-107">O método **WSMan. SessionFlagEnableSPNServerPort** retorna o valor do sinalizador de autenticação **WSManFlagEnableSPNServerPort** para uso no parâmetro *flags* do método [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="760c7-107">The **WSMan.SessionFlagEnableSPNServerPort** method returns the value of the authentication flag **WSManFlagEnableSPNServerPort** for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="760c7-108">Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante.</span><span class="sxs-lookup"><span data-stu-id="760c7-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="760c7-109">Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="760c7-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="760c7-110">**WSManFlagEnableSPNServerPort** é uma constante na enumeração **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="760c7-110">**WSManFlagEnableSPNServerPort** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="760c7-111">Para obter mais informações, consulte [**outras constantes de sessão**](other-session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="760c7-111">For more information, see [**Other Session Constants**](other-session-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="760c7-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="760c7-112">Syntax</span></span>


```VB
WSMan.SessionFlagEnableSPNServerPort( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="760c7-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="760c7-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="760c7-114">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="760c7-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="760c7-115">O valor da constante.</span><span class="sxs-lookup"><span data-stu-id="760c7-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="760c7-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="760c7-116">Return value</span></span>

<span data-ttu-id="760c7-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="760c7-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="760c7-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="760c7-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="760c7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="760c7-119">Requirements</span></span>



| <span data-ttu-id="760c7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="760c7-120">Requirement</span></span> | <span data-ttu-id="760c7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="760c7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="760c7-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="760c7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="760c7-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="760c7-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="760c7-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="760c7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="760c7-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="760c7-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="760c7-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="760c7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="760c7-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="760c7-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="760c7-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="760c7-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="760c7-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="760c7-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="760c7-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="760c7-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="760c7-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="760c7-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="760c7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="760c7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="760c7-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="760c7-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="760c7-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="760c7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="760c7-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="760c7-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="760c7-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="760c7-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





