---
title: Media. imageSourceWidth
description: A propriedade imageSourceWidth recupera a largura do item de mídia atual em pixels.
ms.assetid: 6559bd51-cec2-4fc6-aab8-f2fdd1d59bae
keywords:
- Media. imageSourceWidth Windows Media Player
topic_type:
- apiref
api_name:
- Media.imageSourceWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2a3fef7b74a3d033b058f0afd1f6eece007bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783740"
---
# <a name="mediaimagesourcewidth"></a><span data-ttu-id="d4715-104">Media. imageSourceWidth</span><span class="sxs-lookup"><span data-stu-id="d4715-104">Media.imageSourceWidth</span></span>

<span data-ttu-id="d4715-105">A propriedade **imageSourceWidth** recupera a largura do item de mídia atual em pixels.</span><span class="sxs-lookup"><span data-stu-id="d4715-105">The **imageSourceWidth** property retrieves the width of the current media item in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4715-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4715-106">Syntax</span></span>

<span data-ttu-id="d4715-107">*Player*. *currentMedia*. **imageSourceWidth**</span><span class="sxs-lookup"><span data-stu-id="d4715-107">*player*.*currentMedia*.**imageSourceWidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="d4715-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="d4715-108">Possible Values</span></span>

<span data-ttu-id="d4715-109">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="d4715-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4715-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4715-110">Remarks</span></span>

<span data-ttu-id="d4715-111">Se o item de mídia não for o atual, essa propriedade retornará zero.</span><span class="sxs-lookup"><span data-stu-id="d4715-111">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="d4715-112">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d4715-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="d4715-113">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d4715-113">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d4715-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d4715-114">Examples</span></span>

<span data-ttu-id="d4715-115">O exemplo de JScript a seguir usa *mídia*. **imageSourceWidth** para exibir o tamanho da imagem, em pixels, do **item de mídia atual. As informações são impressas em um elemento HTML TEXTAREA chamado vídeos. O objeto de jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d4715-115">The following JScript example uses *Media*.**imageSourceWidth** to display the image size, in pixels, of the **current media item. The information is printed to an HTML TEXTAREA element named VideoSize. The Player** object was created with ID = "player".</span></span>


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player"  EVENT = OpenStateChange(NewState)>

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



## <a name="requirements"></a><span data-ttu-id="d4715-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4715-116">Requirements</span></span>



| <span data-ttu-id="d4715-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4715-117">Requirement</span></span> | <span data-ttu-id="d4715-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d4715-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4715-119">Versão</span><span class="sxs-lookup"><span data-stu-id="d4715-119">Version</span></span><br/> | <span data-ttu-id="d4715-120">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d4715-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d4715-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d4715-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="d4715-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4715-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4715-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4715-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4715-124">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="d4715-124">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="d4715-125">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="d4715-125">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="d4715-126">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d4715-126">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="d4715-127">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d4715-127">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





