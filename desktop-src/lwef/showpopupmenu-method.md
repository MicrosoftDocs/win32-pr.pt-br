---
title: Método ShowPopupMenu
description: Método ShowPopupMenu
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0325a552cc3c1f91a64c1240964f1d0c329292c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813639"
---
# <a name="showpopupmenu-method"></a><span data-ttu-id="7a0b8-103">Método ShowPopupMenu</span><span class="sxs-lookup"><span data-stu-id="7a0b8-103">ShowPopupMenu Method</span></span>

<span data-ttu-id="7a0b8-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7a0b8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="7a0b8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="7a0b8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="7a0b8-106">Exibe o menu pop-up do caractere no local especificado.</span><span class="sxs-lookup"><span data-stu-id="7a0b8-106">Displays the character's pop-up menu at the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="7a0b8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="7a0b8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="7a0b8-108">*Agente. ***Caracteres ("*** characterid ***"). ShowPopupMenu*** x, y*</span><span class="sxs-lookup"><span data-stu-id="7a0b8-108">*agent.\*\*\*Characters("*\*\* CharacterID ***").ShowPopupMenu*** x, y\*</span></span>



| <span data-ttu-id="7a0b8-109">Parte</span><span class="sxs-lookup"><span data-stu-id="7a0b8-109">Part</span></span> | <span data-ttu-id="7a0b8-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7a0b8-110">Description</span></span>                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a0b8-111">*x*</span><span class="sxs-lookup"><span data-stu-id="7a0b8-111">*x*</span></span>  | <span data-ttu-id="7a0b8-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="7a0b8-112">Required.</span></span> <span data-ttu-id="7a0b8-113">Um valor inteiro que indica a coordenada de tela horizontal (*x*) para exibir o menu.</span><span class="sxs-lookup"><span data-stu-id="7a0b8-113">An integer value that indicates the horizontal (*x*) screen coordinate to display the menu.</span></span> <span data-ttu-id="7a0b8-114">Essas coordenadas devem ser especificadas em pixels.</span><span class="sxs-lookup"><span data-stu-id="7a0b8-114">These coordinates must be specified in pixels.</span></span> |
| <span data-ttu-id="7a0b8-115">*y*</span><span class="sxs-lookup"><span data-stu-id="7a0b8-115">*y*</span></span>  | <span data-ttu-id="7a0b8-116">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="7a0b8-116">Required.</span></span> <span data-ttu-id="7a0b8-117">Um valor inteiro que indica a coordenada de tela vertical (*y*) para exibir o menu.</span><span class="sxs-lookup"><span data-stu-id="7a0b8-117">An integer value that indicates the vertical (*y*) screen coordinate to display the menu.</span></span> <span data-ttu-id="7a0b8-118">Essas coordenadas devem ser especificadas em pixels.</span><span class="sxs-lookup"><span data-stu-id="7a0b8-118">These coordinates must be specified in pixels.</span></span>   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a0b8-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a0b8-119">Remarks</span></span>

<span data-ttu-id="7a0b8-120">O Agent exibe automaticamente o menu pop-up do caractere quando o usuário clica com o botão direito do mouse no caractere.</span><span class="sxs-lookup"><span data-stu-id="7a0b8-120">Agent automatically displays the character's pop-up menu when the user right-clicks the character.</span></span> <span data-ttu-id="7a0b8-121">Se você definir [**AutoPopupMenu**](autopopupmenu-property.md) como **false**, poderá usar esse método para exibir o menu.</span><span class="sxs-lookup"><span data-stu-id="7a0b8-121">If you set [**AutoPopupMenu**](autopopupmenu-property.md) to **False**, you can use this method to display the menu.</span></span>

<span data-ttu-id="7a0b8-122">O menu permanece exibido até que o usuário selecione um comando ou exiba outro menu.</span><span class="sxs-lookup"><span data-stu-id="7a0b8-122">The menu remains displayed until the user selects a command or displays another menu.</span></span> <span data-ttu-id="7a0b8-123">Somente um menu pop-up pode ser exibido de cada vez; Portanto, as chamadas para esse método irão cancelar (remover) o menu anterior.</span><span class="sxs-lookup"><span data-stu-id="7a0b8-123">Only one pop-up menu can be displayed at a time; therefore, calls to this method will cancel (remove) the former menu.</span></span>

<span data-ttu-id="7a0b8-124">Esse método deve ser chamado somente quando o aplicativo cliente é o cliente ativo do caractere; caso contrário, ele falhará.</span><span class="sxs-lookup"><span data-stu-id="7a0b8-124">This method should be called only when your client application is the active client of the character; otherwise it fails.</span></span> <span data-ttu-id="7a0b8-125">Para determinar o sucesso desse método, você pode chamá-lo como uma função e ele retornará um valor booliano indicando se o método teve êxito.</span><span class="sxs-lookup"><span data-stu-id="7a0b8-125">To determine the success of this method you can call it as a function and it will return a Boolean value indicating whether the method succeeded.</span></span>


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a><span data-ttu-id="7a0b8-126">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7a0b8-126">See Also</span></span>

[<span data-ttu-id="7a0b8-127">**Propriedade AutoPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="7a0b8-127">**AutoPopupMenu property**</span></span>](autopopupmenu-property.md)


 

 




