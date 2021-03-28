---
description: Chamado quando as identidades de usuário são alternadas.
ms.assetid: e88383fc-e58e-4987-be4b-8ce2ab1368db
title: 'Método IIdentityChangeNotify:: SwitchIdentities (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.SwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 925b52a4470c768501dd928784d85a89d05a90c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988962"
---
# <a name="iidentitychangenotifyswitchidentities-method"></a><span data-ttu-id="58d54-103">Método IIdentityChangeNotify:: SwitchIdentities</span><span class="sxs-lookup"><span data-stu-id="58d54-103">IIdentityChangeNotify::SwitchIdentities method</span></span>

<span data-ttu-id="58d54-104">\[O **SwitchIdentities** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="58d54-104">\[**SwitchIdentities** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="58d54-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="58d54-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="58d54-106">Chamado quando as identidades de usuário são alternadas.</span><span class="sxs-lookup"><span data-stu-id="58d54-106">Called when user identities are switched.</span></span>

## <a name="syntax"></a><span data-ttu-id="58d54-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58d54-107">Syntax</span></span>


```C++
HRESULT SwitchIdentities();
```



## <a name="parameters"></a><span data-ttu-id="58d54-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58d54-108">Parameters</span></span>

<span data-ttu-id="58d54-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="58d54-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="58d54-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58d54-110">Return value</span></span>

<span data-ttu-id="58d54-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="58d54-111">Type: **HRESULT**</span></span>

<span data-ttu-id="58d54-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="58d54-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="58d54-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="58d54-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="58d54-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="58d54-114">Remarks</span></span>

<span data-ttu-id="58d54-115">Você pode implementar esse método para fornecer um comportamento personalizado para seu aplicativo quando um usuário tiver alternado com êxito as identidades.</span><span class="sxs-lookup"><span data-stu-id="58d54-115">You may implement this method to provide custom behavior for your application when a user has successfully switched identities.</span></span> <span data-ttu-id="58d54-116">Para fornecer um comportamento personalizado antes que ocorra uma alternância de identidade do usuário, implemente o método [**IIdentityChangeNotify:: QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md) .</span><span class="sxs-lookup"><span data-stu-id="58d54-116">To provide custom behavior before a user identity switch occurs, implement the [**IIdentityChangeNotify::QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="58d54-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58d54-117">Requirements</span></span>



| <span data-ttu-id="58d54-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="58d54-118">Requirement</span></span> | <span data-ttu-id="58d54-119">Valor</span><span class="sxs-lookup"><span data-stu-id="58d54-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58d54-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58d54-120">Minimum supported client</span></span><br/> | <span data-ttu-id="58d54-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="58d54-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="58d54-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58d54-122">Minimum supported server</span></span><br/> | <span data-ttu-id="58d54-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="58d54-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="58d54-124">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="58d54-124">End of client support</span></span><br/>    | <span data-ttu-id="58d54-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="58d54-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="58d54-126">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="58d54-126">End of server support</span></span><br/>    | <span data-ttu-id="58d54-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="58d54-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="58d54-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="58d54-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="58d54-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="58d54-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="58d54-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="58d54-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="58d54-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="58d54-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="58d54-132">DLL</span><span class="sxs-lookup"><span data-stu-id="58d54-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58d54-133"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58d54-133"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="58d54-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="58d54-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58d54-135">**IIdentityChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="58d54-135">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> <dt>

[<span data-ttu-id="58d54-136">**IIdentityChangeNotify::QuerySwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="58d54-136">**IIdentityChangeNotify::QuerySwitchIdentities**</span></span>](iidentitychangenotify-queryswitchidentities.md)
</dt> </dl>

 

 




