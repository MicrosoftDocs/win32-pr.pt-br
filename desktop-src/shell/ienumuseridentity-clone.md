---
description: 'IEnumUserIdentity:: Clone não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.'
ms.assetid: dde9afca-db8d-41ba-afa0-94eadecb695b
title: 'Método IEnumUserIdentity:: clone (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Clone
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: ebdec426fe7ab591c801c00b637211e903cf5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988966"
---
# <a name="ienumuseridentityclone-method"></a><span data-ttu-id="df648-104">Método IEnumUserIdentity:: clone</span><span class="sxs-lookup"><span data-stu-id="df648-104">IEnumUserIdentity::Clone method</span></span>

<span data-ttu-id="df648-105">\[**IEnumUserIdentity:: clone** não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="df648-105">\[**IEnumUserIdentity::Clone** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="df648-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="df648-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="df648-107">Obtém uma cópia da enumeração atual.</span><span class="sxs-lookup"><span data-stu-id="df648-107">Gets a copy of the current enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="df648-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df648-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumUserIdentity **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="df648-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df648-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df648-110">*ppEnum* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="df648-110">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df648-111">Tipo: **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="df648-111">Type: **[**IEnumUserIdentity**](ienumuseridentity.md)\*\***</span></span>

<span data-ttu-id="df648-112">O endereço de um ponteiro que recebe uma cópia dessa enumeração.</span><span class="sxs-lookup"><span data-stu-id="df648-112">The address of a pointer that receives a copy of this enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df648-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df648-113">Return value</span></span>

<span data-ttu-id="df648-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="df648-114">Type: **HRESULT**</span></span>

<span data-ttu-id="df648-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="df648-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="df648-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="df648-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="df648-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="df648-117">Remarks</span></span>

<span data-ttu-id="df648-118">[**IEnumUserIdentity**](ienumuseridentity.md) mantém uma contagem interna que especifica qual interface está próxima de ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="df648-118">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="df648-119">O valor dessa contagem será aplicado à interface recebida por *ppEnum*.</span><span class="sxs-lookup"><span data-stu-id="df648-119">The value of this count will be applied to the interface received by *ppenum*.</span></span> <span data-ttu-id="df648-120">Para redefinir a contagem, chame [**IEnumUserIdentity:: Reset**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="df648-120">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df648-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df648-121">Requirements</span></span>



| <span data-ttu-id="df648-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="df648-122">Requirement</span></span> | <span data-ttu-id="df648-123">Valor</span><span class="sxs-lookup"><span data-stu-id="df648-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df648-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df648-124">Minimum supported client</span></span><br/> | <span data-ttu-id="df648-125">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="df648-125">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="df648-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df648-126">Minimum supported server</span></span><br/> | <span data-ttu-id="df648-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="df648-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="df648-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="df648-128">End of client support</span></span><br/>    | <span data-ttu-id="df648-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="df648-129">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="df648-130">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="df648-130">End of server support</span></span><br/>    | <span data-ttu-id="df648-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="df648-131">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="df648-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df648-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="df648-133"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="df648-133"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="df648-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="df648-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="df648-135"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="df648-135"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="df648-136">DLL</span><span class="sxs-lookup"><span data-stu-id="df648-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df648-137"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df648-137"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df648-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="df648-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df648-139">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="df648-139">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="df648-140">**IEnumUserIdentity:: Reset**</span><span class="sxs-lookup"><span data-stu-id="df648-140">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> </dl>

 

 




