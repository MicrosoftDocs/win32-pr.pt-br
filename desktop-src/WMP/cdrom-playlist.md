---
title: Cdrom. playlist
description: A propriedade playlist recupera um objeto playlist que representa as faixas no CD atualmente na unidade de CD ou as entradas de título no nível raiz do DVD.
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- Cdrom. playlist Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom.playlist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcdb50daa169c6f6eb0690de376abd4433ffe130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105783624"
---
# <a name="cdromplaylist"></a><span data-ttu-id="87baa-104">Cdrom. playlist</span><span class="sxs-lookup"><span data-stu-id="87baa-104">Cdrom.playlist</span></span>

<span data-ttu-id="87baa-105">A propriedade **playlist** recupera um objeto **playlist** que representa as faixas no CD atualmente na unidade de CD ou as entradas de título no nível raiz do DVD.</span><span class="sxs-lookup"><span data-stu-id="87baa-105">The **playlist** property retrieves a **Playlist** object representing the tracks on the CD currently in the CD drive or the root-level title entries for DVD.</span></span>

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a><span data-ttu-id="87baa-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="87baa-106">Possible Values</span></span>

<span data-ttu-id="87baa-107">Esta propriedade é um objeto de **lista de reprodução** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="87baa-107">This property is a read-only **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="87baa-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="87baa-108">Remarks</span></span>

<span data-ttu-id="87baa-109">Normalmente, os DVDs são organizados em títulos.</span><span class="sxs-lookup"><span data-stu-id="87baa-109">Typically, DVDs are organized into titles.</span></span> <span data-ttu-id="87baa-110">Cada título contém um ou mais capítulos.</span><span class="sxs-lookup"><span data-stu-id="87baa-110">Each title contains one or more chapters.</span></span> <span data-ttu-id="87baa-111">Cada DVD é criado de forma diferente, portanto, como os títulos e capítulos são usados, cabe ao autor do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="87baa-111">Each DVD is authored differently, so how titles and chapters are used is up to the content author.</span></span>

<span data-ttu-id="87baa-112">Para DVD, esse método recupera uma lista de reprodução que contém como o primeiro item um objeto de **mídia** que representa a mídia de DVD.</span><span class="sxs-lookup"><span data-stu-id="87baa-112">For DVD, this method retrieves a playlist that contains as the first item a **Media** object that represents the DVD media.</span></span> <span data-ttu-id="87baa-113">A reprodução dos resultados do item no DVD será reproduzida desde o início se for a primeira reprodução após a inserção de um novo DVD ou a retomada da reprodução se o DVD for o mesmo que o último DVD exibido.</span><span class="sxs-lookup"><span data-stu-id="87baa-113">Playing the item results in the DVD playing from the beginning if it is the first play after inserting a new DVD, or resuming playback if the DVD is the same as the last DVD viewed.</span></span> <span data-ttu-id="87baa-114">Definir esse item como o atual durante os resultados da reprodução no DVD é reproduzido desde o início.</span><span class="sxs-lookup"><span data-stu-id="87baa-114">Setting this item as the current one during playback results in the DVD playing from the beginning.</span></span>

<span data-ttu-id="87baa-115">Itens adicionais (objetos de **mídia** ) na playlist são títulos de DVD que são representados por listas de reprodução aninhadas.</span><span class="sxs-lookup"><span data-stu-id="87baa-115">Additional items (**Media** objects) in the playlist are DVD titles that are represented by nested playlists.</span></span> <span data-ttu-id="87baa-116">Quando você especifica *controles*. **currentItem** para igual a um desses itens aninhados da lista de reprodução, o Windows Media Player define automaticamente a lista de reprodução aninhada como *Player*. **currentPlaylist** após a reprodução do capítulo começar.</span><span class="sxs-lookup"><span data-stu-id="87baa-116">When you specify *Controls*.**currentItem** to equal one of these nested playlist items, Windows Media Player automatically sets the nested playlist as *Player*.**currentPlaylist** after chapter playback begins.</span></span> <span data-ttu-id="87baa-117">Você pode usar as propriedades, métodos e eventos do objeto **currentPlaylist** para trabalhar com capítulos de DVD, que também são itens de playlist.</span><span class="sxs-lookup"><span data-stu-id="87baa-117">You can then use the **currentPlaylist** object properties, methods, and events to work with DVD chapters, which are also playlist items.</span></span>

<span data-ttu-id="87baa-118">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="87baa-118">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="87baa-119">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="87baa-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="87baa-120">**Windows Media Player 10 Mobile:** Não há suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="87baa-120">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="87baa-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="87baa-121">Examples</span></span>

<span data-ttu-id="87baa-122">O exemplo a seguir usa *cdrom*. **lista de reprodução** para preencher um elemento de texto HTML, chamado mytext, com os títulos do CD de áudio atualmente na primeira unidade de CD.</span><span class="sxs-lookup"><span data-stu-id="87baa-122">The following example uses *Cdrom*.**playlist** to fill an HTML text element, named myText, with the titles of the audio CD currently in the first CD drive.</span></span> <span data-ttu-id="87baa-123">Use *cdromCollection*. **contagem** para determinar o número de unidades de CD disponíveis.</span><span class="sxs-lookup"><span data-stu-id="87baa-123">Use *CdromCollection*.**count** to determine the number of available CD drives.</span></span> <span data-ttu-id="87baa-124">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="87baa-124">The **Player** object was created with ID = "Player".</span></span>


```
// Store the CD playlist object.
var pl = Player.cdromCollection.Item(0).Playlist;

// Iterate through the CD track list.
for(var i = 0; i < pl.count; i++){

   // Print each CD track name.
   myText.value += pl.Item(i).name + "\n"; 
}
```



## <a name="requirements"></a><span data-ttu-id="87baa-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87baa-125">Requirements</span></span>



| <span data-ttu-id="87baa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="87baa-126">Requirement</span></span> | <span data-ttu-id="87baa-127">Valor</span><span class="sxs-lookup"><span data-stu-id="87baa-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="87baa-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87baa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="87baa-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="87baa-129">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87baa-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87baa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="87baa-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="87baa-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="87baa-132">Versão</span><span class="sxs-lookup"><span data-stu-id="87baa-132">Version</span></span><br/>                  | <span data-ttu-id="87baa-133">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="87baa-133">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="87baa-134">DLL</span><span class="sxs-lookup"><span data-stu-id="87baa-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87baa-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87baa-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87baa-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="87baa-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87baa-137">**Objeto cdrom**</span><span class="sxs-lookup"><span data-stu-id="87baa-137">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="87baa-138">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="87baa-138">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="87baa-139">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="87baa-139">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





