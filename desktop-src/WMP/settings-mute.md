---
title: Configurações. mudo
description: A propriedade MUTE especifica e recupera um valor que indica se o áudio está mudo.
ms.assetid: d6d4b46d-5631-4af7-bd99-21674f067121
keywords:
- Configurações. ativar mudo do Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mute
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061439e9e091b2ad1cf6be49873d7e3895132b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786152"
---
# <a name="settingsmute"></a><span data-ttu-id="9d24d-104">Configurações. mudo</span><span class="sxs-lookup"><span data-stu-id="9d24d-104">Settings.mute</span></span>

<span data-ttu-id="9d24d-105">A propriedade **MUTE** especifica e recupera um valor que indica se o áudio está mudo.</span><span class="sxs-lookup"><span data-stu-id="9d24d-105">The **mute** property specifies and retrieves a value indicating whether audio is muted.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d24d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d24d-106">Syntax</span></span>

<span data-ttu-id="9d24d-107">Player. Settings. mudo</span><span class="sxs-lookup"><span data-stu-id="9d24d-107">player.settings.mute</span></span>

## <a name="possible-values"></a><span data-ttu-id="9d24d-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="9d24d-108">Possible Values</span></span>

<span data-ttu-id="9d24d-109">Esta propriedade é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9d24d-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="9d24d-110">Valor</span><span class="sxs-lookup"><span data-stu-id="9d24d-110">Value</span></span> | <span data-ttu-id="9d24d-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d24d-111">Description</span></span>                  |
|-------|------------------------------|
| <span data-ttu-id="9d24d-112">true</span><span class="sxs-lookup"><span data-stu-id="9d24d-112">true</span></span>  | <span data-ttu-id="9d24d-113">O áudio está mudo.</span><span class="sxs-lookup"><span data-stu-id="9d24d-113">Audio is muted.</span></span>              |
| <span data-ttu-id="9d24d-114">false</span><span class="sxs-lookup"><span data-stu-id="9d24d-114">false</span></span> | <span data-ttu-id="9d24d-115">Padrão.</span><span class="sxs-lookup"><span data-stu-id="9d24d-115">Default.</span></span> <span data-ttu-id="9d24d-116">O áudio não está mudo.</span><span class="sxs-lookup"><span data-stu-id="9d24d-116">Audio is not muted.</span></span> |



 

## <a name="examples"></a><span data-ttu-id="9d24d-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9d24d-117">Examples</span></span>

<span data-ttu-id="9d24d-118">O exemplo a seguir cria um elemento de caixa de seleção HTML que permite que o usuário ative mudo e mudo de áudio.</span><span class="sxs-lookup"><span data-stu-id="9d24d-118">The following example creates an HTML CHECKBOX element that allows the user to mute and un-mute audio.</span></span> <span data-ttu-id="9d24d-119">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9d24d-119">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX"  ID = MUTE  
             onClick = "
                        /* Use the CHECKBOX state to set 
                           the mute property. */
                        Player.settings.mute = MUTE.checked;
">
```



## <a name="requirements"></a><span data-ttu-id="9d24d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d24d-120">Requirements</span></span>



| <span data-ttu-id="9d24d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d24d-121">Requirement</span></span> | <span data-ttu-id="9d24d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9d24d-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9d24d-123">Versão</span><span class="sxs-lookup"><span data-stu-id="9d24d-123">Version</span></span><br/> | <span data-ttu-id="9d24d-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9d24d-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9d24d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9d24d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="9d24d-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d24d-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d24d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d24d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d24d-128">**Objeto de configurações**</span><span class="sxs-lookup"><span data-stu-id="9d24d-128">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





