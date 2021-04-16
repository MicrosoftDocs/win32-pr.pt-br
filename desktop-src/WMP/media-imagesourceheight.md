---
title: Media. imageSourceHeight
description: A propriedade ImageSourceHeight recupera a altura do item de mídia atual em pixels.
ms.assetid: fa98ec62-4c58-46ab-98f3-8017096d46d8
keywords:
- Media. imageSourceHeight Windows Media Player
topic_type:
- apiref
api_name:
- Media.imageSourceHeight
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de364243e71c6653085b4c9c9ff81f148dc299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794617"
---
# <a name="mediaimagesourceheight"></a><span data-ttu-id="947cb-104">Media. imageSourceHeight</span><span class="sxs-lookup"><span data-stu-id="947cb-104">Media.imageSourceHeight</span></span>

<span data-ttu-id="947cb-105">A propriedade **ImageSourceHeight** recupera a altura do item de mídia atual em pixels.</span><span class="sxs-lookup"><span data-stu-id="947cb-105">The **ImageSourceHeight** property retrieves the height of the current media item in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="947cb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="947cb-106">Syntax</span></span>

<span data-ttu-id="947cb-107">*Player*. *currentMedia*. **imageSourceHeight**</span><span class="sxs-lookup"><span data-stu-id="947cb-107">*player*.*currentMedia*.**imageSourceHeight**</span></span>

## <a name="possible-values"></a><span data-ttu-id="947cb-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="947cb-108">Possible Values</span></span>

<span data-ttu-id="947cb-109">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="947cb-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="947cb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="947cb-110">Remarks</span></span>

<span data-ttu-id="947cb-111">Se o item de mídia não for o atual, essa propriedade retornará zero.</span><span class="sxs-lookup"><span data-stu-id="947cb-111">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="947cb-112">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="947cb-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="947cb-113">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="947cb-113">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="947cb-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="947cb-114">Examples</span></span>

<span data-ttu-id="947cb-115">O exemplo de JScript a seguir usa *Media*. imageSourceHeight para exibir o tamanho da imagem, em pixels, do item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="947cb-115">The following JScript example uses *Media*.imageSourceHeight to display the image size, in pixels, of the current media item.</span></span> <span data-ttu-id="947cb-116">As informações são impressas em um elemento HTML TEXTAREA chamado vídeos.</span><span class="sxs-lookup"><span data-stu-id="947cb-116">The information is printed to an HTML TEXTAREA element named VideoSize.</span></span> <span data-ttu-id="947cb-117">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="947cb-117">The **Player** object was created with ID = "player".</span></span>


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Store the height and width of the new media item.
   var Height = Player.currentMedia.imageSourceHeight;
   var Width =  Player.currentMedia.imageSourceWidth;

   // Erase the information in the text area.
   VideoSize.value = "";

   // Test whether an image is visible.
   if (Height != 0 && Width != 0)

      // Display the image size information.
      VideoSize.value = Width + " x " + Height;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="947cb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="947cb-118">Requirements</span></span>



| <span data-ttu-id="947cb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="947cb-119">Requirement</span></span> | <span data-ttu-id="947cb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="947cb-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="947cb-121">Versão</span><span class="sxs-lookup"><span data-stu-id="947cb-121">Version</span></span><br/> | <span data-ttu-id="947cb-122">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="947cb-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="947cb-123">DLL</span><span class="sxs-lookup"><span data-stu-id="947cb-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="947cb-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="947cb-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="947cb-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="947cb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="947cb-126">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="947cb-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="947cb-127">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="947cb-127">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="947cb-128">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="947cb-128">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="947cb-129">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="947cb-129">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





