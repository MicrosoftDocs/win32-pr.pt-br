---
title: Tratamento de erro (OpenGL)
description: Quando o OpenGL detecta um erro, ele registra um código de erro atual.
ms.assetid: 8e40e382-14fd-44df-8e1c-ebceb34af19c
keywords:
- erro ao manipular o OpenGL
- Tratamento de erro de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2005eb38f85e6e57f814a3ec61abf8b76fa4761
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105768584"
---
# <a name="error-handling-opengl"></a><span data-ttu-id="e1a6b-105">Tratamento de erro (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="e1a6b-105">Error Handling (OpenGL)</span></span>

<span data-ttu-id="e1a6b-106">Quando o OpenGL detecta um erro, ele registra um código de erro atual.</span><span class="sxs-lookup"><span data-stu-id="e1a6b-106">When OpenGL detects an error, it records a current error code.</span></span> <span data-ttu-id="e1a6b-107">A função que causou o erro é ignorada, portanto, não tem nenhum efeito sobre o estado do OpenGL ou sobre o conteúdo do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="e1a6b-107">The function that caused the error is ignored, so it has no effect on the OpenGL state or on the framebuffer contents.</span></span> <span data-ttu-id="e1a6b-108">(Se o erro registrado foi GL \_ SEM \_ \_ memória, no entanto, os resultados da função são indefinidos.) Depois de registrado, o código de erro atual não é limpo até que você chame a função de consulta [**glGetError**](glgeterror.md) , que retorna o código de erro atual.</span><span class="sxs-lookup"><span data-stu-id="e1a6b-108">(If the error recorded was GL\_OUT\_OF\_MEMORY, however, the results of the function are undefined.) Once recorded, the current error code isn't cleared until you call the [**glGetError**](glgeterror.md) query function, which returns the current error code.</span></span>

<span data-ttu-id="e1a6b-109">As implementações do OpenGL podem retornar vários códigos de erro atuais, cada um deles permanece definido até a consulta.</span><span class="sxs-lookup"><span data-stu-id="e1a6b-109">Implementations of OpenGL may return multiple current error codes, each of which remains set until queried.</span></span> <span data-ttu-id="e1a6b-110">A função **glGetError** retornará GL \_ sem \_ erro depois que você tiver consultado todos os códigos de erro atuais ou se não houver erro.</span><span class="sxs-lookup"><span data-stu-id="e1a6b-110">The **glGetError** function returns GL\_NO\_ERROR once you've queried all the current error codes or if there is no error.</span></span> <span data-ttu-id="e1a6b-111">Portanto, se você obtiver um código de erro, chame **glGetError** até o GL \_ nenhum \_ erro será retornado para certificar-se de que você descobriu todos os erros.</span><span class="sxs-lookup"><span data-stu-id="e1a6b-111">Therefore, if you obtain an error code, call **glGetError** until GL\_NO\_ERROR is returned to be sure you've discovered all the errors.</span></span> <span data-ttu-id="e1a6b-112">Para obter a lista de códigos de erro, confira [códigos de erro OpenGL](opengl-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e1a6b-112">For the list of error codes, see [OpenGL error codes](opengl-error-codes.md).</span></span>

<span data-ttu-id="e1a6b-113">Você pode usar a função [**gluErrorString**](gluerrorstring.md) Glu para obter uma cadeia de caracteres descritiva correspondente ao código de erro passado.</span><span class="sxs-lookup"><span data-stu-id="e1a6b-113">You can use the [**gluErrorString**](gluerrorstring.md) GLU function to obtain a descriptive string corresponding to the error code passed in.</span></span> <span data-ttu-id="e1a6b-114">Para obter mais informações sobre o **gluErrorString**, consulte [tratamento de erros](handling-errors.md).</span><span class="sxs-lookup"><span data-stu-id="e1a6b-114">For more information on **gluErrorString**, see [Handling Errors](handling-errors.md).</span></span>

> [!Note]  
> <span data-ttu-id="e1a6b-115">As funções GLU geralmente retornam valores de erro se um erro for detectado.</span><span class="sxs-lookup"><span data-stu-id="e1a6b-115">GLU functions often return error values if an error is detected.</span></span> <span data-ttu-id="e1a6b-116">Além disso, a biblioteca do utilitário OpenGL define os códigos de erro GLU \_ Enumeração inválida \_ , glu \_ \_ valor inválido e Glu \_ memória insuficiente \_ \_ , que têm o mesmo significado que os códigos de erro OpenGL relacionados.</span><span class="sxs-lookup"><span data-stu-id="e1a6b-116">Also, the OpenGL Utility library defines the error codes GLU\_INVALID\_ENUM, GLU\_INVALID\_VALUE, and GLU\_OUT\_OF\_MEMORY, which have the same meaning as the related OpenGL error codes.</span></span>

 

 

 




