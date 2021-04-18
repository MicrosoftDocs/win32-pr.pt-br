---
title: Ambienteattributes. zIndex
description: O atributo zIndex especifica ou recupera a ordem na qual o controle é renderizado.
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- ZIndex do Windows Media Player de ambiente.
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52480cc387c0a9e5e45c4b8e8fd2dae4199dbd16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770527"
---
# <a name="ambientattributeszindex"></a><span data-ttu-id="396a5-104">Ambienteattributes. zIndex</span><span class="sxs-lookup"><span data-stu-id="396a5-104">AmbientAttributes.zIndex</span></span>

<span data-ttu-id="396a5-105">O atributo **ZIndex** especifica ou recupera a ordem na qual o controle é renderizado.</span><span class="sxs-lookup"><span data-stu-id="396a5-105">The **zIndex** attribute specifies or retrieves the order in which the control is rendered.</span></span>

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a><span data-ttu-id="396a5-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="396a5-106">Possible Values</span></span>

<span data-ttu-id="396a5-107">Esse atributo é um **número** de leitura/gravação (**longo**) com um valor padrão de zero.</span><span class="sxs-lookup"><span data-stu-id="396a5-107">This attribute is a read/write **Number** (**long**) with a default value of zero.</span></span> <span data-ttu-id="396a5-108">O intervalo é o de um inteiro longo assinado.</span><span class="sxs-lookup"><span data-stu-id="396a5-108">The range is that of a signed long integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="396a5-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="396a5-109">Remarks</span></span>

<span data-ttu-id="396a5-110">O bitmap em segundo plano de uma **exibição** ou **subexibição** tem um índice z fixo de zero.</span><span class="sxs-lookup"><span data-stu-id="396a5-110">The background bitmap of a **VIEW** or **SUBVIEW** has a fixed z index of zero.</span></span> <span data-ttu-id="396a5-111">Se você quiser que um controle esteja por trás do plano de fundo, o **ZIndex** deverá ser definido como um número negativo.</span><span class="sxs-lookup"><span data-stu-id="396a5-111">If you want a control to be behind the background, the **zIndex** must be set to a negative number.</span></span>

<span data-ttu-id="396a5-112">O índice z de um **modo de exibição** ou de uma **subexibição** é um índice absoluto, enquanto o índice z de um controle é relativo ao índice z da **exibição** ou **subexibição** que o contém.</span><span class="sxs-lookup"><span data-stu-id="396a5-112">The z index of a **VIEW** or **SUBVIEW** is an absolute index, while the z index of a control is relative to the z index of the **VIEW** or **SUBVIEW** that contains it.</span></span>

<span data-ttu-id="396a5-113">Não há suporte para o atributo **ZIndex** nos elementos **browser** e **playlist** .</span><span class="sxs-lookup"><span data-stu-id="396a5-113">The **zIndex** attribute is not supported by the **BROWSER** and **PLAYLIST** elements.</span></span> <span data-ttu-id="396a5-114">Ele não funcionará com o elemento **Video** se for um *vídeo*. **sem janela** é definido como false, nem com o elemento **Effects** , se houver **efeitos**. em **janela** é definido como true.</span><span class="sxs-lookup"><span data-stu-id="396a5-114">It will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if **EFFECTS**.**windowed** is set to true.</span></span>

<span data-ttu-id="396a5-115">Os elementos **buttonelement** usam o **ZIndex** de seus **botões**.</span><span class="sxs-lookup"><span data-stu-id="396a5-115">**BUTTONELEMENT** elements use the **zIndex** of their **BUTTONGROUP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="396a5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="396a5-116">Requirements</span></span>



| <span data-ttu-id="396a5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="396a5-117">Requirement</span></span> | <span data-ttu-id="396a5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="396a5-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="396a5-119">Versão</span><span class="sxs-lookup"><span data-stu-id="396a5-119">Version</span></span><br/> | <span data-ttu-id="396a5-120">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="396a5-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="396a5-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="396a5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="396a5-122">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="396a5-122">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





