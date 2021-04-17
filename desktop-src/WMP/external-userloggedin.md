---
title: External. userlogado
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External. userlogado
ms.assetid: d02d9486-c692-4f46-bc29-f0aaa45cad0f
keywords:
- External. userlogado no Windows Media Player
topic_type:
- apiref
api_name:
- External.userLoggedIn
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5454dd9d2fa2d771005448a4157c33b5634a30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811101"
---
# <a name="externaluserloggedin"></a><span data-ttu-id="306bd-105">External. userlogado</span><span class="sxs-lookup"><span data-stu-id="306bd-105">External.userLoggedIn</span></span>

> [!Note]  
> <span data-ttu-id="306bd-106">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="306bd-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="306bd-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="306bd-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="306bd-108">A propriedade **Userlogind** recupera um valor que indica se o usuário está conectado à loja online.</span><span class="sxs-lookup"><span data-stu-id="306bd-108">The **userLoggedIn** property retrieves a value indicating whether the user is logged in to the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="306bd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="306bd-109">Syntax</span></span>

``` syntax
window.external.userLoggedIn
```

## <a name="possible-values"></a><span data-ttu-id="306bd-110">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="306bd-110">Possible Values</span></span>

<span data-ttu-id="306bd-111">Esta propriedade é um **booliano** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="306bd-111">This property is a read-only **Boolean**.</span></span> <span data-ttu-id="306bd-112">**Verdadeiro** indica que o usuário está conectado e **false** indica que o usuário está desconectado.</span><span class="sxs-lookup"><span data-stu-id="306bd-112">**TRUE** indicates that the user is logged in, and **FALSE** indicates that the user is logged out.</span></span>

## <a name="requirements"></a><span data-ttu-id="306bd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="306bd-113">Requirements</span></span>



| <span data-ttu-id="306bd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="306bd-114">Requirement</span></span> | <span data-ttu-id="306bd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="306bd-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="306bd-116">Versão</span><span class="sxs-lookup"><span data-stu-id="306bd-116">Version</span></span><br/> | <span data-ttu-id="306bd-117">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="306bd-117">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="306bd-118">DLL</span><span class="sxs-lookup"><span data-stu-id="306bd-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="306bd-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="306bd-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="306bd-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="306bd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="306bd-121">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="306bd-121">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="306bd-122">**External. attemptLogin**</span><span class="sxs-lookup"><span data-stu-id="306bd-122">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="306bd-123">**Evento external. OnLoginChange**</span><span class="sxs-lookup"><span data-stu-id="306bd-123">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> </dl>

 

 





