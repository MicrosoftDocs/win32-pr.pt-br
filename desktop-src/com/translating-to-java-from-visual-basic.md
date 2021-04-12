---
title: Convertendo para Java de Visual Basic
description: Convertendo para Java de Visual Basic
ms.assetid: 2bd61efc-f4f4-46f7-aa5a-f6cefc54d86b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84d02071641901c5217069d997c22fa04c94cef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363712"
---
# <a name="translating-to-java-from-visual-basic"></a><span data-ttu-id="5023e-103">Convertendo para Java de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5023e-103">Translating to Java from Visual Basic</span></span>

<span data-ttu-id="5023e-104">Por padrão, Visual Basic passa parâmetros por referência.</span><span class="sxs-lookup"><span data-stu-id="5023e-104">By default, Visual Basic passes parameters by reference.</span></span> <span data-ttu-id="5023e-105">Parâmetros que devem ser passados pelo valor somente são especificados pela palavra-chave **ByVal**.</span><span class="sxs-lookup"><span data-stu-id="5023e-105">Parameters that are meant to be passed by value only are specified by the keyword **ByVal**.</span></span>

<span data-ttu-id="5023e-106">O Java não oferece suporte a matrizes multidimensionais.</span><span class="sxs-lookup"><span data-stu-id="5023e-106">Java does not support multidimensional arrays.</span></span> <span data-ttu-id="5023e-107">Métodos que aceitam ou retornam matrizes multidimensionais não estão disponíveis no Java.</span><span class="sxs-lookup"><span data-stu-id="5023e-107">Methods that accept or return multidimensional arrays are not available from Java.</span></span>

<span data-ttu-id="5023e-108">Java e Visual Basic diferem ligeiramente na forma como representam propriedades.</span><span class="sxs-lookup"><span data-stu-id="5023e-108">Java and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="5023e-109">No Java, as propriedades são representadas como um conjunto de funções de acessador, uma que define o valor da propriedade e outra que recupera o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="5023e-109">In Java, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="5023e-110">Em Visual Basic, as propriedades são representadas como um único item que pode ser usado para recuperar ou definir o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="5023e-110">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5023e-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5023e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5023e-112">Convertendo para Java</span><span class="sxs-lookup"><span data-stu-id="5023e-112">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




