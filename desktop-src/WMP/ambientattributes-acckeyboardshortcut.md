---
title: Ambienteattributes. accKeyboardShortcut
description: O atributo accKeyboardShortcut especifica ou recupera uma descrição de atalho de teclado para qualquer elemento.
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- AccKeyboardShortcut do Windows Media Player de ambiente.
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d7259f0b32e3575d902a83b6508383361028d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763384"
---
# <a name="ambientattributesacckeyboardshortcut"></a><span data-ttu-id="55b4c-104">Ambienteattributes. accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="55b4c-104">AmbientAttributes.accKeyboardShortcut</span></span>

<span data-ttu-id="55b4c-105">O atributo **accKeyboardShortcut** especifica ou recupera uma descrição de atalho de teclado para qualquer elemento.</span><span class="sxs-lookup"><span data-stu-id="55b4c-105">The **accKeyboardShortcut** attribute specifies or retrieves a keyboard shortcut description for any element.</span></span>

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a><span data-ttu-id="55b4c-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="55b4c-106">Possible Values</span></span>

<span data-ttu-id="55b4c-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação com um valor padrão de "" (cadeia de caracteres vazia).</span><span class="sxs-lookup"><span data-stu-id="55b4c-107">This attribute is a read/write **String** with a default value of "" (empty string).</span></span> <span data-ttu-id="55b4c-108">Para o elemento **Button** , esse atributo tem um valor padrão de "SPACEBAR ou Enter".</span><span class="sxs-lookup"><span data-stu-id="55b4c-108">For the **BUTTON** element, this attribute has a default value of "Spacebar or Enter".</span></span> <span data-ttu-id="55b4c-109">Para o elemento **Slider** , o valor padrão é "seta para a direita/para cima para aumentar, seta para a esquerda/para baixo para diminuir".</span><span class="sxs-lookup"><span data-stu-id="55b4c-109">For the **SLIDER** element, the default value is "Right/Up Arrow to increase, Left/Down Arrow to decrease".</span></span>

## <a name="remarks"></a><span data-ttu-id="55b4c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="55b4c-110">Remarks</span></span>

<span data-ttu-id="55b4c-111">Esse atributo é usado para fins de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="55b4c-111">This attribute is used for accessibility purposes.</span></span> <span data-ttu-id="55b4c-112">Ele permite uma descrição do atalho de teclado para qualquer elemento a ser lido em voz alta por um programa leitor.</span><span class="sxs-lookup"><span data-stu-id="55b4c-112">It allows a description of the keyboard shortcut for any element to be read aloud by a reader program.</span></span> <span data-ttu-id="55b4c-113">Esse atributo não define o atalho.</span><span class="sxs-lookup"><span data-stu-id="55b4c-113">This attribute does not set the shortcut.</span></span> <span data-ttu-id="55b4c-114">O Scripter deve fazer esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="55b4c-114">The scripter must do that work.</span></span>

<span data-ttu-id="55b4c-115">Esse atributo também se aplica a elementos de botão dentro do controle de grupo de botão.</span><span class="sxs-lookup"><span data-stu-id="55b4c-115">This attribute also applies to button elements inside the button group control.</span></span>

## <a name="requirements"></a><span data-ttu-id="55b4c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55b4c-116">Requirements</span></span>



| <span data-ttu-id="55b4c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="55b4c-117">Requirement</span></span> | <span data-ttu-id="55b4c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="55b4c-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="55b4c-119">Versão</span><span class="sxs-lookup"><span data-stu-id="55b4c-119">Version</span></span><br/> | <span data-ttu-id="55b4c-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="55b4c-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55b4c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="55b4c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b4c-122">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="55b4c-122">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





