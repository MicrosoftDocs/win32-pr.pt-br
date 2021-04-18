---
title: CdromCollection. contagem
description: A propriedade Count recupera o número de unidades de CD e DVD disponíveis no sistema.
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- CdromCollection. contagem do Windows Media Player
topic_type:
- apiref
api_name:
- CdromCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf7150ca31caaf68fa51ae42fded223d24a8e59f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760275"
---
# <a name="cdromcollectioncount"></a><span data-ttu-id="5ad1d-104">CdromCollection. contagem</span><span class="sxs-lookup"><span data-stu-id="5ad1d-104">CdromCollection.count</span></span>

<span data-ttu-id="5ad1d-105">A propriedade **Count** recupera o número de unidades de CD e DVD disponíveis no sistema.</span><span class="sxs-lookup"><span data-stu-id="5ad1d-105">The **count** property retrieves the number of available CD and DVD drives on the system.</span></span>

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a><span data-ttu-id="5ad1d-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5ad1d-106">Possible Values</span></span>

<span data-ttu-id="5ad1d-107">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="5ad1d-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="5ad1d-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ad1d-108">Remarks</span></span>

<span data-ttu-id="5ad1d-109">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5ad1d-109">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="5ad1d-110">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5ad1d-110">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="5ad1d-111">As unidades de DVD-ROM são contadas exatamente como unidades de CD.</span><span class="sxs-lookup"><span data-stu-id="5ad1d-111">DVD-ROM drives are counted exactly like CD drives.</span></span> <span data-ttu-id="5ad1d-112">No entanto, o controle do Windows Media Player só dá suporte à funcionalidade de DVD para sistemas operacionais Windows XP ou posteriores.</span><span class="sxs-lookup"><span data-stu-id="5ad1d-112">However, the Windows Media Player control only supports DVD functionality for Windows XP or later operating systems.</span></span> <span data-ttu-id="5ad1d-113">Normalmente, as unidades de DVD podem reproduzir mídia de CD, mas as unidades de CD não podem reproduzir mídias em DVD.</span><span class="sxs-lookup"><span data-stu-id="5ad1d-113">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

<span data-ttu-id="5ad1d-114">**Windows Media Player 10 Mobile:** Esse método sempre retorna 0.</span><span class="sxs-lookup"><span data-stu-id="5ad1d-114">**Windows Media Player 10 Mobile:** This method always returns 0.</span></span>

## <a name="examples"></a><span data-ttu-id="5ad1d-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5ad1d-115">Examples</span></span>

<span data-ttu-id="5ad1d-116">O exemplo de JScript a seguir usa *cdromCollection*. **contagem** para exibir o número de unidades de CD e DVD disponíveis no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="5ad1d-116">The following JScript example uses *CdromCollection*.**count** to display the number of CD and DVD drives available on the user's computer.</span></span> <span data-ttu-id="5ad1d-117">O objeto de jogador foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5ad1d-117">The player object was created with ID = "Player".</span></span>


```JScript
// Store the count of drives found on the computer.
var numCDROMS = Player.cdromCollection.count;

// Build the string to display to the user.
var displayString = numCDROMS + " drive(s) found.";

// Show a message box with the count information.
alert(displayString);
```



## <a name="requirements"></a><span data-ttu-id="5ad1d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ad1d-118">Requirements</span></span>



| <span data-ttu-id="5ad1d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ad1d-119">Requirement</span></span> | <span data-ttu-id="5ad1d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5ad1d-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad1d-121">Versão</span><span class="sxs-lookup"><span data-stu-id="5ad1d-121">Version</span></span><br/> | <span data-ttu-id="5ad1d-122">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5ad1d-122">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="5ad1d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5ad1d-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="5ad1d-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ad1d-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ad1d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ad1d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ad1d-126">**Objeto cdromCollection**</span><span class="sxs-lookup"><span data-stu-id="5ad1d-126">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="5ad1d-127">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5ad1d-127">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5ad1d-128">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5ad1d-128">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





