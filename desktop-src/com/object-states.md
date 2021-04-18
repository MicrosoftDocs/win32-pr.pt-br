---
title: Estados de objeto
description: Estados de objeto
ms.assetid: 8ebef6d6-7a2f-4b95-91ca-999646cde82d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268b9bc9c69009850a5172259ab7a13c760d2c72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813583"
---
# <a name="object-states"></a><span data-ttu-id="0d1d4-103">Estados de objeto</span><span class="sxs-lookup"><span data-stu-id="0d1d4-103">Object States</span></span>

<span data-ttu-id="0d1d4-104">Um objeto composto existe em um dos três Estados: passivo, carregado ou em execução.</span><span class="sxs-lookup"><span data-stu-id="0d1d4-104">A compound object exists in one of three states: passive, loaded, or running.</span></span> <span data-ttu-id="0d1d4-105">Um estado de objeto de documento composto descreve a relação entre o objeto em seu contêiner e o aplicativo responsável por sua criação.</span><span class="sxs-lookup"><span data-stu-id="0d1d4-105">A compound-document object's state describes the relationship between the object in its container and the application responsible for its creation.</span></span> <span data-ttu-id="0d1d4-106">A tabela a seguir resume esses Estados.</span><span class="sxs-lookup"><span data-stu-id="0d1d4-106">The following table summarizes these states.</span></span>



| <span data-ttu-id="0d1d4-107">Estado de objeto</span><span class="sxs-lookup"><span data-stu-id="0d1d4-107">Object state</span></span>       | <span data-ttu-id="0d1d4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d1d4-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d1d4-109">Passivo</span><span class="sxs-lookup"><span data-stu-id="0d1d4-109">Passive</span></span><br/> | <span data-ttu-id="0d1d4-110">O objeto de documento composto existe somente no armazenamento, seja no disco ou em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0d1d4-110">The compound-document object exists only in storage, either on disk or in a database.</span></span> <span data-ttu-id="0d1d4-111">Nesse estado, o objeto não está disponível para exibição ou edição.</span><span class="sxs-lookup"><span data-stu-id="0d1d4-111">In this state, the object is unavailable for viewing or editing.</span></span><br/>                                                                                                                                                                                                                                   |
| <span data-ttu-id="0d1d4-112">Carregado</span><span class="sxs-lookup"><span data-stu-id="0d1d4-112">Loaded</span></span><br/>  | <span data-ttu-id="0d1d4-113">As estruturas de dados do objeto criadas pelo manipulador de objetos estão na memória do contêiner.</span><span class="sxs-lookup"><span data-stu-id="0d1d4-113">The object's data structures created by the object handler are in the container's memory.</span></span> <span data-ttu-id="0d1d4-114">O contêiner estabeleceu comunicação com o manipulador de objetos e há dados de apresentação em cache disponíveis para renderizar o objeto.</span><span class="sxs-lookup"><span data-stu-id="0d1d4-114">The container has established communication with the object handler and there is cached presentation data available for rendering the object.</span></span> <span data-ttu-id="0d1d4-115">As chamadas são processadas pelo manipulador de objetos.</span><span class="sxs-lookup"><span data-stu-id="0d1d4-115">Calls are processed by the object handler.</span></span> <span data-ttu-id="0d1d4-116">Esse Estado, devido à baixa sobrecarga, é usado quando um usuário está simplesmente exibindo ou imprimindo um objeto.</span><span class="sxs-lookup"><span data-stu-id="0d1d4-116">This state, because of its low overhead, is used when a user is simply viewing or printing an object.</span></span><br/> |
| <span data-ttu-id="0d1d4-117">Executando</span><span class="sxs-lookup"><span data-stu-id="0d1d4-117">Running</span></span><br/> | <span data-ttu-id="0d1d4-118">Os objetos que controlam a comunicação remota foram criados e o aplicativo do servidor OLE está em execução.</span><span class="sxs-lookup"><span data-stu-id="0d1d4-118">The objects that control remoting have been created and the OLE server application is running.</span></span> <span data-ttu-id="0d1d4-119">As interfaces do objeto são acessíveis e o contêiner pode receber a notificação de alterações.</span><span class="sxs-lookup"><span data-stu-id="0d1d4-119">The object's interfaces are accessible, and the container can receive notification of changes.</span></span> <span data-ttu-id="0d1d4-120">Nesse estado, um usuário final pode editar ou, de outra forma, manipular o objeto.</span><span class="sxs-lookup"><span data-stu-id="0d1d4-120">In this state, an end user can edit or otherwise manipulate the object.</span></span><br/>                                                                                                                    |



 

<span data-ttu-id="0d1d4-121">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="0d1d4-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="0d1d4-122">Inserindo o estado carregado</span><span class="sxs-lookup"><span data-stu-id="0d1d4-122">Entering the Loaded State</span></span>](entering-the-loaded-state.md)
-   [<span data-ttu-id="0d1d4-123">Entrando no estado de execução</span><span class="sxs-lookup"><span data-stu-id="0d1d4-123">Entering the Running State</span></span>](entering-the-running-state.md)
-   [<span data-ttu-id="0d1d4-124">Inserindo o estado passivo</span><span class="sxs-lookup"><span data-stu-id="0d1d4-124">Entering the Passive State</span></span>](entering-the-passive-state.md)

## <a name="related-topics"></a><span data-ttu-id="0d1d4-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d1d4-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d1d4-126">Documentos compostos</span><span class="sxs-lookup"><span data-stu-id="0d1d4-126">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 





