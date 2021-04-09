---
title: Método WSMan. SessionFlagSkipCACheck (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagSkipCACheck para uso no parâmetro flags de WSMan. CreateSession.
ms.assetid: a67cadb3-c20a-4a58-a13b-5bbd23c547d1
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagSkipCACheck
- Método SessionFlagSkipCACheck Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagSkipCACheck
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCACheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e536112b16ad8cbab3cebb2de582a2e0ea8aec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008876"
---
# <a name="wsmansessionflagskipcacheck-method"></a><span data-ttu-id="7d882-106">Método WSMan. SessionFlagSkipCACheck</span><span class="sxs-lookup"><span data-stu-id="7d882-106">WSMan.SessionFlagSkipCACheck method</span></span>

<span data-ttu-id="7d882-107">O método **WSMan. SessionFlagSkipCACheck** retorna o valor do sinalizador de autenticação **WSManFlagSkipCACheck** para uso no parâmetro *flags* de [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="7d882-107">The **WSMan.SessionFlagSkipCACheck** method returns the value of the **WSManFlagSkipCACheck** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="7d882-108">Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante.</span><span class="sxs-lookup"><span data-stu-id="7d882-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="7d882-109">Para obter mais informações sobre como chamar esse método e exemplos de código, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7d882-109">For more information about how to call this method and code examples, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="7d882-110">**WSManFlagSkipCACheck** é uma constante na enumeração **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="7d882-110">**WSManFlagSkipCACheck** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="7d882-111">Para obter mais informações, consulte [**constantes de autenticação**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7d882-111">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7d882-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d882-112">Syntax</span></span>


```VB
WSMan.SessionFlagSkipCACheck( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="7d882-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d882-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d882-114">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="7d882-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d882-115">O valor da constante.</span><span class="sxs-lookup"><span data-stu-id="7d882-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d882-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7d882-116">Return value</span></span>

<span data-ttu-id="7d882-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7d882-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7d882-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7d882-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d882-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d882-119">Requirements</span></span>



| <span data-ttu-id="7d882-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d882-120">Requirement</span></span> | <span data-ttu-id="7d882-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7d882-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d882-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d882-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7d882-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d882-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="7d882-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d882-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7d882-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d882-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7d882-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d882-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d882-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d882-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7d882-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="7d882-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7d882-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7d882-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="7d882-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7d882-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="7d882-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7d882-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7d882-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7d882-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d882-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d882-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7d882-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d882-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d882-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="7d882-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="7d882-136">**Session**</span><span class="sxs-lookup"><span data-stu-id="7d882-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





