---
title: Método Settings. requestMediaAccessRights
description: O método requestMediaAccessRights solicita um nível especificado de acesso à biblioteca. | Método Settings. requestMediaAccessRights
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- método requestMediaAccessRights Windows Media Player
- método requestMediaAccessRights Windows Media Player, classe Settings
- Classe de configurações Windows Media Player, método requestMediaAccessRights
topic_type:
- apiref
api_name:
- Settings.requestMediaAccessRights
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfeed45666ee1f63bf995b211030b0b840c4279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747496"
---
# <a name="settingsrequestmediaaccessrights-method"></a><span data-ttu-id="2554b-107">Método Settings. requestMediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="2554b-107">Settings.requestMediaAccessRights method</span></span>

<span data-ttu-id="2554b-108">O método **requestMediaAccessRights** solicita um nível especificado de acesso à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2554b-108">The **requestMediaAccessRights** method requests a specified level of access to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="2554b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2554b-109">Syntax</span></span>


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a><span data-ttu-id="2554b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2554b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2554b-111">*acesso* \[ ao no\]</span><span class="sxs-lookup"><span data-stu-id="2554b-111">*access* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2554b-112">**Cadeia de caracteres** que especifica o nível de direitos de acesso desejado.</span><span class="sxs-lookup"><span data-stu-id="2554b-112">**String** specifying the desired access rights level.</span></span> <span data-ttu-id="2554b-113">Contém um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="2554b-113">Contains one of the following values.</span></span>



| <span data-ttu-id="2554b-114">String</span><span class="sxs-lookup"><span data-stu-id="2554b-114">String</span></span> | <span data-ttu-id="2554b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="2554b-115">Description</span></span>                      |
|--------|----------------------------------|
| <span data-ttu-id="2554b-116">none</span><span class="sxs-lookup"><span data-stu-id="2554b-116">none</span></span>   | <span data-ttu-id="2554b-117">Somente direitos de acesso do item atual.</span><span class="sxs-lookup"><span data-stu-id="2554b-117">Current item access rights only.</span></span> |
| <span data-ttu-id="2554b-118">ler</span><span class="sxs-lookup"><span data-stu-id="2554b-118">read</span></span>   | <span data-ttu-id="2554b-119">Somente direitos de acesso de leitura.</span><span class="sxs-lookup"><span data-stu-id="2554b-119">Read access rights only.</span></span>         |
| <span data-ttu-id="2554b-120">completa</span><span class="sxs-lookup"><span data-stu-id="2554b-120">full</span></span>   | <span data-ttu-id="2554b-121">Direitos de acesso de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2554b-121">Read/Write access rights.</span></span>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2554b-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2554b-122">Return value</span></span>

<span data-ttu-id="2554b-123">Esse método retorna um valor **booliano** que indica se os direitos de acesso solicitados foram concedidos.</span><span class="sxs-lookup"><span data-stu-id="2554b-123">This method returns a **Boolean** value indicating whether the requested access rights were granted.</span></span>

## <a name="remarks"></a><span data-ttu-id="2554b-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="2554b-124">Remarks</span></span>

<span data-ttu-id="2554b-125">Uma página da Web deve primeiro solicitar permissão do usuário para ler informações ou gravar dados na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2554b-125">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="2554b-126">Invocar esse método solicita ao usuário uma caixa de diálogo que solicita o nível de permissão especificado.</span><span class="sxs-lookup"><span data-stu-id="2554b-126">Invoking this method prompts the user with a dialog box that requests the specified permission level.</span></span> <span data-ttu-id="2554b-127">Isso significa que determinados métodos, propriedades e eventos ficarão inacessíveis a partir do código se os direitos de acesso apropriados não tiverem sido concedidos.</span><span class="sxs-lookup"><span data-stu-id="2554b-127">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="2554b-128">O nível de direitos de acesso atual pode ser recuperado usando *as configurações*. **mediaAccessRights**.</span><span class="sxs-lookup"><span data-stu-id="2554b-128">The current access rights level can be retrieved using *Settings*.**mediaAccessRights**.</span></span>

<span data-ttu-id="2554b-129">**Windows Media Player 10 Mobile**: esse método sempre retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="2554b-129">**Windows Media Player 10 Mobile**: This method always returns **true**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2554b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2554b-130">Requirements</span></span>



| <span data-ttu-id="2554b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2554b-131">Requirement</span></span> | <span data-ttu-id="2554b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="2554b-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2554b-133">Versão</span><span class="sxs-lookup"><span data-stu-id="2554b-133">Version</span></span><br/> | <span data-ttu-id="2554b-134">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2554b-134">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="2554b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2554b-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="2554b-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2554b-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2554b-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="2554b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2554b-138">**Objeto de configurações**</span><span class="sxs-lookup"><span data-stu-id="2554b-138">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="2554b-139">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2554b-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> </dl>

 

 





