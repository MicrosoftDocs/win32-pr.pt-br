---
description: Trabalhando com buffers de mídia DMO
ms.assetid: 6d0c51b8-0d79-4f04-8e90-0cea4f3b1427
title: Trabalhando com buffers de mídia DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c870b3a4a035c71a4dcadf9a38b4c2a150097e7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105784572"
---
# <a name="working-with-dmo-media-buffers"></a><span data-ttu-id="6bc63-103">Trabalhando com buffers de mídia DMO</span><span class="sxs-lookup"><span data-stu-id="6bc63-103">Working with DMO Media Buffers</span></span>

<span data-ttu-id="6bc63-104">Os dados de entrada são passados para o codec DMOs usando buffers de mídia.</span><span class="sxs-lookup"><span data-stu-id="6bc63-104">Input data is passed to the codec DMOs using media buffers.</span></span> <span data-ttu-id="6bc63-105">Um buffer de mídia é um objeto que implementa a interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="6bc63-105">A media buffer is an object that implements the [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) interface.</span></span> <span data-ttu-id="6bc63-106">Você pode implementar uma classe para essa finalidade ou, se você estiver usando o Windows Media Format SDK em seu aplicativo, poderá usar os objetos de buffer que são definidos nesse SDK.</span><span class="sxs-lookup"><span data-stu-id="6bc63-106">You can implement a class for this purpose or, if you are using the Windows Media Format SDK in your application, you can use the buffer objects that are defined in that SDK.</span></span>

<span data-ttu-id="6bc63-107">Se você implementar sua própria classe de buffer, tenha cuidado com a forma como a memória de buffer é manipulada.</span><span class="sxs-lookup"><span data-stu-id="6bc63-107">If you implement your own buffer class, be careful about how the buffer memory is handled.</span></span> <span data-ttu-id="6bc63-108">Quando você passa um exemplo de entrada, o DMO mantém uma referência ao buffer até que ele seja concluído com o exemplo.</span><span class="sxs-lookup"><span data-stu-id="6bc63-108">When you pass an input sample, the DMO keeps a reference to the buffer until it is finished with the sample.</span></span> <span data-ttu-id="6bc63-109">Você pode liberar imediatamente sua referência para a interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) , mas não tem como saber quando o codec não precisa mais de sua referência.</span><span class="sxs-lookup"><span data-stu-id="6bc63-109">You can immediately release your reference to the [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) interface, but you have no way of knowing when the codec no longer needs its reference.</span></span> <span data-ttu-id="6bc63-110">Para ter certeza de que a memória é liberada quando o objeto se exclui, você deve implementar sua classe para que ela aloque e libere a memória para o buffer internamente.</span><span class="sxs-lookup"><span data-stu-id="6bc63-110">To be certain that the memory is freed when the object deletes itself, you should implement your class so that it allocates and frees the memory for the buffer internally.</span></span>

<span data-ttu-id="6bc63-111">Como o DMOs mantém referências a buffers por um período de tempo desconhecido, não é uma questão comum usar um pool limitado de buffers.</span><span class="sxs-lookup"><span data-stu-id="6bc63-111">Because the DMOs keep references to buffers for an unknown period of time, it is not a trivial matter to use a limited pool of buffers.</span></span> <span data-ttu-id="6bc63-112">A solução mais simples é alocar um novo buffer para cada exemplo, embora fazer isso não seja eficiente.</span><span class="sxs-lookup"><span data-stu-id="6bc63-112">The simplest solution is to allocate a new buffer for each sample, although doing so is inefficient.</span></span>

<span data-ttu-id="6bc63-113">Uma solução melhor é implementar um objeto para gerenciar um pool de buffers.</span><span class="sxs-lookup"><span data-stu-id="6bc63-113">A better solution is to implement an object to manage a pool of buffers.</span></span> <span data-ttu-id="6bc63-114">Para fazer isso, escreva o código no método **Release** da sua implementação [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) que chama um método de seu Gerenciador de buffer (em vez de excluir a si mesmo) quando a contagem de referência cai para zero.</span><span class="sxs-lookup"><span data-stu-id="6bc63-114">To do this, write code in the **Release** method of your [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) implementation that calls a method of your buffer manager (instead of deleting itself) when the reference count drops to zero.</span></span> <span data-ttu-id="6bc63-115">O Gerenciador de buffer pode manter uma lista de ponteiros para objetos de buffer alocados.</span><span class="sxs-lookup"><span data-stu-id="6bc63-115">The buffer manager can then maintain a list of pointers to allocated buffer objects.</span></span> <span data-ttu-id="6bc63-116">Crie um método no Gerenciador de buffer para verificar a lista de buffers livres e retornar um ponteiro para que seu aplicativo possa acessar os buffers quando necessário.</span><span class="sxs-lookup"><span data-stu-id="6bc63-116">Create a method in your buffer manager to check the list of free buffers and return a pointer so that your application can access buffers when needed.</span></span> <span data-ttu-id="6bc63-117">Esse método deve criar novos buffers conforme necessário e adicioná-los à lista.</span><span class="sxs-lookup"><span data-stu-id="6bc63-117">This method should create new buffers as needed and add them to the list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bc63-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6bc63-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bc63-119">Trabalhando com codec DMOs</span><span class="sxs-lookup"><span data-stu-id="6bc63-119">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
