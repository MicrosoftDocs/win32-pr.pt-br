---
title: Cdrom. driveSpecifier
description: A propriedade driveSpecifier recupera a letra da unidade de CD ou DVD.
ms.assetid: f592819e-61ba-4ae1-b748-b6f29df88067
keywords:
- Cdrom. driveSpecifier Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom.driveSpecifier
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fef04f56de87bb6aeb4843e5aedb6e5ed74418a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499289"
---
# <a name="cdromdrivespecifier"></a><span data-ttu-id="dbfd4-104">Cdrom. driveSpecifier</span><span class="sxs-lookup"><span data-stu-id="dbfd4-104">Cdrom.driveSpecifier</span></span>

<span data-ttu-id="dbfd4-105">A propriedade **driveSpecifier** recupera a letra da unidade de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="dbfd4-105">The **driveSpecifier** property retrieves the CD or DVD drive letter.</span></span>

``` syntax
player.cdromCollection.item(
        index
        ).driveSpecifier
      
```

## <a name="possible-values"></a><span data-ttu-id="dbfd4-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="dbfd4-106">Possible Values</span></span>

<span data-ttu-id="dbfd4-107">Esta propriedade é uma **cadeia de caracteres** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="dbfd4-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbfd4-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbfd4-108">Remarks</span></span>

<span data-ttu-id="dbfd4-109">Normalmente, as unidades de DVD podem reproduzir mídia de CD, mas as unidades de CD não podem reproduzir mídias em DVD.</span><span class="sxs-lookup"><span data-stu-id="dbfd4-109">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span> <span data-ttu-id="dbfd4-110">Essa propriedade recupera um especificador de unidade para um índice de unidade com base em zero dentro do intervalo recuperado usando *cdromCollection*. **contagem**.</span><span class="sxs-lookup"><span data-stu-id="dbfd4-110">This property retrieves a drive specifier for a zero-based drive index within the range retrieved using *CdromCollection*.**count**.</span></span> <span data-ttu-id="dbfd4-111">O valor recuperado assume a forma *X*:, em que *X* representa a letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="dbfd4-111">The value retrieved takes the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="dbfd4-112">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="dbfd4-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="dbfd4-113">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="dbfd4-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="dbfd4-114">**Windows Media Player 10 Mobile:** Não há suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="dbfd4-114">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="dbfd4-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dbfd4-115">Examples</span></span>

<span data-ttu-id="dbfd4-116">O exemplo de JScript a seguir usa *cdrom*. **driveSpecifier** para preencher uma área de texto HTML chamada MyText com uma lista separada por vírgulas de unidades de CD e DVD disponíveis.</span><span class="sxs-lookup"><span data-stu-id="dbfd4-116">The following JScript example uses *Cdrom*.**driveSpecifier** to fill an HTML text area named myText with a comma-separated list of available CD and DVD drives.</span></span> <span data-ttu-id="dbfd4-117">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="dbfd4-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Allocate an array to store the drive specifiers.
var MYdriveSpecifiers = new Array();

// Loop through the available drives using CdromCollection.count.
for (var i = 0; i < Player.cdRomCollection.count; i++){

// For each available drive, add a corresponding item 
// to the MYdriveSpecifiers array. 
    MYdriveSpecifiers[i] = Player.CDRomCollection.item(i).driveSpecifier;
}

// Write the array of drive letter specifiers to the text area.
myText.value = "Drive letters found: " + MYdriveSpecifiers;
```



## <a name="requirements"></a><span data-ttu-id="dbfd4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbfd4-118">Requirements</span></span>



| <span data-ttu-id="dbfd4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbfd4-119">Requirement</span></span> | <span data-ttu-id="dbfd4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="dbfd4-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dbfd4-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbfd4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dbfd4-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dbfd4-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dbfd4-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbfd4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dbfd4-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dbfd4-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dbfd4-125">Versão</span><span class="sxs-lookup"><span data-stu-id="dbfd4-125">Version</span></span><br/>                  | <span data-ttu-id="dbfd4-126">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="dbfd4-126">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="dbfd4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="dbfd4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbfd4-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbfd4-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbfd4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbfd4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbfd4-130">**Objeto cdrom**</span><span class="sxs-lookup"><span data-stu-id="dbfd4-130">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="dbfd4-131">**CdromCollection. contagem**</span><span class="sxs-lookup"><span data-stu-id="dbfd4-131">**CdromCollection.count**</span></span>](cdromcollection-count.md)
</dt> <dt>

[<span data-ttu-id="dbfd4-132">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="dbfd4-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="dbfd4-133">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="dbfd4-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





