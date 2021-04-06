---
description: O método de exibição de cursor torna o cursor visível quando o objeto MSWebDVD está no modo de tela inteira.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: Método de concursor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917c1d0d2724259fc19baf72ab6b3844cddc3419
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825829"
---
# <a name="showcursor-method"></a><span data-ttu-id="edecf-103">Método de concursor</span><span class="sxs-lookup"><span data-stu-id="edecf-103">ShowCursor Method</span></span>

> [!Note]  
> <span data-ttu-id="edecf-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="edecf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="edecf-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="edecf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="edecf-106">O `ShowCursor` método torna o cursor visível quando o objeto **MSWebDVD** está no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="edecf-106">The `ShowCursor` method makes the cursor visible when the **MSWebDVD** object is in full-screen mode.</span></span>

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a><span data-ttu-id="edecf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="edecf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edecf-108"><span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*</span><span class="sxs-lookup"><span data-stu-id="edecf-108"><span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*</span></span>
</dt> <dd>

<span data-ttu-id="edecf-109">Especifica se o cursor deve ser mostrado como um booliano.</span><span class="sxs-lookup"><span data-stu-id="edecf-109">Specifies whether to show the cursor as a Boolean.</span></span>



| <span data-ttu-id="edecf-110">Valor</span><span class="sxs-lookup"><span data-stu-id="edecf-110">Value</span></span> | <span data-ttu-id="edecf-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="edecf-111">Description</span></span>            |
|-------|------------------------|
| <span data-ttu-id="edecf-112">true</span><span class="sxs-lookup"><span data-stu-id="edecf-112">true</span></span>  | <span data-ttu-id="edecf-113">Exibir o cursor</span><span class="sxs-lookup"><span data-stu-id="edecf-113">Show the cursor</span></span>        |
| <span data-ttu-id="edecf-114">false</span><span class="sxs-lookup"><span data-stu-id="edecf-114">false</span></span> | <span data-ttu-id="edecf-115">Não mostrar o cursor</span><span class="sxs-lookup"><span data-stu-id="edecf-115">Do not show the cursor</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edecf-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="edecf-116">Return Value</span></span>

<span data-ttu-id="edecf-117">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="edecf-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="edecf-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="edecf-118">Remarks</span></span>

<span data-ttu-id="edecf-119">Quando a exibição do DVD entra no modo de tela inteira, o cursor desaparece dentro de 3 a 5 segundos.</span><span class="sxs-lookup"><span data-stu-id="edecf-119">When the DVD display goes into full-screen mode, the cursor disappears within 3 to 5 seconds.</span></span> <span data-ttu-id="edecf-120">Use esse método para tornar o cursor visível novamente se os botões de controle do seu aplicativo estiverem visíveis no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="edecf-120">Use this method to make the cursor visible again if your application's control buttons are visible in full-screen mode.</span></span>

 

 



