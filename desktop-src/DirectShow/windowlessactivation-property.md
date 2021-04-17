---
description: A propriedade WindowlessActivation Inicializa o objeto MSWebDVD no tempo de design para o modo de janela ou sem janela.
ms.assetid: 290a9459-154a-4ec7-a013-d696e6b27341
title: Propriedade WindowlessActivation
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427fdcb265d60200bfe8716cd1ece384861fbdf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770243"
---
# <a name="windowlessactivation-property"></a><span data-ttu-id="f7f40-103">Propriedade WindowlessActivation</span><span class="sxs-lookup"><span data-stu-id="f7f40-103">WindowlessActivation Property</span></span>

> [!Note]  
> <span data-ttu-id="f7f40-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f7f40-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f7f40-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f7f40-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f7f40-106">A `WindowlessActivation` Propriedade Inicializa o objeto **MSWebDVD** no tempo de design para o modo de janela ou sem janela.</span><span class="sxs-lookup"><span data-stu-id="f7f40-106">The `WindowlessActivation` property initializes the **MSWebDVD** object at design time for either windowed or windowless mode.</span></span>

``` syntax
[ bWindowless = ] MSWebDVD.WindowlessActivation
```

## <a name="return-value"></a><span data-ttu-id="f7f40-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f7f40-107">Return Value</span></span>

<span data-ttu-id="f7f40-108">Retorna se o objeto está no modo de janela como um booliano.</span><span class="sxs-lookup"><span data-stu-id="f7f40-108">Returns whether the object is in windowed mode as a Boolean.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7f40-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7f40-109">Remarks</span></span>

<span data-ttu-id="f7f40-110">Essa propriedade é de leitura/gravação com um valor padrão de true.</span><span class="sxs-lookup"><span data-stu-id="f7f40-110">This property is read/write with a default value of true.</span></span> <span data-ttu-id="f7f40-111">Portanto, você só precisa definir essa propriedade se estiver executando o objeto **MSWebDVD** em um contêiner em janela.</span><span class="sxs-lookup"><span data-stu-id="f7f40-111">Therefore, you only need to set this property if you are running the **MSWebDVD** object in a windowed container.</span></span> <span data-ttu-id="f7f40-112">Quando contido em uma página da Web no Microsoft® Internet Explorer, o **MSWebDVD** está sempre no modo sem janela e você não precisa definir essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f7f40-112">When contained in a Web page in Microsoft® Internet Explorer, **MSWebDVD** is always in windowless mode, and you don't need to set this property.</span></span>

 

 



