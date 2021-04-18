---
description: Esta seção detalha a versão binária do formato de arquivo DirectX (. x), conforme introduzido com o lançamento do DirectX 3,0.
ms.assetid: d1b6698f-72bd-40a4-a501-c2093cd940f6
title: Codificação binária
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56937b54be82e36d6ff18aab2a2349be6d59cc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814390"
---
# <a name="binary-encoding"></a><span data-ttu-id="976ac-103">Codificação binária</span><span class="sxs-lookup"><span data-stu-id="976ac-103">Binary Encoding</span></span>

<span data-ttu-id="976ac-104">Esta seção detalha a versão binária do formato de arquivo DirectX (. x), conforme introduzido com o lançamento do DirectX 3,0.</span><span class="sxs-lookup"><span data-stu-id="976ac-104">This section details the binary version of the DirectX (.x) file format as introduced with the release of DirectX 3.0.</span></span>

<span data-ttu-id="976ac-105">O formato binário é uma representação indexada do formato de texto.</span><span class="sxs-lookup"><span data-stu-id="976ac-105">The binary format is a tokenized representation of the text format.</span></span> <span data-ttu-id="976ac-106">Os tokens podem ser autônomos ou acompanhados por registros de dados primitivos.</span><span class="sxs-lookup"><span data-stu-id="976ac-106">Tokens can be stand-alone or accompanied by primitive data records.</span></span> <span data-ttu-id="976ac-107">Tokens autônomos fornecem estrutura gramatical e tokens de registro fornecem os dados necessários.</span><span class="sxs-lookup"><span data-stu-id="976ac-107">Stand-alone tokens give grammatical structure, and record-bearing tokens supply the necessary data.</span></span>

<span data-ttu-id="976ac-108">Observe que todos os dados são armazenados no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="976ac-108">Note that all data is stored in little-endian format.</span></span> <span data-ttu-id="976ac-109">Um fluxo de dados binários válido consiste em um cabeçalho seguido por modelos e/ou objetos de dados.</span><span class="sxs-lookup"><span data-stu-id="976ac-109">A valid binary data stream consists of a header followed by templates and/or data objects.</span></span>

<span data-ttu-id="976ac-110">Esta seção aborda os seguintes componentes do formato de arquivo binário e fornece um modelo de exemplo e um objeto de dados binários.</span><span class="sxs-lookup"><span data-stu-id="976ac-110">This section discusses the following components of the binary file format and provides an example template and binary data object.</span></span>

-   [<span data-ttu-id="976ac-111">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="976ac-111">Header</span></span>](header.md)
-   [<span data-ttu-id="976ac-112">Token</span><span class="sxs-lookup"><span data-stu-id="976ac-112">Tokens</span></span>](tokens.md)
-   [<span data-ttu-id="976ac-113">Registros de token</span><span class="sxs-lookup"><span data-stu-id="976ac-113">Token Records</span></span>](token-records.md)
-   [<span data-ttu-id="976ac-114">Modelos</span><span class="sxs-lookup"><span data-stu-id="976ac-114">Templates</span></span>](dx9-graphics-reference-x-file-binaryencoding-templates.md)
-   [<span data-ttu-id="976ac-115">Dados</span><span class="sxs-lookup"><span data-stu-id="976ac-115">Data</span></span>](dx9-graphics-reference-x-file-binaryencoding-data.md)
-   [<span data-ttu-id="976ac-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="976ac-116">Examples</span></span>](examples.md)

## <a name="related-topics"></a><span data-ttu-id="976ac-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="976ac-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="976ac-118">X referência de formato de arquivo</span><span class="sxs-lookup"><span data-stu-id="976ac-118">X File Format Reference</span></span>](dx9-graphics-reference-x-file-format.md)
</dt> </dl>

 

 



