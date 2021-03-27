---
description: O verificador de tipo de arquivo é uma ferramenta que permite que fornecedores de software independentes (ISVs) verifiquem se seus tipos de arquivo exclusivos são implementados corretamente.
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: Verificador de tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8e4a588e4889241762a9d8e0567d4a4542c0255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828304"
---
# <a name="file-type-verifier"></a><span data-ttu-id="d0f6d-103">Verificador de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="d0f6d-103">File Type Verifier</span></span>

<span data-ttu-id="d0f6d-104">O verificador de tipo de arquivo é uma ferramenta que permite que fornecedores de software independentes (ISVs) verifiquem se seus tipos de arquivo exclusivos são implementados corretamente.</span><span class="sxs-lookup"><span data-stu-id="d0f6d-104">The File Type Verifier is a tool that enables independent software vendors (ISVs) to verify that their unique file types are implemented correctly.</span></span> <span data-ttu-id="d0f6d-105">Implementações de alta qualidade dos manipuladores de tipo de arquivo são cruciais para uma boa experiência de usuário, pois os usuários interagem com o formato de arquivo de várias maneiras no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="d0f6d-105">High quality implementations of your file type handlers are crucial for a good user experience because users interact with your file format in many ways in Windows Explorer.</span></span> <span data-ttu-id="d0f6d-106">Os usuários podem fazer pesquisas de texto completo, classificar por metadados personalizados ou exibir miniaturas e visualizações ricas de seu formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d0f6d-106">Users can do full-text searches, sort by custom metadata, or view rich thumbnails and previews of your file format.</span></span>

<span data-ttu-id="d0f6d-107">Para obter instruções sobre como usar o verificador de tipo de arquivo, consulte [como usar o verificador de tipo de arquivo](how-to-use-the-file-type-verifier.md).</span><span class="sxs-lookup"><span data-stu-id="d0f6d-107">For instructions on using the File Type Verifier, see [How To Use the File Type Verifier](how-to-use-the-file-type-verifier.md).</span></span>

## <a name="about-the-file-type-verifier-tool"></a><span data-ttu-id="d0f6d-108">Sobre a ferramenta de verificação de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="d0f6d-108">About the File Type Verifier Tool</span></span>

<span data-ttu-id="d0f6d-109">O File Type Verifier é um programa que está disponível como parte do [SDK do Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d0f6d-109">File Type Verifier is a program that is available as part of the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d0f6d-110">Ele foi projetado para ajudar os desenvolvedores que criam [tipos de arquivos](fa-file-types.md) personalizados do Windows a detectarem possíveis problemas com seus tipos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d0f6d-110">It is designed to help developers who create custom Windows [File Types](fa-file-types.md) to detect potential issues with their file types.</span></span> <span data-ttu-id="d0f6d-111">Embora o verificador de tipo de arquivo seja executado somente no Windows 7 e posterior, as regras que o verificador de tipo de arquivo impõe aplicam-se a todas as versões do Windows onde os recursos que ele verifica estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d0f6d-111">Although the File Type Verifier runs only on Windows 7 and later, the rules that the File Type Verifier enforces apply to all versions of Windows where the features it checks are available.</span></span>

<span data-ttu-id="d0f6d-112">O verificador de tipo de arquivo executa vários testes no tipo de arquivo para verificar se ele está registrado corretamente e se ele fornece os [manipuladores de tipo de arquivo](fa-file-extensions.md) apropriados para exibir o tipo de arquivo corretamente no Windows Explorer e, quando apropriado, que ele dá suporte à indexação do conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d0f6d-112">The File Type Verifier runs several tests on the file type to verify that it is properly registered, and that it provides the appropriate [File Type Handlers](fa-file-extensions.md) to display the file type properly in Windows Explorer, and when appropriate, that it supports indexing the file content.</span></span>

<span data-ttu-id="d0f6d-113">O verificador de tipo de arquivo testa as seguintes coisas:</span><span class="sxs-lookup"><span data-stu-id="d0f6d-113">The File Type Verifier tests the following things:</span></span>

-   [<span data-ttu-id="d0f6d-114">Gerenciadores de visualização</span><span class="sxs-lookup"><span data-stu-id="d0f6d-114">Preview Handlers</span></span>](building-preview-handlers.md)
-   [<span data-ttu-id="d0f6d-115">Manipuladores de miniatura</span><span class="sxs-lookup"><span data-stu-id="d0f6d-115">Thumbnail Handlers</span></span>](building-thumbnail-providers.md)
-   [<span data-ttu-id="d0f6d-116">Manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="d0f6d-116">Property Handlers</span></span>](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [<span data-ttu-id="d0f6d-117">Manipuladores de verbo</span><span class="sxs-lookup"><span data-stu-id="d0f6d-117">Verb Handlers</span></span>](fa-verbs.md)
-   [<span data-ttu-id="d0f6d-118">Filtros (IFilter)</span><span class="sxs-lookup"><span data-stu-id="d0f6d-118">Filters (IFilter)</span></span>](../search/-search-3x-wds-extidx-filters.md)
-   [<span data-ttu-id="d0f6d-119">Associações de tipo</span><span class="sxs-lookup"><span data-stu-id="d0f6d-119">Kind Associations</span></span>](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="d0f6d-120">Tipos observados</span><span class="sxs-lookup"><span data-stu-id="d0f6d-120">Perceived Types</span></span>](fa-perceivedtypes.md)
-   [<span data-ttu-id="d0f6d-121">Propriedades importantes</span><span class="sxs-lookup"><span data-stu-id="d0f6d-121">Important Properties</span></span>](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a><span data-ttu-id="d0f6d-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0f6d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0f6d-123">Como usar o verificador de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="d0f6d-123">How To Use the File Type Verifier</span></span>](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="d0f6d-124">registro de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="d0f6d-124">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="d0f6d-125">Tipos de arquivo</span><span class="sxs-lookup"><span data-stu-id="d0f6d-125">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="d0f6d-126">Como funcionam as associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="d0f6d-126">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="d0f6d-127">Exibição de conteúdo por tipo de arquivo ou tipo</span><span class="sxs-lookup"><span data-stu-id="d0f6d-127">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="d0f6d-128">Manipuladores de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="d0f6d-128">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="d0f6d-129">Identificadores programáticos</span><span class="sxs-lookup"><span data-stu-id="d0f6d-129">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="d0f6d-130">Tipos observados</span><span class="sxs-lookup"><span data-stu-id="d0f6d-130">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="d0f6d-131">Matrizes de associação</span><span class="sxs-lookup"><span data-stu-id="d0f6d-131">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
