---
title: Usando o manifesto de transferência
description: O assistente de publicação na Web e o assistente de pedido de impressão online usam o manifesto de transferência para comunicar detalhes de transferência de dados entre o computador cliente e o site do servidor.
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Assistente de publicação na Web, transferir manifesto
- Assistente de ordenação de impressão online, transferir manifesto
- transferir manifesto
- manifest
- janela. external, transferir manifesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fa7b3a35a6f06e2939b6c25f82d12c2b98a7f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823758"
---
# <a name="using-the-transfer-manifest"></a><span data-ttu-id="a725d-108">Usando o manifesto de transferência</span><span class="sxs-lookup"><span data-stu-id="a725d-108">Using the Transfer Manifest</span></span>

<span data-ttu-id="a725d-109">O assistente de publicação na Web e o assistente de pedido de impressão online usam o manifesto de transferência para comunicar detalhes de transferência de dados entre o computador cliente e o site do servidor.</span><span class="sxs-lookup"><span data-stu-id="a725d-109">The Web Publishing Wizard and Online Print Ordering Wizard use the transfer manifest to communicate details of data transfer between the client computer and the server site.</span></span>

## <a name="the-purpose-of-the-transfer-manifest"></a><span data-ttu-id="a725d-110">A finalidade do manifesto de transferência</span><span class="sxs-lookup"><span data-stu-id="a725d-110">The Purpose of the Transfer Manifest</span></span>

<span data-ttu-id="a725d-111">O manifesto de transferência descreve os arquivos envolvidos na transferência, incluindo detalhes como a hierarquia de destino e os metadados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="a725d-111">The transfer manifest describes files involved in the transfer, including details such as the destination hierarchy and the file's metadata.</span></span> <span data-ttu-id="a725d-112">O script do lado do servidor pode modificar o manifesto removendo arquivos inadequados da lista e adicionando informações sobre como e onde os arquivos devem ser transferidos.</span><span class="sxs-lookup"><span data-stu-id="a725d-112">Server-side script can modify the manifest by removing inappropriate files from the list and adding information about how and where the files should be transferred.</span></span>

<span data-ttu-id="a725d-113">O manifesto é exposto como a propriedade **Window. external. Property ("TransferManifest")**, um documento XML modelo de objeto do documento (dom).</span><span class="sxs-lookup"><span data-stu-id="a725d-113">The manifest is exposed as the property **window.external.Property("TransferManifest")**, an XML Document Object Model (DOM) document.</span></span> <span data-ttu-id="a725d-114">Para obter mais informações sobre o XML DOM, consulte a documentação do MSDN para [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a725d-114">For more information on the XML DOM, see the MSDN documentation for [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).</span></span>

<span data-ttu-id="a725d-115">A organização de nível superior do manifesto de transferência é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="a725d-115">The top-level organization of the transfer manifest is as follows:</span></span>


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



<span data-ttu-id="a725d-116">A página HTML do lado do servidor pode usar os nós no manifesto para obter determinadas informações sobre os arquivos a serem copiados e, em seguida, modificar a interface do usuário do serviço de acordo.</span><span class="sxs-lookup"><span data-stu-id="a725d-116">The server-side HTML page can use the nodes in the manifest to obtain certain information about the files to be copied and then modify the service's UI accordingly.</span></span> <span data-ttu-id="a725d-117">Por exemplo, um site de impressão de fotos pode usar as informações para exibir miniaturas das imagens escolhidas, enquanto um site de armazenamento pode usar as informações para garantir que haja espaço de armazenamento suficiente disponível para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="a725d-117">For instance, a photo printing site might use the information to display thumbnails of the chosen images, while a storage site might use the information to ensure that sufficient storage space is available for that user.</span></span> <span data-ttu-id="a725d-118">Para obter informações completas sobre os nós e atributos de manifesto de transferência, consulte [transferir esquema de manifesto](/windows/desktop/shell/interfaces).</span><span class="sxs-lookup"><span data-stu-id="a725d-118">For complete information on the transfer manifest nodes and attributes, see [Transfer Manifest Schema](/windows/desktop/shell/interfaces).</span></span>

<span data-ttu-id="a725d-119">O esquema de manifesto de transferência é gravado como um modelo aberto para que os elementos não definidos especificamente no esquema possam aparecer no manifesto de transferência.</span><span class="sxs-lookup"><span data-stu-id="a725d-119">The transfer manifest schema is written as an open model so that elements not specifically defined in the schema may appear in the transfer manifest.</span></span> <span data-ttu-id="a725d-120">Portanto, um site de provedor pode adicionar elementos proprietários para seu próprio uso sem perturbar a validade do manifesto.</span><span class="sxs-lookup"><span data-stu-id="a725d-120">Therefore, a provider site might add proprietary elements for its own use without disturbing the validity of the manifest.</span></span> <span data-ttu-id="a725d-121">O esquema também é definido para que a ordem dos elementos não seja restrita.</span><span class="sxs-lookup"><span data-stu-id="a725d-121">The schema is also defined so that the order of elements is not restricted.</span></span>

> [!Note]  
> <span data-ttu-id="a725d-122">O manifesto é recriado cada vez que um novo provedor é escolhido para que o provedor tenha a chance de armazenar informações do site no manifesto.</span><span class="sxs-lookup"><span data-stu-id="a725d-122">The manifest is re-created each time a new provider is chosen so that the provider has a chance to store site information in the manifest.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a725d-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a725d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a725d-124">Transferir esquema de manifesto</span><span class="sxs-lookup"><span data-stu-id="a725d-124">Transfer Manifest Schema</span></span>](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 