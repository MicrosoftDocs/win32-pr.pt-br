---
title: Propriedade IWMPSettings2 mediaAccessRights
description: A propriedade mediaAccessRights Obtém um valor que indica as permissões concedidas atualmente para acesso à biblioteca.
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- Propriedade mediaAccessRights Windows Media Player
- Propriedade mediaAccessRights Windows Media Player, interface IWMPSettings2
- Interface IWMPSettings2 Windows Media Player, Propriedade mediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.mediaAccessRights
- IWMPSettings2.get_mediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cca06b9618767e7748b4b1308ed97860c7c80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768813"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a><span data-ttu-id="82e0a-106">Propriedade IWMPSettings2:: mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="82e0a-106">IWMPSettings2::mediaAccessRights property</span></span>

<span data-ttu-id="82e0a-107">A propriedade **mediaAccessRights** Obtém um valor que indica as permissões concedidas atualmente para acesso à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="82e0a-107">The **mediaAccessRights** property gets a value indicating the permissions currently granted for library access.</span></span>

<span data-ttu-id="82e0a-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="82e0a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="82e0a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82e0a-109">Syntax</span></span>


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a><span data-ttu-id="82e0a-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="82e0a-110">Property value</span></span>

<span data-ttu-id="82e0a-111">Um **System. String** que é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="82e0a-111">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="82e0a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="82e0a-112">Value</span></span> | <span data-ttu-id="82e0a-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="82e0a-113">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="82e0a-114">nenhum</span><span class="sxs-lookup"><span data-stu-id="82e0a-114">none</span></span>  | <span data-ttu-id="82e0a-115">Somente direitos de acesso do item atual.</span><span class="sxs-lookup"><span data-stu-id="82e0a-115">Current item access rights only.</span></span> |
| <span data-ttu-id="82e0a-116">ler</span><span class="sxs-lookup"><span data-stu-id="82e0a-116">read</span></span>  | <span data-ttu-id="82e0a-117">Somente direitos de acesso de leitura.</span><span class="sxs-lookup"><span data-stu-id="82e0a-117">Read access rights only.</span></span>         |
| <span data-ttu-id="82e0a-118">completa</span><span class="sxs-lookup"><span data-stu-id="82e0a-118">full</span></span>  | <span data-ttu-id="82e0a-119">Direitos de acesso de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="82e0a-119">Read/Write access rights.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="82e0a-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="82e0a-120">Remarks</span></span>

<span data-ttu-id="82e0a-121">Uma página da Web deve primeiro solicitar permissão do usuário para ler informações ou gravar dados na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="82e0a-121">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="82e0a-122">Isso significa que determinados métodos, propriedades e eventos ficarão inacessíveis a partir do código se os direitos de acesso apropriados não tiverem sido concedidos.</span><span class="sxs-lookup"><span data-stu-id="82e0a-122">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="82e0a-123">Para obter direitos de acesso, o aplicativo chama **IWMPSettings2. get \_ requestMediaAccessRights**, passando um parâmetro que especifica o nível de direitos de acesso desejado.</span><span class="sxs-lookup"><span data-stu-id="82e0a-123">To obtain access rights, the application calls **IWMPSettings2.get\_requestMediaAccessRights**, passing a parameter that specifies the desired access rights level.</span></span>

<span data-ttu-id="82e0a-124">Os aplicativos em execução no computador do usuário sempre têm direitos de acesso total.</span><span class="sxs-lookup"><span data-stu-id="82e0a-124">Applications running on the user's computer always have full access rights.</span></span>

## <a name="requirements"></a><span data-ttu-id="82e0a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82e0a-125">Requirements</span></span>



| <span data-ttu-id="82e0a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="82e0a-126">Requirement</span></span> | <span data-ttu-id="82e0a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="82e0a-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82e0a-128">Versão</span><span class="sxs-lookup"><span data-stu-id="82e0a-128">Version</span></span><br/>   | <span data-ttu-id="82e0a-129">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="82e0a-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="82e0a-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="82e0a-130">Namespace</span></span><br/> | <span data-ttu-id="82e0a-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="82e0a-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="82e0a-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="82e0a-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="82e0a-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="82e0a-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82e0a-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="82e0a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82e0a-135">**Interface IWMPSettings2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="82e0a-135">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="82e0a-136">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="82e0a-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





