---
title: Método cdrom. EJECT
description: O método EJECT ejeta o CD ou DVD da unidade. | Método cdrom. EJECT
ms.assetid: f43c7f10-7de2-488c-833a-ecd3ac21744b
keywords:
- método de ejeção do Windows Media Player
- método de ejeção Windows Media Player, classe cdrom
- Classe de cdrom Windows Media Player, método de ejeção
topic_type:
- apiref
api_name:
- Cdrom.eject
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78326ca57dcf097344fc073681fae772222ea9ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105788184"
---
# <a name="cdromeject-method"></a><span data-ttu-id="bb061-107">Método cdrom. EJECT</span><span class="sxs-lookup"><span data-stu-id="bb061-107">Cdrom.eject method</span></span>

<span data-ttu-id="bb061-108">O método **EJECT** ejeta o CD ou DVD da unidade.</span><span class="sxs-lookup"><span data-stu-id="bb061-108">The **eject** method ejects the CD or DVD from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb061-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb061-109">Syntax</span></span>


```JScript
Cdrom.eject()
```



## <a name="parameters"></a><span data-ttu-id="bb061-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb061-110">Parameters</span></span>

<span data-ttu-id="bb061-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bb061-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bb061-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb061-112">Return value</span></span>

<span data-ttu-id="bb061-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bb061-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb061-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb061-114">Remarks</span></span>

<span data-ttu-id="bb061-115">Se a porta da unidade estiver aberta, esse método fechará a porta.</span><span class="sxs-lookup"><span data-stu-id="bb061-115">If the drive door is open, this method closes the door.</span></span>

<span data-ttu-id="bb061-116">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="bb061-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="bb061-117">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="bb061-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="bb061-118">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="bb061-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="bb061-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bb061-119">Examples</span></span>

<span data-ttu-id="bb061-120">O exemplo a seguir cria um elemento de botão HTML que usa *cdrom*. **ejete** para abrir a porta da unidade que tem o índice de especificador de unidade zero.</span><span class="sxs-lookup"><span data-stu-id="bb061-120">The following example creates an HTML button element that uses *Cdrom*.**eject** to open the door of the drive that has drive specifier index zero.</span></span> <span data-ttu-id="bb061-121">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="bb061-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"
       NAME = "EJECTBUTTON"
       VALUE = "EJECT"
       OnClick =  "Player.cdromCollection.item(0).eject()"
>
```



## <a name="requirements"></a><span data-ttu-id="bb061-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb061-122">Requirements</span></span>



| <span data-ttu-id="bb061-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb061-123">Requirement</span></span> | <span data-ttu-id="bb061-124">Valor</span><span class="sxs-lookup"><span data-stu-id="bb061-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb061-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb061-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bb061-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bb061-126">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb061-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb061-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bb061-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bb061-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bb061-129">Versão</span><span class="sxs-lookup"><span data-stu-id="bb061-129">Version</span></span><br/>                  | <span data-ttu-id="bb061-130">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="bb061-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="bb061-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bb061-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb061-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb061-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb061-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb061-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb061-134">**Objeto cdrom**</span><span class="sxs-lookup"><span data-stu-id="bb061-134">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="bb061-135">**Player. PlayState**</span><span class="sxs-lookup"><span data-stu-id="bb061-135">**Player.playState**</span></span>](player-playstate.md)
</dt> <dt>

[<span data-ttu-id="bb061-136">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="bb061-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="bb061-137">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="bb061-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





