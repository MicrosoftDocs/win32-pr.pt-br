---
title: Criando objetos vinculados e incorporados de dados existentes
description: Criando objetos vinculados e incorporados de dados existentes
ms.assetid: 76848b7e-6068-4bac-9793-304f813096f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f60064516a4312a9de3ce511e00e49ce7276f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637157"
---
# <a name="creating-linked-and-embedded-objects-from-existing-data"></a><span data-ttu-id="c5e0e-103">Criando objetos vinculados e incorporados de dados existentes</span><span class="sxs-lookup"><span data-stu-id="c5e0e-103">Creating Linked and Embedded Objects from Existing Data</span></span>

<span data-ttu-id="c5e0e-104">Normalmente, um usuário monta um documento composto usando a área de transferência ou arrasta e solta para copiar um objeto de dados de seu aplicativo de servidor para o aplicativo de contêiner do usuário.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-104">A user typically assembles a compound document by using either the clipboard or drag and drop to copy a data object from its server application to the user's container application.</span></span> <span data-ttu-id="c5e0e-105">Com aplicativos que dão suporte ao OLE, o usuário pode iniciar a transferência do servidor ou do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-105">With applications that support OLE, the user can initiate the transfer from either the server or the container.</span></span> <span data-ttu-id="c5e0e-106">Por exemplo, o servidor pode copiar dados para a área de transferência no aplicativo de servidor e, em seguida, alternar para o aplicativo de contêiner e escolher colar objeto especial/inserido ou um comando de menu equivalente para criar um novo objeto inserido a partir dos dados selecionados.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-106">For example, the server can copy data to the clipboard in the server application, then switch to the container application and choose Paste Special/Embedded Object or an equivalent menu command to create a new embedded object from the selected data.</span></span> <span data-ttu-id="c5e0e-107">Ou, o usuário pode arrastar os dados de um aplicativo para o outro.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-107">Or, the user can drag the data from one application to the other.</span></span> <span data-ttu-id="c5e0e-108">O processo é semelhante para a criação de um objeto vinculado.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-108">The process is similar for creating a linked object.</span></span>

> [!Note]  
> <span data-ttu-id="c5e0e-109">Um aplicativo que funciona como servidor OLE e contêiner pode usar uma seleção de seus próprios dados para criar um objeto incorporado ou vinculado em um novo local dentro do mesmo documento.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-109">An application that functions as both OLE server and container can use a selection of its own data to create an embedded or linked object at a new location within the same document.</span></span>

 

<span data-ttu-id="c5e0e-110">A transferência de dados entre o servidor OLE e os aplicativos de contêiner é criada na transferência de dados uniforme, conforme descrito em [transferência de dados](data-transfer.md).</span><span class="sxs-lookup"><span data-stu-id="c5e0e-110">Data transfer between OLE server and container applications is built on uniform data transfer, as described in [Data Transfer](data-transfer.md).</span></span> <span data-ttu-id="c5e0e-111">Os servidores OLE e manipuladores de objeto implementam [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) para disponibilizar seus dados para transferências usando a área de transferência ou arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-111">OLE servers and object handlers implement [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) in order to make their data available for transfers using either the clipboard or drag and drop.</span></span> <span data-ttu-id="c5e0e-112">Os objetos OLE dão suporte a todos os formatos de área de transferência usual.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-112">OLE objects support all the usual clipboard formats.</span></span> <span data-ttu-id="c5e0e-113">Além disso, eles dão suporte a seis formatos de área de transferência que dão suporte à criação de objetos vinculados e incorporados de um objeto de dados selecionado.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-113">In addition, they support six clipboard formats that support the creation of linked and embedded objects from a selected data object.</span></span>

<span data-ttu-id="c5e0e-114">Os formatos de área de transferência OLE descrevem os objetos de dados que, ao serem descartados ou colados em contêineres OLE, devem se tornar objetos compostos ou vinculados ao documento composto.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-114">OLE clipboard formats describe data objects that, upon being dropped or pasted in OLE containers, are to become embedded or linked compound-document objects.</span></span> <span data-ttu-id="c5e0e-115">O objeto de dados apresenta esses formatos aos aplicativos de contêiner em ordem de fidelidade como descrições dos dados.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-115">The data object presents these formats to container applications in order of their fidelity as descriptions of the data.</span></span> <span data-ttu-id="c5e0e-116">Em outras palavras, o objeto apresenta primeiro o formato que o representa melhor, seguido pelo seguinte formato melhor e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-116">In other words, the object presents first the format that best represents it, followed by the next best format, and so on.</span></span> <span data-ttu-id="c5e0e-117">Essa ordenação intencional incentiva um aplicativo de contêiner a usar o melhor formato possível.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-117">This intentional ordering encourages a container application to use the best possible format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5e0e-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5e0e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5e0e-119">Documentos compostos</span><span class="sxs-lookup"><span data-stu-id="c5e0e-119">Compound Documents</span></span>](compound-documents.md)
</dt> <dt>

[<span data-ttu-id="c5e0e-120">Transferência de Dados</span><span class="sxs-lookup"><span data-stu-id="c5e0e-120">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 




