---
description: O formato de arquivo X se refere a arquivos com a extensão de nome de arquivo. X.
ms.assetid: 06b3dcb3-03fc-4d99-b8c3-32f56d8bf49e
title: Arquivos X (herdados) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0e4ce85a0ff5ecbc2f680f55b8162d13bc1042
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825597"
---
# <a name="x-files-legacy-direct3d-9"></a><span data-ttu-id="bc74c-103">Arquivos X (herdados) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bc74c-103">X Files (Legacy) (Direct3D 9)</span></span>

<span data-ttu-id="bc74c-104">O formato de arquivo X se refere a arquivos com a extensão de nome de arquivo. X.</span><span class="sxs-lookup"><span data-stu-id="bc74c-104">The X file format refers to files with the .x file name extension.</span></span> <span data-ttu-id="bc74c-105">Os arquivos X foram introduzidos com o DirectX 2,0.</span><span class="sxs-lookup"><span data-stu-id="bc74c-105">X files were introduced with DirectX 2.0.</span></span> <span data-ttu-id="bc74c-106">Uma versão binária desse formato foi posteriormente liberada com o DirectX 3,0, que também está descrito nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="bc74c-106">A binary version of this format was subsequently released with DirectX 3.0, which is also described in this documentation.</span></span> <span data-ttu-id="bc74c-107">O DirectX 6,0 introduziu interfaces e métodos que permitem ler e gravar em arquivos. x.</span><span class="sxs-lookup"><span data-stu-id="bc74c-107">DirectX 6.0 introduced interfaces and methods that enable reading from and writing to .x files.</span></span>

<span data-ttu-id="bc74c-108">Os arquivos X fornecem um formato controlado por modelo que permite o armazenamento de malhas, texturas, animações e objetos definíveis pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="bc74c-108">X files provide a template-driven format that enables the storage of meshes, textures, animations, and user-definable objects.</span></span> <span data-ttu-id="bc74c-109">O suporte para conjuntos de animação permite que você armazene caminhos predefinidos para reprodução em tempo real.</span><span class="sxs-lookup"><span data-stu-id="bc74c-109">Support for animation sets enables you to store predefined paths for playback in real time.</span></span> <span data-ttu-id="bc74c-110">Também há suporte para instanciações e hierarquias.</span><span class="sxs-lookup"><span data-stu-id="bc74c-110">Instancing and hierarchies are also supported.</span></span> <span data-ttu-id="bc74c-111">A instanciação permite várias referências a um objeto, como uma malha, enquanto armazena seus dados somente uma vez por arquivo.</span><span class="sxs-lookup"><span data-stu-id="bc74c-111">Instancing enables multiple references to an object, such as a mesh, while storing its data only once per file.</span></span> <span data-ttu-id="bc74c-112">As hierarquias são usadas para expressar relações entre registros de dados.</span><span class="sxs-lookup"><span data-stu-id="bc74c-112">Hierarchies are used to express relationships between data records.</span></span>

<span data-ttu-id="bc74c-113">O formato de arquivo. x fornece primitivos de dados de baixo nível nos quais os aplicativos definem primitivos de nível superior por meio de modelos.</span><span class="sxs-lookup"><span data-stu-id="bc74c-113">The .x file format provides low-level data primitives on which applications define higher-level primitives through templates.</span></span>

<span data-ttu-id="bc74c-114">Modelos tridimensionais criados em aplicativos Maya de 3ds Max ou alias \| Wavefront podem ser convertidos em arquivos. x com as extensões do DirectX para Alias Maya.</span><span class="sxs-lookup"><span data-stu-id="bc74c-114">Three-dimensional models created in Discreet's 3ds max or Alias\|Wavefront's Maya applications can be converted to .x files with the DirectX Extensions for Alias Maya.</span></span>

<span data-ttu-id="bc74c-115">Esta seção descreve a estrutura de arquivos. x e como usá-los em seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="bc74c-115">This section describes the structure of .x files and how to use them in your applications.</span></span> <span data-ttu-id="bc74c-116">As informações são divididas nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="bc74c-116">Information is divided into the following topics.</span></span>

-   [<span data-ttu-id="bc74c-117">Carregando um arquivo X (Herdado) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bc74c-117">Loading an X File (Legacy) (Direct3D 9)</span></span>](loading-an-x-file--legacy-.md)
-   [<span data-ttu-id="bc74c-118">Salvando em um arquivo X (Herdado) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bc74c-118">Saving to an X File (Legacy) (Direct3D 9)</span></span>](saving-to-an-x-file--legacy-.md)
-   [<span data-ttu-id="bc74c-119">Definindo um cubo simples (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bc74c-119">Defining a Simple Cube (Direct3D 9)</span></span>](defining-a-simple-cube.md)
-   [<span data-ttu-id="bc74c-120">Adicionando texturas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bc74c-120">Adding Textures (Direct3D 9)</span></span>](adding-textures.md)
-   [<span data-ttu-id="bc74c-121">Adicionando quadros e animações (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bc74c-121">Adding Frames and Animations (Direct3D 9)</span></span>](adding-frames-and-animations.md)

<span data-ttu-id="bc74c-122">Para obter mais informações sobre o formato de arquivo. x, consulte [x file Reference](dx9-graphics-reference-d3dx-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="bc74c-122">For more information about the .x file format, see [X File Reference](dx9-graphics-reference-d3dx-x-file.md).</span></span>

<span data-ttu-id="bc74c-123">Para obter mais informações sobre a API de arquivo. x, consulte [x file Reference (legacy)](dx9-graphics-reference-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="bc74c-123">For more information about the .x file API, see [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc74c-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc74c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc74c-125">Introdução</span><span class="sxs-lookup"><span data-stu-id="bc74c-125">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



