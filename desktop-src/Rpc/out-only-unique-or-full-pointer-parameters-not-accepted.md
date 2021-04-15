---
title: Out-Only parâmetros de ponteiro exclusivos ou completos não aceitos
description: Ponteiros únicos ou completos que são \ out somente não são aceitos pelo compilador MIDL. Essas especificações fazem com que o compilador MIDL gere uma mensagem de erro.
ms.assetid: 0477980e-d76e-452f-9ab1-71a8ed8642d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b21baa370c1b68fb3c708a8fdb21115686646f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499107"
---
# <a name="out-only-unique-or-full-pointer-parameters-not-accepted"></a><span data-ttu-id="527d7-104">Out-Only parâmetros de ponteiro exclusivos ou completos não aceitos</span><span class="sxs-lookup"><span data-stu-id="527d7-104">Out-Only Unique or Full Pointer Parameters Not Accepted</span></span>

<span data-ttu-id="527d7-105">Ponteiros exclusivos ou completos que estão \[ [fora](/windows/desktop/Midl/out-idl) \] de somente não são aceitos pelo compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="527d7-105">Unique or full pointers that are \[ [out](/windows/desktop/Midl/out-idl)\]-only are not accepted by the MIDL compiler.</span></span> <span data-ttu-id="527d7-106">Essas especificações fazem com que o compilador MIDL gere uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="527d7-106">Such specifications cause the MIDL compiler to generate an error message.</span></span>

<span data-ttu-id="527d7-107">O stub de servidor gerado automaticamente precisa alocar memória para o ponteiro Referent para que o aplicativo de servidor possa armazenar dados nessa área de memória.</span><span class="sxs-lookup"><span data-stu-id="527d7-107">The automatically generated server stub has to allocate memory for the pointer referent so that the server application can store data in that memory area.</span></span> <span data-ttu-id="527d7-108">De acordo com a definição de um parâmetro somente **\[ out \]**, nenhuma informação sobre o parâmetro é transmitida do cliente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="527d7-108">According to the definition of an **\[out\]**-only parameter, no information about the parameter is transmitted from client to server.</span></span> <span data-ttu-id="527d7-109">No caso de um ponteiro exclusivo, que pode usar o valor NULL, o stub do servidor não tem informações suficientes para duplicar corretamente o ponteiro exclusivo no espaço de endereço do servidor, nem o stub tem informações sobre se o ponteiro deve apontar para um endereço válido ou se deve ser definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="527d7-109">In the case of a unique pointer, which can take the value null, the server stub does not have enough information to correctly duplicate the unique pointer in the server's address space, nor does the stub have any information about whether the pointer should point to a valid address or whether it should be set to null.</span></span> <span data-ttu-id="527d7-110">Portanto, essa combinação não é permitida.</span><span class="sxs-lookup"><span data-stu-id="527d7-110">Therefore, this combination is not allowed.</span></span>

<span data-ttu-id="527d7-111">Em vez de \[ **out**, [Unique](/windows/desktop/Midl/unique) \] ou \[ **out**, ponteiros [PTR](/windows/desktop/Midl/ptr) \] , use \[ ponteiros **in**, **out**, **Unique** \] ou \[ **in**, **out**, **PTR** \] ou use outro nível de indireção, como um ponteiro de referência que aponte para o ponteiro exclusivo ou completo válido.</span><span class="sxs-lookup"><span data-stu-id="527d7-111">Rather than \[**out**, [unique](/windows/desktop/Midl/unique)\] or \[**out**, [ptr](/windows/desktop/Midl/ptr)\] pointers, use \[**in**, **out**, **unique**\] or \[**in**, **out**, **ptr**\] pointers, or use another level of indirection such as a reference pointer that points to the valid unique or full pointer.</span></span>

 

 