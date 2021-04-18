---
title: Salvando e restaurando conjuntos de variáveis de estado
description: Você pode salvar e restaurar os valores de uma coleção de variáveis de estado em uma pilha de atributos com as funções glPushAttrib e glPopAttrib.
ms.assetid: 339de633-4158-4907-b985-2d75b465fb2a
keywords:
- Variáveis de estado OpenGL
- Salvando variáveis de estado OpenGL
- restaurando variáveis de estado OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3192c228ea35005c5755802d3cd1b873f7b7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105750458"
---
# <a name="saving-and-restoring-sets-of-state-variables"></a><span data-ttu-id="e2cc8-106">Salvando e restaurando conjuntos de variáveis de estado</span><span class="sxs-lookup"><span data-stu-id="e2cc8-106">Saving and Restoring Sets of State Variables</span></span>

<span data-ttu-id="e2cc8-107">Você pode salvar e restaurar os valores de uma coleção de variáveis de estado em uma pilha de atributos com as funções [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) .</span><span class="sxs-lookup"><span data-stu-id="e2cc8-107">You can save and restore the values of a collection of state variables on an attribute stack with the [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) functions.</span></span> <span data-ttu-id="e2cc8-108">A pilha de atributos tem uma profundidade de pelo menos 16.</span><span class="sxs-lookup"><span data-stu-id="e2cc8-108">The attribute stack has a depth of at least 16.</span></span> <span data-ttu-id="e2cc8-109">Para obter a profundidade real, use a \_ profundidade máxima de \_ \_ pilha de Atrib GL \_ com [**glGetIntegerv**](glgetintegerv.md).</span><span class="sxs-lookup"><span data-stu-id="e2cc8-109">To obtain the actual depth, use GL\_MAX\_ATTRIB\_STACK\_DEPTH with [**glGetIntegerv**](glgetintegerv.md).</span></span> <span data-ttu-id="e2cc8-110">Enviar por push uma pilha completa ou limpar uma vazia gera um erro.</span><span class="sxs-lookup"><span data-stu-id="e2cc8-110">Pushing a full stack or popping an empty one generates an error.</span></span>

<span data-ttu-id="e2cc8-111">Em geral, é mais rápido usar **glPushAttrib** e **glPopAttrib** do que obter e restaurar os valores por conta própria.</span><span class="sxs-lookup"><span data-stu-id="e2cc8-111">It is generally faster to use **glPushAttrib** and **glPopAttrib** than to get and restore the values yourself.</span></span> <span data-ttu-id="e2cc8-112">Alguns valores podem ser enviados e retirados no hardware, e salvar e restaurá-los pode ter uso intensivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e2cc8-112">Some values might be pushed and popped in the hardware, and saving and restoring them can be resource-intensive.</span></span> <span data-ttu-id="e2cc8-113">Além disso, se você estiver operando em um cliente remoto, todos os dados de atributo deverão ser transferidos pela conexão de rede e de volta conforme são salvos e restaurados.</span><span class="sxs-lookup"><span data-stu-id="e2cc8-113">Also, if you're operating on a remote client, all of the attribute data must be transferred across the network connection and back as it is saved and restored.</span></span> <span data-ttu-id="e2cc8-114">No entanto, a implementação do OpenGL mantém a pilha de atributos no servidor, evitando atrasos de rede desnecessários.</span><span class="sxs-lookup"><span data-stu-id="e2cc8-114">However, your OpenGL implementation keeps the attribute stack on the server, avoiding unnecessary network delays.</span></span>

<span data-ttu-id="e2cc8-115">O protótipo de **glPushAttrib** é:</span><span class="sxs-lookup"><span data-stu-id="e2cc8-115">The prototype of **glPushAttrib** is:</span></span>

<span data-ttu-id="e2cc8-116">**void** **glPushAttrib**( *máscara* de GLbitfield);</span><span class="sxs-lookup"><span data-stu-id="e2cc8-116">**void** **glPushAttrib**(**GLbitfield** *mask* );</span></span>

<span data-ttu-id="e2cc8-117">O uso de [**glPushAttrib**](glpushattrib.md) salva todos os atributos indicados por bits na *máscara* , enviando-os por push para a pilha de atributos.</span><span class="sxs-lookup"><span data-stu-id="e2cc8-117">Using [**glPushAttrib**](glpushattrib.md) saves all the attributes indicated by bits in *mask* by pushing them onto the attribute stack.</span></span> <span data-ttu-id="e2cc8-118">Para obter uma lista dos bits de máscara possíveis que você pode logicamente ou juntos para salvar qualquer combinação de atributos, consulte [grupos de atributos](attribute-groups.md).</span><span class="sxs-lookup"><span data-stu-id="e2cc8-118">For a list of the possible mask bits you can logically OR together to save any combination of attributes, see [Attribute Groups](attribute-groups.md).</span></span> <span data-ttu-id="e2cc8-119">Cada bit corresponde a uma coleção de variáveis de estado individuais.</span><span class="sxs-lookup"><span data-stu-id="e2cc8-119">Each bit corresponds to a collection of individual state variables.</span></span> <span data-ttu-id="e2cc8-120">Por exemplo, \_ o bit de iluminação GL \_ refere-se a todas as variáveis de estado relacionadas à iluminação, que incluem a cor do material atual; o ambiente, a difusão, a especulação e a luz emitida; uma lista das luzes que estão habilitadas; e as direções dos destaques.</span><span class="sxs-lookup"><span data-stu-id="e2cc8-120">For example, GL\_LIGHTING\_BIT refers to all the state variables related to lighting, which include the current material color; the ambient, diffuse, specular, and emitted light; a list of the lights that are enabled; and the directions of the spotlights.</span></span> <span data-ttu-id="e2cc8-121">Quando você chama [**glPopAttrib**](glpopattrib.md), todas essas variáveis são restauradas.</span><span class="sxs-lookup"><span data-stu-id="e2cc8-121">When you call [**glPopAttrib**](glpopattrib.md), all those variables are restored.</span></span> <span data-ttu-id="e2cc8-122">Para descobrir exatamente quais atributos são salvos para valores de máscara específicos, consulte [variáveis de estado OpenGL](opengl-state-variables.md).</span><span class="sxs-lookup"><span data-stu-id="e2cc8-122">To find out exactly which attributes are saved for particular mask values, see [OpenGL State Variables](opengl-state-variables.md).</span></span>

 

 




