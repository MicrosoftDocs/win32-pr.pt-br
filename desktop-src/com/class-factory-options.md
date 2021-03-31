---
title: Opções de fábrica de classes
description: Opções de fábrica de classes
ms.assetid: e9e33e07-7628-4c5e-965d-e12a9c1d69c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fab52ea11a0e7e20d10757eb8d6e86577afc35c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641882"
---
# <a name="class-factory-options"></a><span data-ttu-id="ccc6c-103">Opções de fábrica de classes</span><span class="sxs-lookup"><span data-stu-id="ccc6c-103">Class Factory Options</span></span>

<span data-ttu-id="ccc6c-104">Um controle ActiveX, em virtude de ser um objeto COM, deve ter um código de servidor associado que dê suporte à criação de controle por meio de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) como um mínimo.</span><span class="sxs-lookup"><span data-stu-id="ccc6c-104">An ActiveX Control, by virtue of being a COM object, must have associated server code that supports control creation through [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) as a minimum.</span></span>

<span data-ttu-id="ccc6c-105">É opcional, não obrigatório, que esse objeto de classe também ofereça suporte a [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) para o gerenciamento de licenciamento.</span><span class="sxs-lookup"><span data-stu-id="ccc6c-105">It is optional, not required, that this class object also support [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) for licensing management.</span></span> <span data-ttu-id="ccc6c-106">Somente os fornecedores que se preocupam com o licenciamento precisam dar suporte ao mecanismo de licenciamento do COM.</span><span class="sxs-lookup"><span data-stu-id="ccc6c-106">Only those vendors that are concerned about licensing need to support COM's licensing mechanism.</span></span> <span data-ttu-id="ccc6c-107">Em outras palavras, como **IClassFactory2** é a única maneira de alcançar o licenciamento de nível com, essa interface é necessária no objeto de classe para os controles que desejam ser licenciados.</span><span class="sxs-lookup"><span data-stu-id="ccc6c-107">In other words, because **IClassFactory2** is the only way to achieve COM-level licensing, this interface is required on the class object for those controls that want to be licensed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccc6c-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ccc6c-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccc6c-109">Controles</span><span class="sxs-lookup"><span data-stu-id="ccc6c-109">Controls</span></span>](controls.md)
</dt> </dl>

 

 