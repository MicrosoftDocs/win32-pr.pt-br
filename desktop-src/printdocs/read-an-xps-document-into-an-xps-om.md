---
description: Descreve como ler um documento XPS existente de um arquivo em um OM XPS.
ms.assetid: 92a8d19f-1c9e-4e02-a3d4-f2869ec871df
title: Ler um documento XPS em um OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c3b703de24be58db875618b575cebf9c1c0b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297293"
---
# <a name="read-an-xps-document-into-an-xps-om"></a><span data-ttu-id="47d5c-103">Ler um documento XPS em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="47d5c-103">Read an XPS Document into an XPS OM</span></span>

<span data-ttu-id="47d5c-104">Descreve como ler um documento XPS existente de um arquivo em um OM XPS.</span><span class="sxs-lookup"><span data-stu-id="47d5c-104">Describes how to read an existing XPS document from a file into an XPS OM.</span></span>

<span data-ttu-id="47d5c-105">Para criar um OM XPS de um documento XPS, chame o método [**IXpsOMObjectFactory:: CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) .</span><span class="sxs-lookup"><span data-stu-id="47d5c-105">To create an XPS OM from an XPS document, call the [**IXpsOMObjectFactory::CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) method.</span></span>

<span data-ttu-id="47d5c-106">Antes de usar esses exemplos de código em seu programa, leia o aviso de isenção de responsabilidade em [tarefas comuns de programação de documentos XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="47d5c-106">Before using these code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="47d5c-107">Exemplo de código</span><span class="sxs-lookup"><span data-stu-id="47d5c-107">Code Example</span></span>

<span data-ttu-id="47d5c-108">O exemplo de código a seguir pressupõe que a inicialização descrita em [inicializar um om XPS](xps-object-model-initialization.md) tenha sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="47d5c-108">The following code example assumes that the initialization described in [Initialize an XPS OM](xps-object-model-initialization.md) has succeeded.</span></span>


```C++
    IXpsOMPackage *package = NULL;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &package);

    // package now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.

    // When finished with the package, release the object.
    if (NULL != package) package->Release();
```



<span data-ttu-id="47d5c-109">Para criar um OM XPS de um documento XPS que é armazenado como um fluxo, chame [**IXpsOMObjectFactory:: CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).</span><span class="sxs-lookup"><span data-stu-id="47d5c-109">To create an XPS OM from an XPS document that is stored as a stream, call [**IXpsOMObjectFactory::CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).</span></span>

## <a name="remarks"></a><span data-ttu-id="47d5c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="47d5c-110">Remarks</span></span>

<span data-ttu-id="47d5c-111">Se você escrever um OM XPS imediatamente depois de ler um pacote XPS nele, parte do conteúdo original poderá ser perdida ou alterada.</span><span class="sxs-lookup"><span data-stu-id="47d5c-111">If you write an XPS OM immediately after you have read an XPS package into it, some of the original content might be lost or changed.</span></span>

<span data-ttu-id="47d5c-112">Algumas das alterações que podem ocorrer nesse caso são listadas na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="47d5c-112">Some of the changes that can occur in such case are listed in the table that follows:</span></span>

| <span data-ttu-id="47d5c-113">Recurso de documento</span><span class="sxs-lookup"><span data-stu-id="47d5c-113">Document feature</span></span>                      | <span data-ttu-id="47d5c-114">Ação</span><span class="sxs-lookup"><span data-stu-id="47d5c-114">Action</span></span>                                                             |
|---------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="47d5c-115">Assinaturas digitais</span><span class="sxs-lookup"><span data-stu-id="47d5c-115">Digital signatures</span></span><br/>         | <span data-ttu-id="47d5c-116">Removido do documento</span><span class="sxs-lookup"><span data-stu-id="47d5c-116">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="47d5c-117">Parte DiscardControl</span><span class="sxs-lookup"><span data-stu-id="47d5c-117">DiscardControl part</span></span><br/>        | <span data-ttu-id="47d5c-118">Removido do documento</span><span class="sxs-lookup"><span data-stu-id="47d5c-118">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="47d5c-119">Partes do documento estrangeiro</span><span class="sxs-lookup"><span data-stu-id="47d5c-119">Foreign document parts</span></span><br/>     | <span data-ttu-id="47d5c-120">Removido do documento</span><span class="sxs-lookup"><span data-stu-id="47d5c-120">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="47d5c-121">Marcação FixedPage</span><span class="sxs-lookup"><span data-stu-id="47d5c-121">FixedPage markup</span></span><br/>           | <span data-ttu-id="47d5c-122">Modificado a partir do original</span><span class="sxs-lookup"><span data-stu-id="47d5c-122">Modified from the original</span></span><br/>                              |
| <span data-ttu-id="47d5c-123">Marcação do dicionário de recursos</span><span class="sxs-lookup"><span data-stu-id="47d5c-123">Resource dictionary markup</span></span><br/> | <span data-ttu-id="47d5c-124">Modificado a partir do original, se o sinalizador de otimização estiver definido</span><span class="sxs-lookup"><span data-stu-id="47d5c-124">Modified from the original, if Optimization flag is set</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="47d5c-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="47d5c-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="47d5c-126">**Próximas etapas**</span><span class="sxs-lookup"><span data-stu-id="47d5c-126">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="47d5c-127">Navegar no OM XPS</span><span class="sxs-lookup"><span data-stu-id="47d5c-127">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="47d5c-128">Gravar texto em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="47d5c-128">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="47d5c-129">Desenhar gráficos em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="47d5c-129">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="47d5c-130">Coloque as imagens em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="47d5c-130">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="47d5c-131">**Usado nesta seção**</span><span class="sxs-lookup"><span data-stu-id="47d5c-131">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="47d5c-132">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="47d5c-132">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="47d5c-133">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="47d5c-133">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

<span data-ttu-id="47d5c-134">**Para obter mais informações**</span><span class="sxs-lookup"><span data-stu-id="47d5c-134">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="47d5c-135">Inicializar um OM XPS</span><span class="sxs-lookup"><span data-stu-id="47d5c-135">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="47d5c-136">API de empacotamento</span><span class="sxs-lookup"><span data-stu-id="47d5c-136">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="47d5c-137">Referência da API do documento XPS</span><span class="sxs-lookup"><span data-stu-id="47d5c-137">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="47d5c-138">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="47d5c-138">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

