---
title: Valores de retorno de função
description: Os valores de retorno de função são semelhantes aos parâmetros somente-out-only porque seus dados não são fornecidos pelo aplicativo cliente.
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ada3808d024f201ef01a5f4977149a0ab9c75e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105787028"
---
# <a name="function-return-values"></a><span data-ttu-id="e85b4-103">Valores de retorno de função</span><span class="sxs-lookup"><span data-stu-id="e85b4-103">Function Return Values</span></span>

<span data-ttu-id="e85b4-104">Os valores de retorno de função são semelhantes aos parâmetros somente de **\[ saída \]** porque seus dados não são fornecidos pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="e85b4-104">Function return values are similar to **\[out\]**-only parameters because their data is not provided by the client application.</span></span> <span data-ttu-id="e85b4-105">No entanto, eles são gerenciados de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="e85b4-105">However they are managed differently.</span></span> <span data-ttu-id="e85b4-106">Ao contrário dos parâmetros somente **\[ out \]**, eles não precisam ser ponteiros.</span><span class="sxs-lookup"><span data-stu-id="e85b4-106">Unlike **\[out\]**-only parameters, they are not required to be pointers.</span></span> <span data-ttu-id="e85b4-107">O procedimento remoto pode retornar qualquer tipo de dados válido, exceto ponteiros de referência e uniões não encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="e85b4-107">The remote procedure can return any valid data type except reference pointers and nonencapsulated unions.</span></span>

<span data-ttu-id="e85b4-108">No entanto, é recomendável usar um parâmetro **\[ out \]** em vez de um valor de retorno para tipos de dados complexos.</span><span class="sxs-lookup"><span data-stu-id="e85b4-108">However, using an **\[out\]** parameter instead of a return value for complex data types is recommended.</span></span> <span data-ttu-id="e85b4-109">Ao retornar tipos de dados complexos, o compilador MIDL gerará um stub de modo/os.</span><span class="sxs-lookup"><span data-stu-id="e85b4-109">While returning complex data types, the MIDL compiler will generate an /Os mode stub.</span></span> <span data-ttu-id="e85b4-110">Como resultado, todas as informações recentes de verificação de erros fornecidas pelo/robust são perdidas.</span><span class="sxs-lookup"><span data-stu-id="e85b4-110">As a result, all recent error-checking information provided by /robust is lost.</span></span>

<span data-ttu-id="e85b4-111">Os valores de retorno de função que são tipos de ponteiro são alocados pelo stub do cliente com uma chamada para [ \_ \_ alocar usuário de MIDL](/windows/desktop/Midl/midl-user-allocate-1).</span><span class="sxs-lookup"><span data-stu-id="e85b4-111">Function return values that are pointer types are allocated by the client stub with a call to [midl\_user\_allocate](/windows/desktop/Midl/midl-user-allocate-1).</span></span> <span data-ttu-id="e85b4-112">Da mesma forma, somente o atributo de ponteiro exclusivo ou completo pode ser aplicado a um tipo de retorno de função de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="e85b4-112">Accordingly, only the unique or full pointer attribute can be applied to a pointer function-return type.</span></span>

 

 