---
title: Armazenamentos e fluxos
description: Um objeto de armazenamento é análogo a um diretório do sistema de arquivos.
ms.assetid: 57b2a66d-e912-4879-b778-75f8461d211f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebc44a22779b4ae63ee7c39b55888d2ea23579f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635186"
---
# <a name="storages-and-streams"></a><span data-ttu-id="f5ce7-103">Armazenamentos e fluxos</span><span class="sxs-lookup"><span data-stu-id="f5ce7-103">Storages and Streams</span></span>

<span data-ttu-id="f5ce7-104">Um objeto de armazenamento é análogo a um diretório do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f5ce7-104">A storage object is analogous to a file system directory.</span></span> <span data-ttu-id="f5ce7-105">Assim como um diretório pode conter outros diretórios e arquivos, um objeto de armazenamento pode conter outros objetos de armazenamento e objetos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="f5ce7-105">Just as a directory can contain other directories and files, a storage object can contain other storage objects and stream objects.</span></span> <span data-ttu-id="f5ce7-106">Também como um diretório, um objeto de armazenamento controla os locais e os tamanhos dos objetos de armazenamento e os objetos de fluxo aninhados abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="f5ce7-106">Also like a directory, a storage object tracks the locations and sizes of the storage objects and stream objects nested beneath it.</span></span>

<span data-ttu-id="f5ce7-107">Um objeto de fluxo é análogo à noção tradicional de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f5ce7-107">A stream object is analogous to the traditional notion of a file.</span></span> <span data-ttu-id="f5ce7-108">Como um arquivo, um fluxo contém dados armazenados como uma sequência consecutiva de bytes.</span><span class="sxs-lookup"><span data-stu-id="f5ce7-108">Like a file, a stream contains data stored as a consecutive sequence of bytes.</span></span>

<span data-ttu-id="f5ce7-109">Um arquivo composto COM consiste em um objeto de armazenamento raiz contendo pelo menos um objeto de fluxo representando seus dados nativos junto com um ou mais objetos de armazenamento correspondentes aos seus objetos vinculados e incorporados.</span><span class="sxs-lookup"><span data-stu-id="f5ce7-109">A COM compound file consists of a root storage object containing at least one stream object representing its native data along with one or more storage objects corresponding to its linked and embedded objects.</span></span> <span data-ttu-id="f5ce7-110">O objeto de armazenamento raiz é mapeado para um nome de arquivo em qualquer sistema de arquivos que ele esteja residindo.</span><span class="sxs-lookup"><span data-stu-id="f5ce7-110">The root storage object maps to a file name in whatever file system it happens to reside.</span></span> <span data-ttu-id="f5ce7-111">Cada um dos objetos dentro do documento também é representado por um objeto de armazenamento que contém um ou mais objetos Stream, e talvez também contenha um ou mais objetos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f5ce7-111">Each of the objects inside the document also is represented by a storage object containing one or more stream objects, and perhaps also containing one or more storage objects.</span></span> <span data-ttu-id="f5ce7-112">Dessa forma, um documento pode consistir em um número ilimitado de objetos aninhados.</span><span class="sxs-lookup"><span data-stu-id="f5ce7-112">In this way, a document can consist of an unlimited number of nested objects.</span></span> <span data-ttu-id="f5ce7-113">Para obter mais informações, consulte [arquivos compostos](compound-files.md).</span><span class="sxs-lookup"><span data-stu-id="f5ce7-113">For more information, see [Compound Files](compound-files.md).</span></span>

 

 




