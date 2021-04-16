---
title: Método external. attemptLogin
description: O método attemptLogin exibe uma caixa de diálogo para que o usuário possa tentar fazer logon na loja online.
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- método attemptLogin Windows Media Player
- método attemptLogin Windows Media Player, classe externa
- Classe externa Windows Media Player, método attemptLogin
topic_type:
- apiref
api_name:
- External.attemptLogin
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86958c241f2399efbe342371b8cd4cfd376ff628
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794473"
---
# <a name="externalattemptlogin-method"></a><span data-ttu-id="84045-106">Método external. attemptLogin</span><span class="sxs-lookup"><span data-stu-id="84045-106">External.attemptLogin method</span></span>

<span data-ttu-id="84045-107">O método **attemptLogin** exibe uma caixa de diálogo para que o usuário possa tentar fazer logon na loja online.</span><span class="sxs-lookup"><span data-stu-id="84045-107">The **attemptLogin** method displays a dialog box so the user can attempt to log in to the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="84045-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84045-108">Syntax</span></span>


```JScript
External.attemptLogin()
```



## <a name="parameters"></a><span data-ttu-id="84045-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84045-109">Parameters</span></span>

<span data-ttu-id="84045-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="84045-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="84045-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="84045-111">Return value</span></span>

<span data-ttu-id="84045-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="84045-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="84045-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="84045-113">Remarks</span></span>

<span data-ttu-id="84045-114">Se a tentativa de logon resultar em uma alteração de status de logon, o Windows Media Player gerará o evento [OnLoginChange](external-onloginchange-event.md) .</span><span class="sxs-lookup"><span data-stu-id="84045-114">If the log-in attempt results in a change of log-in status, Windows Media Player raises the [OnLoginChange](external-onloginchange-event.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="84045-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84045-115">Requirements</span></span>



| <span data-ttu-id="84045-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="84045-116">Requirement</span></span> | <span data-ttu-id="84045-117">Valor</span><span class="sxs-lookup"><span data-stu-id="84045-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="84045-118">Versão</span><span class="sxs-lookup"><span data-stu-id="84045-118">Version</span></span><br/> | <span data-ttu-id="84045-119">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="84045-119">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="84045-120">DLL</span><span class="sxs-lookup"><span data-stu-id="84045-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="84045-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84045-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84045-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="84045-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84045-123">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="84045-123">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="84045-124">**Evento external. OnLoginChange**</span><span class="sxs-lookup"><span data-stu-id="84045-124">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> <dt>

[<span data-ttu-id="84045-125">**External. userlogado**</span><span class="sxs-lookup"><span data-stu-id="84045-125">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> <dt>

[<span data-ttu-id="84045-126">**IWMPContentPartner:: logon**</span><span class="sxs-lookup"><span data-stu-id="84045-126">**IWMPContentPartner::Login**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[<span data-ttu-id="84045-127">**Gerenciando o logon**</span><span class="sxs-lookup"><span data-stu-id="84045-127">**Managing Login**</span></span>](managing-login.md)
</dt> </dl>

 

 





