---
title: Tipos de dados de função e valores de retorno
description: Tipos de dados de função e valores de retorno
ms.assetid: a17ec8bb-4369-463f-8c67-11457a18595b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28bd7484c3d968e92da5fcd19ee738da1ee811a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916192"
---
# <a name="function-data-types-and-return-values"></a><span data-ttu-id="b6a2b-103">Tipos de dados de função e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="b6a2b-103">Function Data Types and Return Values</span></span>

<span data-ttu-id="b6a2b-104">As funções e macros do AVIFile usam manipuladores de arquivo e fluxo implementados com a tecnologia OLE.</span><span class="sxs-lookup"><span data-stu-id="b6a2b-104">The AVIFile functions and macros use file and stream handlers implemented with OLE technology.</span></span> <span data-ttu-id="b6a2b-105">O tipo de dados padrão de uma função OLE é **STDAPI**, e a função retorna um valor **HRESULT** (zero para êxito ou erro de outra forma).</span><span class="sxs-lookup"><span data-stu-id="b6a2b-105">The standard data type of an OLE function is **STDAPI**, and the function returns an **HRESULT** value (zero for success or an error otherwise).</span></span> <span data-ttu-id="b6a2b-106">Se uma função retornar um valor diferente de um **HRESULT**, o tipo do protótipo da função terá uma sintaxe ligeiramente diferente que incorporará o tipo de valor de retorno entre parênteses após "STDAPI \_ ".</span><span class="sxs-lookup"><span data-stu-id="b6a2b-106">If a function returns a value other than an **HRESULT**, the type of the function's prototype has a slightly different syntax that embeds the return value type in parentheses following "STDAPI\_".</span></span> <span data-ttu-id="b6a2b-107">Por exemplo, uma função que retorna um valor de dados **Long** usa **STDAPI \_ (Long)** na instrução de protótipo.</span><span class="sxs-lookup"><span data-stu-id="b6a2b-107">For example, a function that returns a **LONG** data value uses **STDAPI\_(LONG)** in the prototype statement.</span></span>

 

 




