---
title: Criando um manipulador de arquivo ou de fluxo
description: Criando um manipulador de arquivo ou de fluxo
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b2f118f4f5279cea1aacedd58b86f23afa9a9af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005383"
---
# <a name="creating-a-file-or-stream-handler"></a><span data-ttu-id="7e463-103">Criando um manipulador de arquivo ou de fluxo</span><span class="sxs-lookup"><span data-stu-id="7e463-103">Creating a File or Stream Handler</span></span>

<span data-ttu-id="7e463-104">Em um aplicativo escrito na linguagem de programação C, um manipulador de arquivo ou fluxo geralmente cria uma função para cada método.</span><span class="sxs-lookup"><span data-stu-id="7e463-104">In an application written in the C programming language, a file or stream handler usually creates a function for each method.</span></span> <span data-ttu-id="7e463-105">Seu aplicativo acessa essas funções por meio de uma matriz de ponteiros de função que o manipulador de fluxo cria.</span><span class="sxs-lookup"><span data-stu-id="7e463-105">Your application accesses these functions through an array of function pointers the stream handler creates.</span></span> <span data-ttu-id="7e463-106">Uma estrutura **IAVIStreamVtbl** contém a matriz de ponteiros de função.</span><span class="sxs-lookup"><span data-stu-id="7e463-106">An **IAVIStreamVtbl** structure contains the array of function pointers.</span></span> <span data-ttu-id="7e463-107">Um manipulador de fluxo pode atribuir qualquer nome que desejar para funções que ele cria para os métodos.</span><span class="sxs-lookup"><span data-stu-id="7e463-107">A stream handler can assign any name it wants to functions it creates for the methods.</span></span> <span data-ttu-id="7e463-108">A posição do ponteiro de função na estrutura implica a correspondência da função para o método.</span><span class="sxs-lookup"><span data-stu-id="7e463-108">The position of the function pointer in the structure implies the correspondence of the function to the method.</span></span> <span data-ttu-id="7e463-109">Por exemplo, o primeiro ponteiro de função na estrutura corresponde ao método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="7e463-109">For example, the first function pointer in the structure corresponds to the **QueryInterface** method.</span></span> <span data-ttu-id="7e463-110">Seu manipulador de fluxo deve fornecer todas as funções de uma interface.</span><span class="sxs-lookup"><span data-stu-id="7e463-110">Your stream handler must provide all the functions of an interface.</span></span>

 

 




