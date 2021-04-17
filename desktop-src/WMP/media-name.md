---
title: Media.name
description: A propriedade Name especifica ou recupera o nome do item de mídia.
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Media.name Windows Media Player
topic_type:
- apiref
api_name:
- Media.name
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de8095d88c3ddec9049e0b43461adcf5553ec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763841"
---
# <a name="medianame"></a><span data-ttu-id="f9469-104">Media.name</span><span class="sxs-lookup"><span data-stu-id="f9469-104">Media.name</span></span>

<span data-ttu-id="f9469-105">A propriedade **Name** especifica ou recupera o nome do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="f9469-105">The **name** property specifies or retrieves the name of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9469-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9469-106">Syntax</span></span>

<span data-ttu-id="f9469-107">*Player*. *currentMedia*. **nome** do</span><span class="sxs-lookup"><span data-stu-id="f9469-107">*player*.*currentMedia*.**name**</span></span>

## <a name="possible-values"></a><span data-ttu-id="f9469-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="f9469-108">Possible Values</span></span>

<span data-ttu-id="f9469-109">Essa propriedade é uma **cadeia de caracteres** de leitura/gravação que contém o nome do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="f9469-109">This property is a read/write **String** containing the name of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9469-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9469-110">Remarks</span></span>

<span data-ttu-id="f9469-111">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f9469-111">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="f9469-112">Para especificar o valor dessa propriedade, é necessário ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f9469-112">To specify the value of this property, full access to the library is required.</span></span> <span data-ttu-id="f9469-113">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f9469-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="f9469-114">Antes de usar esse método para especificar o nome de um item de mídia, use **isReadOnlyItem** para determinar se o nome pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="f9469-114">Before using this method to specify the name of a media item, use **isReadOnlyItem** to determine whether the name can be set.</span></span>

<span data-ttu-id="f9469-115">**Windows Media Player 10 Mobile:** Esta propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f9469-115">**Windows Media Player 10 Mobile:** This property is read-only.</span></span>

## <a name="examples"></a><span data-ttu-id="f9469-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9469-116">Examples</span></span>

<span data-ttu-id="f9469-117">O exemplo de JScript a seguir usa *mídia*. **nome** para alterar o nome do item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="f9469-117">The following JScript example uses *Media*.**name** to change the name of the current media item.</span></span> <span data-ttu-id="f9469-118">Um elemento de entrada de texto HTML chamado NameText permite que o usuário insira uma cadeia de texto para o novo nome.</span><span class="sxs-lookup"><span data-stu-id="f9469-118">An HTML TEXT input element named NameText allows the user to enter a text string for the new name.</span></span> <span data-ttu-id="f9469-119">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f9469-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!<entity type="mdash"/>-Create an HTML BUTTON element to execute the name change. -->
<INPUT type = "BUTTON"  id = "NewName"  name = "NewName"  value = "Change Name" 
    onClick = "

        /* Store the current media item. */
        var cm = Player.currentMedia;

        /* Change the name. */
        cm.name = NameText.value;
">

```



## <a name="requirements"></a><span data-ttu-id="f9469-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9469-120">Requirements</span></span>



| <span data-ttu-id="f9469-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9469-121">Requirement</span></span> | <span data-ttu-id="f9469-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f9469-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f9469-123">Versão</span><span class="sxs-lookup"><span data-stu-id="f9469-123">Version</span></span><br/> | <span data-ttu-id="f9469-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f9469-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f9469-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f9469-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="f9469-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9469-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9469-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9469-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9469-128">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="f9469-128">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="f9469-129">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f9469-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="f9469-130">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f9469-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





