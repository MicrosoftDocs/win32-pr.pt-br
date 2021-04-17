---
title: Método external. Authenticate
description: O método Authenticate inicia uma tentativa de autenticar o usuário.
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- método de autenticação do Windows Media Player
- método de autenticação do Windows Media Player, classe externa
- Classe externa Windows Media Player, método de autenticação
topic_type:
- apiref
api_name:
- External.authenticate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2bba0afb80c4285ad8fa8d2c20191321315d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770491"
---
# <a name="externalauthenticate-method"></a><span data-ttu-id="f819c-106">Método external. Authenticate</span><span class="sxs-lookup"><span data-stu-id="f819c-106">External.authenticate method</span></span>

<span data-ttu-id="f819c-107">O método **Authenticate** inicia uma tentativa de autenticar o usuário.</span><span class="sxs-lookup"><span data-stu-id="f819c-107">The **authenticate** method initiates an attempt to authenticate the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="f819c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f819c-108">Syntax</span></span>


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a><span data-ttu-id="f819c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f819c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f819c-110">*AuthenticationIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f819c-110">*AuthenticationIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f819c-111">**Número** (**longo**) que especifica o índice de uma página da Web de autenticação com êxito.</span><span class="sxs-lookup"><span data-stu-id="f819c-111">**Number** (**long**) that specifies the index of an authentication-success webpage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f819c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f819c-112">Return value</span></span>

<span data-ttu-id="f819c-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f819c-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f819c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f819c-114">Remarks</span></span>

<span data-ttu-id="f819c-115">Determinados links em uma página de descoberta têm destinos que devem ser exibidos somente depois que o usuário tiver sido autenticado.</span><span class="sxs-lookup"><span data-stu-id="f819c-115">Certain links on a discovery page have targets that should be displayed only after the user has been authenticated.</span></span> <span data-ttu-id="f819c-116">A página de descoberta, o Windows Media Player e o plug-in da loja online usam as seguintes etapas para autenticar o usuário e exibir a página da Web de destino:</span><span class="sxs-lookup"><span data-stu-id="f819c-116">The discovery page, Windows Media Player, and the online store's plug-in use the following steps to authenticate the user and display the target webpage:</span></span>

1.  <span data-ttu-id="f819c-117">O script em uma página de descoberta chama o *externo*. método **Authenticate** .</span><span class="sxs-lookup"><span data-stu-id="f819c-117">Script on a discovery page calls the *External*.**authenticate** method.</span></span>
2.  <span data-ttu-id="f819c-118">O Windows Media Player exibe uma caixa de diálogo para obter um nome de usuário e senha.</span><span class="sxs-lookup"><span data-stu-id="f819c-118">Windows Media Player displays a dialog box to obtain a user name and password.</span></span>
3.  <span data-ttu-id="f819c-119">O Windows Media Player chama [IWMPContentPartner:: Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), que inicia a tentativa de autenticação e retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f819c-119">Windows Media Player calls [IWMPContentPartner::Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), which initiates the authentication attempt and returns immediately.</span></span>
4.  <span data-ttu-id="f819c-120">Quando a tentativa de autenticação for concluída, o plug-in do repositório online chamará [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passando wmpcnAuthResult e um valor booliano que indica se a tentativa foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f819c-120">When the authentication attempt is complete, the online store's plug-in calls [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnAuthResult and a Boolean value that indicates whether the attempt was successful.</span></span>
5.  <span data-ttu-id="f819c-121">Se a tentativa de autenticação foi bem-sucedida, o Windows Media Player chama [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passando g \_ szItemInfo \_ AUTHENTICATIONSUCCESSURL para obter a URL de uma página da Web de autenticação-êxito.</span><span class="sxs-lookup"><span data-stu-id="f819c-121">If the authentication attempt was successful, Windows Media Player calls [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passing g\_szItemInfo\_AuthenticationSuccessURL, to obtain the URL of an authentication-success webpage.</span></span> <span data-ttu-id="f819c-122">Nesta chamada, o Windows Media Player passa o mesmo índice passado pela página de descoberta para o *externo*. método **Authenticate** .</span><span class="sxs-lookup"><span data-stu-id="f819c-122">In this call, Windows Media Player passes the same index that the discovery page passed to the *External*.**authenticate** method.</span></span>
6.  <span data-ttu-id="f819c-123">O Windows Media Player exibe a página da Web autenticação-êxito.</span><span class="sxs-lookup"><span data-stu-id="f819c-123">Windows Media Player displays the authentication-success webpage.</span></span>

## <a name="requirements"></a><span data-ttu-id="f819c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f819c-124">Requirements</span></span>



| <span data-ttu-id="f819c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f819c-125">Requirement</span></span> | <span data-ttu-id="f819c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f819c-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f819c-127">Versão</span><span class="sxs-lookup"><span data-stu-id="f819c-127">Version</span></span><br/> | <span data-ttu-id="f819c-128">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="f819c-128">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="f819c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f819c-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="f819c-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f819c-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f819c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f819c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f819c-132">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="f819c-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="f819c-133">**External. attemptLogin**</span><span class="sxs-lookup"><span data-stu-id="f819c-133">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="f819c-134">**External. userlogado**</span><span class="sxs-lookup"><span data-stu-id="f819c-134">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





