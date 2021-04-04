---
title: Objetos inseridos (COM)
description: Objetos inseridos
ms.assetid: 1f863fd4-fead-4dd3-b855-8820e015b52a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da9938b17130209fec024f94ee99061ad690693
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085069"
---
# <a name="embedded-objects-com"></a><span data-ttu-id="8da1e-103">Objetos inseridos (COM)</span><span class="sxs-lookup"><span data-stu-id="8da1e-103">Embedded Objects (COM)</span></span>

<span data-ttu-id="8da1e-104">Um objeto incorporado é armazenado fisicamente no documento composto, juntamente com todas as informações necessárias para gerenciar o objeto.</span><span class="sxs-lookup"><span data-stu-id="8da1e-104">An embedded object is physically stored in the compound document, along with all the information needed to manage the object.</span></span> <span data-ttu-id="8da1e-105">Em outras palavras, o objeto incorporado é, na verdade, uma parte do documento composto no qual ele reside.</span><span class="sxs-lookup"><span data-stu-id="8da1e-105">In other words, the embedded object is actually a part of the compound document in which it resides.</span></span> <span data-ttu-id="8da1e-106">Essa organização tem algumas desvantagens.</span><span class="sxs-lookup"><span data-stu-id="8da1e-106">This arrangement has a couple of disadvantages.</span></span> <span data-ttu-id="8da1e-107">Primeiro, um documento composto contendo objetos inseridos será maior que um contendo os mesmos objetos que os links.</span><span class="sxs-lookup"><span data-stu-id="8da1e-107">First, a compound document containing embedded objects will be larger than one containing the same objects as links.</span></span> <span data-ttu-id="8da1e-108">Em segundo lugar, as alterações feitas na origem de um objeto incorporado não serão replicadas automaticamente na cópia inserida, e as alterações na cópia inserida não serão refletidas na origem, pois elas estão com um link.</span><span class="sxs-lookup"><span data-stu-id="8da1e-108">Second, changes made to the source of an embedded object will not be automatically replicated in the embedded copy, and changes in the embedded copy will not be reflected in the source, as they are with a link.</span></span>

<span data-ttu-id="8da1e-109">Ainda assim, para determinadas finalidades, a incorporação oferece várias vantagens em relação aos links.</span><span class="sxs-lookup"><span data-stu-id="8da1e-109">Still, for certain purposes, embedding offers several advantages over links.</span></span> <span data-ttu-id="8da1e-110">Primeiro, os usuários podem transferir documentos compostos com objetos incorporados para outros computadores ou outros locais no mesmo computador, sem quebrar um link.</span><span class="sxs-lookup"><span data-stu-id="8da1e-110">First, users can transfer compound documents with embedded objects to other computers, or other locations on the same computer, without breaking a link.</span></span> <span data-ttu-id="8da1e-111">Em segundo lugar, os usuários podem editar objetos inseridos sem alterar o conteúdo do original.</span><span class="sxs-lookup"><span data-stu-id="8da1e-111">Second, users can edit embedded objects without changing the content of the original.</span></span> <span data-ttu-id="8da1e-112">Às vezes, essa separação é precisamente o que é necessário.</span><span class="sxs-lookup"><span data-stu-id="8da1e-112">Sometimes, this separation is precisely what is required.</span></span> <span data-ttu-id="8da1e-113">Terceiro, os objetos inseridos podem ser ativados em vigor, o que significa que o usuário pode editar ou manipular o objeto sem precisar trabalhar em uma janela separada do contêiner do objeto.</span><span class="sxs-lookup"><span data-stu-id="8da1e-113">Third, embedded objects can be activated in place, meaning that the user can edit or otherwise manipulate the object without having to work in a separate window from that of the object's container.</span></span> <span data-ttu-id="8da1e-114">Em vez disso, quando o objeto é ativado, a interface do usuário do aplicativo de contêiner é alterada para expor essas ferramentas que são necessárias para gerenciar ou modificar o objeto.</span><span class="sxs-lookup"><span data-stu-id="8da1e-114">Instead, when the object is activated, the container application's user interface changes to expose those tools that are necessary to manage or modify the object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8da1e-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8da1e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8da1e-116">Criando objetos vinculados e incorporados de dados existentes</span><span class="sxs-lookup"><span data-stu-id="8da1e-116">Creating Linked and Embedded Objects from Existing Data</span></span>](creating-linked-and-embedded-objects-from-existing-data.md)
</dt> </dl>

 

 




