---
description: Chamado quando o usuário atual solicitou que a identidade do usuário fosse alternada, mas antes do comutador ocorrer.
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: 'Método IIdentityChangeNotify:: QuerySwitchIdentities (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.QuerySwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 42f8033c943e402d434c973f8c768ed5a951811d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828280"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a><span data-ttu-id="bdb1c-103">Método IIdentityChangeNotify:: QuerySwitchIdentities</span><span class="sxs-lookup"><span data-stu-id="bdb1c-103">IIdentityChangeNotify::QuerySwitchIdentities method</span></span>

<span data-ttu-id="bdb1c-104">\[O **QuerySwitchIdentities** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="bdb1c-104">\[**QuerySwitchIdentities** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bdb1c-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="bdb1c-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="bdb1c-106">Chamado quando o usuário atual solicitou que a identidade do usuário fosse alternada, mas antes do comutador ocorrer.</span><span class="sxs-lookup"><span data-stu-id="bdb1c-106">Called when the current user has requested that their user identity be switched, but before the switch occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdb1c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdb1c-107">Syntax</span></span>


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a><span data-ttu-id="bdb1c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdb1c-108">Parameters</span></span>

<span data-ttu-id="bdb1c-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bdb1c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bdb1c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bdb1c-110">Return value</span></span>

<span data-ttu-id="bdb1c-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bdb1c-111">Type: **HRESULT**</span></span>

<span data-ttu-id="bdb1c-112">Resultado da consulta de comutador.</span><span class="sxs-lookup"><span data-stu-id="bdb1c-112">Result of the switch query.</span></span> <span data-ttu-id="bdb1c-113">Se a opção continuar, retorne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bdb1c-113">If the switch should proceed, return S\_OK.</span></span> <span data-ttu-id="bdb1c-114">Caso contrário, \_ a opção retornar E processar \_ cancelada \_ para indicar que a opção de identidade do usuário deve ser anulada.</span><span class="sxs-lookup"><span data-stu-id="bdb1c-114">Otherwise, return E\_PROCESS\_CANCELLED\_SWITCH to indicate that the user identity switch should be aborted.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdb1c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdb1c-115">Remarks</span></span>

<span data-ttu-id="bdb1c-116">Você pode implementar esse método para fornecer um comportamento personalizado para seu aplicativo quando um usuário solicitar que as identidades sejam alternadas.</span><span class="sxs-lookup"><span data-stu-id="bdb1c-116">You may implement this method to provide custom behavior for your application when a user requests that identities be switched.</span></span> <span data-ttu-id="bdb1c-117">Você pode interromper a opção de identidade pendente retornando o valor E \_ processar a \_ opção cancelada \_ .</span><span class="sxs-lookup"><span data-stu-id="bdb1c-117">You can stop the pending identity switch by returning the value E\_PROCESS\_CANCELLED\_SWITCH.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdb1c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdb1c-118">Requirements</span></span>



| <span data-ttu-id="bdb1c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdb1c-119">Requirement</span></span> | <span data-ttu-id="bdb1c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bdb1c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdb1c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdb1c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bdb1c-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bdb1c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bdb1c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdb1c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bdb1c-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bdb1c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bdb1c-125">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="bdb1c-125">End of client support</span></span><br/>    | <span data-ttu-id="bdb1c-126">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bdb1c-126">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="bdb1c-127">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="bdb1c-127">End of server support</span></span><br/>    | <span data-ttu-id="bdb1c-128">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bdb1c-128">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="bdb1c-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bdb1c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdb1c-130"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdb1c-130"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="bdb1c-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="bdb1c-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bdb1c-132"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bdb1c-132"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="bdb1c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="bdb1c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdb1c-134"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdb1c-134"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bdb1c-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdb1c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdb1c-136">**IIdentityChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="bdb1c-136">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> <dt>

[<span data-ttu-id="bdb1c-137">**IIdentityChangeNotify::SwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="bdb1c-137">**IIdentityChangeNotify::SwitchIdentities**</span></span>](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




