---
title: External. AccountType
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A Propriedade AccountType recupera o tipo de conta do usuário atual.
ms.assetid: 4fb6de90-a32d-4483-bbae-b23cbff93bd5
keywords:
- External. AccountType Windows Media Player
topic_type:
- apiref
api_name:
- External.accountType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16fce659f38af19157536a4bf763362c35fc9dfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759708"
---
# <a name="externalaccounttype"></a><span data-ttu-id="73666-106">External. AccountType</span><span class="sxs-lookup"><span data-stu-id="73666-106">External.accountType</span></span>

> [!Note]  
> <span data-ttu-id="73666-107">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="73666-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="73666-108">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="73666-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="73666-109">A propriedade **AccountType** recupera o tipo de conta do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="73666-109">The **accountType** property retrieves the account type of the current user.</span></span>

``` syntax
window.external.accountType
      
```

## <a name="possible-values"></a><span data-ttu-id="73666-110">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="73666-110">Possible Values</span></span>

<span data-ttu-id="73666-111">Essa propriedade é uma **cadeia de caracteres** somente leitura que representa o tipo de conta.</span><span class="sxs-lookup"><span data-stu-id="73666-111">This property is a read-only **String** that represents the account type.</span></span> <span data-ttu-id="73666-112">Cadeias de caracteres que representam vários tipos de conta são definidas pelo repositório online.</span><span class="sxs-lookup"><span data-stu-id="73666-112">Strings that represent various account types are defined by the online store.</span></span>

## <a name="remarks"></a><span data-ttu-id="73666-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="73666-113">Remarks</span></span>

<span data-ttu-id="73666-114">Essa propriedade recupera o tipo de conta chamando o método [IWMPContentPartner:: GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) , que é implementado pelo plug-in da loja online.</span><span class="sxs-lookup"><span data-stu-id="73666-114">This property retrieves the account type by calling the [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) method, which is implemented by the online store's plug-in.</span></span> <span data-ttu-id="73666-115">Se o usuário atual estiver conectado à loja online ou o plug-in tiver armazenado em cache as credenciais do usuário, o método **getContentPartnerInfo** poderá determinar o tipo de conta do usuário e retorná-lo ao Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="73666-115">If the current user is logged in to the online store or the plug-in has cached the user's credentials, the **getContentPartnerInfo** method can determine the user's account type and return it to Windows Media Player.</span></span> <span data-ttu-id="73666-116">O tipo de conta é uma cadeia de caracteres que o Windows Media Player não interpreta.</span><span class="sxs-lookup"><span data-stu-id="73666-116">The account type is a string that Windows Media Player does not interpret.</span></span> <span data-ttu-id="73666-117">Em vez disso, o Windows Media Player passa a cadeia de caracteres do plug-in da loja online para o script na página de descoberta da loja online.</span><span class="sxs-lookup"><span data-stu-id="73666-117">Rather, Windows Media Player passes the string from the online store's plug-in to the script on the online store's discovery page.</span></span>

<span data-ttu-id="73666-118">Se o usuário atual não estiver conectado à loja online e o plug-in da loja online não tiver credenciais armazenadas em cache para o usuário, essa propriedade recuperará qualquer cadeia de caracteres que o método **getContentPartnerInfo** retornar nessa situação.</span><span class="sxs-lookup"><span data-stu-id="73666-118">If the current user is not logged in to the online store and the online store's plug-in does not have cached credentials for the user, this property retrieves whatever string the **getContentPartnerInfo** method returns in that situation.</span></span>

## <a name="requirements"></a><span data-ttu-id="73666-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73666-119">Requirements</span></span>



| <span data-ttu-id="73666-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="73666-120">Requirement</span></span> | <span data-ttu-id="73666-121">Valor</span><span class="sxs-lookup"><span data-stu-id="73666-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73666-122">Versão</span><span class="sxs-lookup"><span data-stu-id="73666-122">Version</span></span><br/> | <span data-ttu-id="73666-123">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="73666-123">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="73666-124">DLL</span><span class="sxs-lookup"><span data-stu-id="73666-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="73666-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73666-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73666-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="73666-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73666-127">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="73666-127">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="73666-128">**External. userlogado**</span><span class="sxs-lookup"><span data-stu-id="73666-128">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





