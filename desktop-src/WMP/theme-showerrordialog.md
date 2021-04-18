---
title: THEME. showErrorDialog
description: O método showErrorDialog exibe a caixa de diálogo de erro padrão.
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- THEME. showErrorDialog Windows Media Player
topic_type:
- apiref
api_name:
- THEME.showErrorDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdc1f9df13ec460ce780507e1bde38a2996f915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813022"
---
# <a name="themeshowerrordialog"></a><span data-ttu-id="85c2a-104">THEME. showErrorDialog</span><span class="sxs-lookup"><span data-stu-id="85c2a-104">THEME.showErrorDialog</span></span>

<span data-ttu-id="85c2a-105">O método **showErrorDialog** exibe a caixa de diálogo de erro padrão.</span><span class="sxs-lookup"><span data-stu-id="85c2a-105">The **showErrorDialog** method displays the standard error dialog box.</span></span>

``` syntax
        theme.showErrorDialog()
```

## <a name="parameters"></a><span data-ttu-id="85c2a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85c2a-106">Parameters</span></span>

<span data-ttu-id="85c2a-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="85c2a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="85c2a-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="85c2a-108">Return Value</span></span>

<span data-ttu-id="85c2a-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="85c2a-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85c2a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="85c2a-110">Remarks</span></span>

<span data-ttu-id="85c2a-111">Se **Settings. enableErrorDialogs** for false, esse método poderá ser usado para exibir programaticamente a caixa de diálogo de erro.</span><span class="sxs-lookup"><span data-stu-id="85c2a-111">If **Settings.enableErrorDialogs** is false, this method can be used to programmatically display the error dialog.</span></span> <span data-ttu-id="85c2a-112">Se não houver erros na fila de erros, a caixa de diálogo de erro não será mostrada.</span><span class="sxs-lookup"><span data-stu-id="85c2a-112">If there are no errors in the error queue, the error dialog box is not shown.</span></span>

<span data-ttu-id="85c2a-113">Para o Windows Media Player 9 Series ou posterior, esse método deve ser chamado a partir do manipulador de eventos de erro.</span><span class="sxs-lookup"><span data-stu-id="85c2a-113">For Windows Media Player 9 Series or later, this method must be called from the error event handler.</span></span> <span data-ttu-id="85c2a-114">O Windows Media Player 9 Series ou posterior limpa a fila de erros de capas depois que o evento de erro foi acionado.</span><span class="sxs-lookup"><span data-stu-id="85c2a-114">Windows Media Player 9 Series or later clears the error queue for skins after the error event has been fired.</span></span>

## <a name="requirements"></a><span data-ttu-id="85c2a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85c2a-115">Requirements</span></span>



| <span data-ttu-id="85c2a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="85c2a-116">Requirement</span></span> | <span data-ttu-id="85c2a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="85c2a-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="85c2a-118">Versão</span><span class="sxs-lookup"><span data-stu-id="85c2a-118">Version</span></span><br/> | <span data-ttu-id="85c2a-119">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="85c2a-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85c2a-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="85c2a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85c2a-121">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="85c2a-121">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="85c2a-122">**Settings. enableErrorDialogs**</span><span class="sxs-lookup"><span data-stu-id="85c2a-122">**Settings.enableErrorDialogs**</span></span>](settings-enableerrordialogs.md)
</dt> </dl>

 

 





