---
title: Admy. editstyle
description: O atributo editstyle especifica ou recupera o estilo do controle caixa de edição.
ms.assetid: 1b3052c4-3087-4d41-af03-d7758680cc3b
keywords:
- Admy. editstyle Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.editStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f225dfca0ec00dd4f45a4eb63f6b2503d5df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758220"
---
# <a name="editboxeditstyle"></a><span data-ttu-id="f1579-104">Admy. editstyle</span><span class="sxs-lookup"><span data-stu-id="f1579-104">EDITBOX.editStyle</span></span>

<span data-ttu-id="f1579-105">O atributo **editstyle** especifica ou recupera o estilo do controle caixa de edição.</span><span class="sxs-lookup"><span data-stu-id="f1579-105">The **editStyle** attribute specifies or retrieves the style of the edit box control.</span></span>

``` syntax
        elementID.editStyle
```

## <a name="possible-values"></a><span data-ttu-id="f1579-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="f1579-106">Possible Values</span></span>

<span data-ttu-id="f1579-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1579-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="f1579-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f1579-108">Value</span></span>     | <span data-ttu-id="f1579-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1579-109">Description</span></span>                                                                     |
|-----------|---------------------------------------------------------------------------------|
| <span data-ttu-id="f1579-110">normal</span><span class="sxs-lookup"><span data-stu-id="f1579-110">normal</span></span>    | <span data-ttu-id="f1579-111">Padrão.</span><span class="sxs-lookup"><span data-stu-id="f1579-111">Default.</span></span> <span data-ttu-id="f1579-112">Exibe texto normal em uma única linha.</span><span class="sxs-lookup"><span data-stu-id="f1579-112">Displays normal text on a single line.</span></span>                                 |
| <span data-ttu-id="f1579-113">password</span><span class="sxs-lookup"><span data-stu-id="f1579-113">password</span></span>  | <span data-ttu-id="f1579-114">Exibe asteriscos ( \* ) no lugar do texto.</span><span class="sxs-lookup"><span data-stu-id="f1579-114">Displays asterisks (\*) in place of text.</span></span> <span data-ttu-id="f1579-115">Só pode ser especificado em tempo de design.</span><span class="sxs-lookup"><span data-stu-id="f1579-115">Can only be specified at design time.</span></span> |
| <span data-ttu-id="f1579-116">letras maiúsculas</span><span class="sxs-lookup"><span data-stu-id="f1579-116">uppercase</span></span> | <span data-ttu-id="f1579-117">Exibe o texto como todas as letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="f1579-117">Displays text as all uppercase.</span></span>                                                 |
| <span data-ttu-id="f1579-118">letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="f1579-118">lowercase</span></span> | <span data-ttu-id="f1579-119">Exibe o texto como todas as letras minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f1579-119">Displays text as all lowercase.</span></span>                                                 |
| <span data-ttu-id="f1579-120">número</span><span class="sxs-lookup"><span data-stu-id="f1579-120">number</span></span>    | <span data-ttu-id="f1579-121">Exibe apenas números.</span><span class="sxs-lookup"><span data-stu-id="f1579-121">Only displays numbers.</span></span>                                                          |
| <span data-ttu-id="f1579-122">tiverem</span><span class="sxs-lookup"><span data-stu-id="f1579-122">multiline</span></span> | <span data-ttu-id="f1579-123">Exibe várias linhas de texto.</span><span class="sxs-lookup"><span data-stu-id="f1579-123">Displays multiple lines of text.</span></span> <span data-ttu-id="f1579-124">Só pode ser especificado em tempo de design.</span><span class="sxs-lookup"><span data-stu-id="f1579-124">Can only be specified at design time.</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="f1579-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1579-125">Remarks</span></span>

<span data-ttu-id="f1579-126">Esse atributo só pode ser definido como "password" ou "Multiline" em tempo de design.</span><span class="sxs-lookup"><span data-stu-id="f1579-126">This attribute can only be set to "password" or "multiline" at design time.</span></span> <span data-ttu-id="f1579-127">Se estiver definido como "Multiline", o valor não poderá ser alterado em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f1579-127">If it is set to "multiline", the value cannot be changed at run time.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1579-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1579-128">Requirements</span></span>



| <span data-ttu-id="f1579-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1579-129">Requirement</span></span> | <span data-ttu-id="f1579-130">Valor</span><span class="sxs-lookup"><span data-stu-id="f1579-130">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="f1579-131">Versão</span><span class="sxs-lookup"><span data-stu-id="f1579-131">Version</span></span><br/> | <span data-ttu-id="f1579-132">Windows Media Player para Windows XP ou posterior</span><span class="sxs-lookup"><span data-stu-id="f1579-132">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1579-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1579-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1579-134">**Elemento admy**</span><span class="sxs-lookup"><span data-stu-id="f1579-134">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> </dl>

 

 





