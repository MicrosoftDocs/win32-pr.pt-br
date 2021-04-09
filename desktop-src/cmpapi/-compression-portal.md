---
description: .
ms.assetid: 3ef35cd0-3742-4fc2-9c06-e0485d3538f2
title: API de compactação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e23493310643ad83dc476c31c094dfe336f910f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089584"
---
# <a name="compression-api"></a><span data-ttu-id="58c12-103">API de compactação</span><span class="sxs-lookup"><span data-stu-id="58c12-103">Compression API</span></span>

## <a name="purpose"></a><span data-ttu-id="58c12-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="58c12-104">Purpose</span></span>

<span data-ttu-id="58c12-105">A API de compactação expõe os algoritmos de compactação Windows MSZIP, XPRESS, XPRESS \_ Huff e LZMS.</span><span class="sxs-lookup"><span data-stu-id="58c12-105">The Compression API exposes the Windows MSZIP, XPRESS, XPRESS\_HUFF, and LZMS compression algorithms.</span></span> <span data-ttu-id="58c12-106">Isso permite que os desenvolvedores de aplicativos do Windows gerenciem versões, serviços e estendam os algoritmos de compactação expostos.</span><span class="sxs-lookup"><span data-stu-id="58c12-106">This enables developers of Windows applications to manage versions, service, and extend the exposed compression algorithms.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="58c12-107">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="58c12-107">Developer audience</span></span>

<span data-ttu-id="58c12-108">A API de compactação foi projetada para uso por desenvolvedores profissionais C/C++ de aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="58c12-108">The Compression API is designed for use by professional C/C++ developers of Windows applications.</span></span> <span data-ttu-id="58c12-109">A API de compactação expõe os algoritmos de compactação sem perdas usados pelo Windows por meio de uma interface pública e uma API de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="58c12-109">The Compression API exposes the lossless compression algorithms used by Windows though a public interface and user-mode API.</span></span> <span data-ttu-id="58c12-110">A API de compactação é o método recomendado para que os desenvolvedores do Windows controlem os algoritmos de compactação.</span><span class="sxs-lookup"><span data-stu-id="58c12-110">The Compression API is the recommended method for Windows developers to control the compression algorithms.</span></span> <span data-ttu-id="58c12-111">Esse recurso é de 64 bits em Windows de 64 bits e 32 bits no Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="58c12-111">This feature is 64-bit on 64-bit Windows and 32-bit on 32-bit Windows.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="58c12-112">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="58c12-112">Run-time requirements</span></span>

<span data-ttu-id="58c12-113">A API de compactação está disponível a partir do Windows 8 ou do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="58c12-113">The Compression API is available beginning with the Windows 8 or Windows Server 2012.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="58c12-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="58c12-114">In this section</span></span>

-   [<span data-ttu-id="58c12-115">Usando a API de compactação</span><span class="sxs-lookup"><span data-stu-id="58c12-115">Using the Compression API</span></span>](using-the-compression-api.md)
-   [<span data-ttu-id="58c12-116">Funções de API de compactação</span><span class="sxs-lookup"><span data-stu-id="58c12-116">Compression API Functions</span></span>](compression-api-functions.md)
-   [<span data-ttu-id="58c12-117">Estruturas de API de compactação</span><span class="sxs-lookup"><span data-stu-id="58c12-117">Compression API Structures</span></span>](compression-api-structures.md)
-   [<span data-ttu-id="58c12-118">Enumerações de API de compactação</span><span class="sxs-lookup"><span data-stu-id="58c12-118">Compression API Enumerations</span></span>](compression-api-enumerations.md)

 

 



