---
description: AVX (extensões de vetor avançado) da Intel é uma extensão de vetor de ponto flutuante de 256 bits da arquitetura Intel. Ele inclui extensões para os conjuntos de instruções e de registro.
ms.assetid: 76357e08-a53c-4490-b08d-1c26900a3826
title: Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 454c8bd5090463cefa1b0ff3a27ef7a04787db0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370348"
---
# <a name="intel-avx"></a><span data-ttu-id="f8095-104">Intel AVX</span><span class="sxs-lookup"><span data-stu-id="f8095-104">Intel AVX</span></span>

## <a name="purpose"></a><span data-ttu-id="f8095-105">Finalidade</span><span class="sxs-lookup"><span data-stu-id="f8095-105">Purpose</span></span>

<span data-ttu-id="f8095-106">AVX (extensões de vetor avançado) da Intel é uma extensão de vetor de ponto flutuante de 256 bits da arquitetura Intel.</span><span class="sxs-lookup"><span data-stu-id="f8095-106">Intel Advanced Vector Extensions (AVX) is a 256-bit SIMD floating point vector extension of Intel architecture.</span></span> <span data-ttu-id="f8095-107">Ele inclui extensões para os conjuntos de instruções e de registro.</span><span class="sxs-lookup"><span data-stu-id="f8095-107">It includes extensions to both instruction and register sets.</span></span>

<span data-ttu-id="f8095-108">A Microsoft desenvolveu alguns aprimoramentos de API, como o XState functions, que permitem que os aplicativos acessem e manipulem informações e estado do recurso do processador estendido, incluindo o Intel AVX.</span><span class="sxs-lookup"><span data-stu-id="f8095-108">Microsoft has developed some API enhancements, such as XState functions, that enable applications to access and manipulate extended processor feature information and state, including Intel AVX.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f8095-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f8095-109">In this section</span></span>



| <span data-ttu-id="f8095-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="f8095-110">Topic</span></span>                                                                     | <span data-ttu-id="f8095-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f8095-111">Description</span></span>                                                                                                                                               |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8095-112">Trabalhando com o contexto XState</span><span class="sxs-lookup"><span data-stu-id="f8095-112">Working with XState Context</span></span>](working-with-xstate-context.md)<br/> | <span data-ttu-id="f8095-113">Este documento contém um exemplo que demonstra como usar as funções de contexto XState para recuperar e definir recursos estendidos em um thread.</span><span class="sxs-lookup"><span data-stu-id="f8095-113">This document contains an example that demonstrates how to use the XState context functions to retrieve and set extended features on a thread.</span></span><br/> |
| [<span data-ttu-id="f8095-114">Funções AVX</span><span class="sxs-lookup"><span data-stu-id="f8095-114">AVX Functions</span></span>](avx-functions.md)<br/>                             | <span data-ttu-id="f8095-115">Funções do Intel AVX</span><span class="sxs-lookup"><span data-stu-id="f8095-115">Intel AVX functions</span></span><br/>                                                                                                                            |



 

## <a name="developer-audience"></a><span data-ttu-id="f8095-116">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="f8095-116">Developer audience</span></span>

<span data-ttu-id="f8095-117">O Intel AVX foi projetado para uso por aplicativos que são intensivamente de computação de ponto flutuante e podem ser vetorizados.</span><span class="sxs-lookup"><span data-stu-id="f8095-117">Intel AVX is designed for use by applications that are strongly floating point compute intensive and can be vectorized.</span></span> <span data-ttu-id="f8095-118">Aplicativos de exemplo incluem processamento de áudio e codecs de áudio, aplicativos de edição de imagens e vídeos, análise de serviços financeiros e software de modelagem, além de software de fabricação e engenharia.</span><span class="sxs-lookup"><span data-stu-id="f8095-118">Example applications include audio processing and audio codecs, image and video editing applications, financial services analysis and modeling software, and manufacturing and engineering software.</span></span>

 

 




