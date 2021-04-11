---
title: Convenções de nomenclatura de objeto de armazenamento
description: Os objetos de armazenamento e fluxo são nomeados de acordo com um conjunto de convenções.
ms.assetid: 72e87c6a-cce5-4456-8336-c657e65c0a34
keywords:
- Armazenamento estruturado Strctd STG, conceitos básicos, convenções de nomenclatura de objeto de armazenamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e828674f4165bdb54dc2ec06748ab4165e75e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363739"
---
# <a name="storage-object-naming-conventions"></a><span data-ttu-id="a2ca6-104">Convenções de nomenclatura de objeto de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a2ca6-104">Storage Object Naming Conventions</span></span>

<span data-ttu-id="a2ca6-105">Os objetos de armazenamento e fluxo são nomeados de acordo com um conjunto de convenções.</span><span class="sxs-lookup"><span data-stu-id="a2ca6-105">Storage and stream objects are named according to a set of conventions.</span></span>

<span data-ttu-id="a2ca6-106">O nome de um objeto de armazenamento raiz é o nome real do arquivo no sistema de arquivos subjacente.</span><span class="sxs-lookup"><span data-stu-id="a2ca6-106">The name of a root storage object is the actual name of the file in the underlying file system.</span></span> <span data-ttu-id="a2ca6-107">Ele está em conformidade com as convenções e restrições que o sistema de arquivos impõe.</span><span class="sxs-lookup"><span data-stu-id="a2ca6-107">It conforms to the conventions and restrictions that the file system imposes.</span></span> <span data-ttu-id="a2ca6-108">As cadeias de caracteres de nome de arquivo passadas para métodos e funções relacionados ao armazenamento são passadas, não interpretadas e inalteradas, para o sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a2ca6-108">File name strings passed to storage-related methods and functions are passed on, uninterpreted and unchanged, to the file system.</span></span>

<span data-ttu-id="a2ca6-109">O nome de um elemento aninhado contido em um objeto de armazenamento é gerenciado pela implementação do objeto de armazenamento específico.</span><span class="sxs-lookup"><span data-stu-id="a2ca6-109">The name of a nested element contained within a storage object is managed by the implementation of the particular storage object.</span></span> <span data-ttu-id="a2ca6-110">Todas as implementações de objetos de armazenamento devem oferecer suporte a nomes de elementos aninhados 32 caracteres de comprimento (incluindo o terminador **nulo** ), embora algumas implementações possam dar suporte a nomes mais longos.</span><span class="sxs-lookup"><span data-stu-id="a2ca6-110">All implementations of storage objects must support nested element names 32 characters in length (including the **NULL** terminator), although some implementations might support longer names.</span></span> <span data-ttu-id="a2ca6-111">Se o objeto de armazenamento faz qualquer conversão de caso é definido pela implementação.</span><span class="sxs-lookup"><span data-stu-id="a2ca6-111">Whether the storage object does any case conversion is implementation-defined.</span></span> <span data-ttu-id="a2ca6-112">Como resultado, os aplicativos que definem nomes de elementos devem escolher nomes que são aceitáveis independentemente de a conversão de maiúsculas e minúsculas ser executada.</span><span class="sxs-lookup"><span data-stu-id="a2ca6-112">As a result, applications that define element names must choose names that are acceptable whether or not case conversion is performed.</span></span> <span data-ttu-id="a2ca6-113">A implementação COM de arquivos compostos dá suporte a nomes com um comprimento máximo de 32 caracteres e não executa nenhuma conversão de maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a2ca6-113">The COM implementation of compound files supports names with a maximum length of 32 characters, and does not perform any case conversion.</span></span>

 

 




