---
title: Copiando dados de um arquivo para outro
description: Copiando dados de um arquivo para outro
ms.assetid: 1403c396-46ea-48b1-a535-922ffca31bc2
keywords:
- SDK do Windows Media Format, copiando dados
- ASF (Advanced Systems Format), copiando dados
- ASF (formato de sistemas avançados), copiando dados
- fluxos, copiando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b38a1675ac79630371fe4d3fda66d44b4b2990
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916565"
---
# <a name="copying-data-from-one-file-to-another"></a><span data-ttu-id="eb377-107">Copiando dados de um arquivo para outro</span><span class="sxs-lookup"><span data-stu-id="eb377-107">Copying Data from One File to Another</span></span>

<span data-ttu-id="eb377-108">No nível mais básico, a cópia de um fluxo de um arquivo ASF para outro é bastante simples.</span><span class="sxs-lookup"><span data-stu-id="eb377-108">At the most basic level, copying a stream from one ASF file to another is fairly straightforward.</span></span> <span data-ttu-id="eb377-109">No entanto, há problemas a serem considerados ao trabalhar com fluxos de vários arquivos de entrada ou ao copiar fluxos que você primeiro descompactar e codificar novamente.</span><span class="sxs-lookup"><span data-stu-id="eb377-109">However, there are issues to consider when working with streams from multiple input files or when copying streams that you first decompress and re-encode.</span></span>

<span data-ttu-id="eb377-110">As seções a seguir descrevem a cópia de fluxos.</span><span class="sxs-lookup"><span data-stu-id="eb377-110">The following sections describe copying streams.</span></span>



| <span data-ttu-id="eb377-111">Seção</span><span class="sxs-lookup"><span data-stu-id="eb377-111">Section</span></span>                                                                                              | <span data-ttu-id="eb377-112">Descripiton</span><span class="sxs-lookup"><span data-stu-id="eb377-112">Descripiton</span></span>                                                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb377-113">Copiando fluxos sem descompactar os dados</span><span class="sxs-lookup"><span data-stu-id="eb377-113">Copying Streams Without Decompressing the Data</span></span>](copying-streams-without-decompressing-the-data.md) | <span data-ttu-id="eb377-114">Descreve como copiar fluxos usando amostras compactadas para preservar a qualidade do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="eb377-114">Describes how to copy streams using compressed samples to preserve the quality of the content.</span></span> |
| [<span data-ttu-id="eb377-115">Copiando fluxos usando amostras descompactadas</span><span class="sxs-lookup"><span data-stu-id="eb377-115">Copying Streams Using Decompressed Samples</span></span>](copying-streams-using-decompressed-samples.md)         | <span data-ttu-id="eb377-116">Descreve as dificuldades na cópia de fluxos usando amostras descompactadas.</span><span class="sxs-lookup"><span data-stu-id="eb377-116">Describes the difficulties in copying streams using decompressed samples.</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="eb377-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eb377-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb377-118">**Objeto do gerenciador de perfis**</span><span class="sxs-lookup"><span data-stu-id="eb377-118">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="eb377-119">**Objeto de configuração de fluxo**</span><span class="sxs-lookup"><span data-stu-id="eb377-119">**Stream Configuration Object**</span></span>](stream-configuration-object.md)
</dt> <dt>

[<span data-ttu-id="eb377-120">**Objeto de leitor síncrono**</span><span class="sxs-lookup"><span data-stu-id="eb377-120">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> <dt>

[<span data-ttu-id="eb377-121">**Objeto do gravador**</span><span class="sxs-lookup"><span data-stu-id="eb377-121">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




