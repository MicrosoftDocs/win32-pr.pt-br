---
title: Settings. mediaAccessRights
description: A propriedade mediaAccessRights recupera um valor que indica os direitos concedidos atualmente para acesso à biblioteca.
ms.assetid: 744e696d-29d2-44b1-a296-5b5d007b689f
keywords:
- Settings. mediaAccessRights Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mediaAccessRights
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bcfb667a1aa09e84ae90324736291d421a3941
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105807325"
---
# <a name="settingsmediaaccessrights"></a><span data-ttu-id="fb3e5-104">Settings. mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="fb3e5-104">Settings.mediaAccessRights</span></span>

<span data-ttu-id="fb3e5-105">A propriedade **mediaAccessRights** recupera um valor que indica os direitos concedidos atualmente para acesso à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="fb3e5-105">The **mediaAccessRights** property retrieves a value indicating the rights currently granted for library access.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb3e5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb3e5-106">Syntax</span></span>

<span data-ttu-id="fb3e5-107">Player. Settings. mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="fb3e5-107">player.settings.mediaAccessRights</span></span>

## <a name="possible-values"></a><span data-ttu-id="fb3e5-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="fb3e5-108">Possible Values</span></span>

<span data-ttu-id="fb3e5-109">Esta propriedade é uma **cadeia de caracteres** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fb3e5-109">This property is a read-only **String**.</span></span>



| <span data-ttu-id="fb3e5-110">Valor</span><span class="sxs-lookup"><span data-stu-id="fb3e5-110">Value</span></span> | <span data-ttu-id="fb3e5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb3e5-111">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="fb3e5-112">none</span><span class="sxs-lookup"><span data-stu-id="fb3e5-112">none</span></span>  | <span data-ttu-id="fb3e5-113">Somente direitos de acesso do item atual.</span><span class="sxs-lookup"><span data-stu-id="fb3e5-113">Current item access rights only.</span></span> |
| <span data-ttu-id="fb3e5-114">ler</span><span class="sxs-lookup"><span data-stu-id="fb3e5-114">read</span></span>  | <span data-ttu-id="fb3e5-115">Somente direitos de acesso de leitura.</span><span class="sxs-lookup"><span data-stu-id="fb3e5-115">Read access rights only.</span></span>         |
| <span data-ttu-id="fb3e5-116">completa</span><span class="sxs-lookup"><span data-stu-id="fb3e5-116">full</span></span>  | <span data-ttu-id="fb3e5-117">Direitos de acesso de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fb3e5-117">Read/Write access rights.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="fb3e5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb3e5-118">Remarks</span></span>

<span data-ttu-id="fb3e5-119">Uma página da Web deve primeiro solicitar permissão do usuário para ler informações ou gravar dados na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="fb3e5-119">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="fb3e5-120">Isso significa que determinados métodos, propriedades e eventos ficarão inacessíveis a partir do código se os direitos de acesso apropriados não tiverem sido concedidos.</span><span class="sxs-lookup"><span data-stu-id="fb3e5-120">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="fb3e5-121">Para obter direitos de acesso, o aplicativo chama *as configurações*. **requestMediaAccessRights**, passando um parâmetro que especifica o nível de direitos de acesso desejado.</span><span class="sxs-lookup"><span data-stu-id="fb3e5-121">To obtain access rights, the application calls *Settings*.**requestMediaAccessRights**, passing a parameter that specifies the desired access rights level.</span></span>

<span data-ttu-id="fb3e5-122">**Windows Media Player 10 Mobile**: essa propriedade sempre retorna **Full**.</span><span class="sxs-lookup"><span data-stu-id="fb3e5-122">**Windows Media Player 10 Mobile**: This property always returns **full**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb3e5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb3e5-123">Requirements</span></span>



| <span data-ttu-id="fb3e5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb3e5-124">Requirement</span></span> | <span data-ttu-id="fb3e5-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fb3e5-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb3e5-126">Versão</span><span class="sxs-lookup"><span data-stu-id="fb3e5-126">Version</span></span><br/> | <span data-ttu-id="fb3e5-127">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="fb3e5-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="fb3e5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="fb3e5-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb3e5-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb3e5-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb3e5-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb3e5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb3e5-131">**Objeto de configurações**</span><span class="sxs-lookup"><span data-stu-id="fb3e5-131">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="fb3e5-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="fb3e5-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





