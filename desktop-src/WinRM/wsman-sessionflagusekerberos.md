---
title: Método WSMan. SessionFlagUseKerberos (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagUseKerberos para uso no parâmetro flags de WSMan. CreateSession.
ms.assetid: be005312-1e87-4371-9791-709a9be46f7c
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagUseKerberos
- Método SessionFlagUseKerberos Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagUseKerberos
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseKerberos
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e7436a5b79480b39c093545a0b579da3d13082
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644679"
---
# <a name="wsmansessionflagusekerberos-method"></a><span data-ttu-id="2f09a-106">Método WSMan. SessionFlagUseKerberos</span><span class="sxs-lookup"><span data-stu-id="2f09a-106">WSMan.SessionFlagUseKerberos method</span></span>

<span data-ttu-id="2f09a-107">O método **WSMan. SessionFlagUseKerberos** retorna o valor do sinalizador de autenticação **WSManFlagUseKerberos** para uso no parâmetro *flags* de [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="2f09a-107">The **WSMan.SessionFlagUseKerberos** method returns the value of the **WSManFlagUseKerberos** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="2f09a-108">Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante.</span><span class="sxs-lookup"><span data-stu-id="2f09a-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="2f09a-109">Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2f09a-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="2f09a-110">**WSManFlagUseKerberos** é uma constante na enumeração **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="2f09a-110">**WSManFlagUseKerberos** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="2f09a-111">Para obter mais informações, consulte [constantes de autenticação](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2f09a-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f09a-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f09a-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseKerberos( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="2f09a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f09a-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f09a-114">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="2f09a-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f09a-115">O valor da constante.</span><span class="sxs-lookup"><span data-stu-id="2f09a-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f09a-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f09a-116">Return value</span></span>

<span data-ttu-id="2f09a-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2f09a-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2f09a-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2f09a-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f09a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f09a-119">Requirements</span></span>



| <span data-ttu-id="2f09a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f09a-120">Requirement</span></span> | <span data-ttu-id="2f09a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2f09a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f09a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f09a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2f09a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f09a-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2f09a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f09a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2f09a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f09a-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2f09a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f09a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f09a-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f09a-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f09a-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="2f09a-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2f09a-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2f09a-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="2f09a-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f09a-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f09a-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2f09a-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2f09a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2f09a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f09a-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f09a-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2f09a-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2f09a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f09a-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="2f09a-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="2f09a-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="2f09a-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





