---
title: Elemento Reference (preterido)
description: Elemento Reference (preterido)
ms.assetid: 0a549750-abaa-43bf-8420-8fe00eb6feff
keywords:
- Metaarquivos do Windows Media, elemento Reference
- Metafiles, elemento Reference
- elemento Reference
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c521b080609bbe51470a2de960481a86e8264c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105784691"
---
# <a name="reference-element-deprecated"></a><span data-ttu-id="93a20-106">Elemento Reference (preterido)</span><span class="sxs-lookup"><span data-stu-id="93a20-106">reference Element (deprecated)</span></span>

<span data-ttu-id="93a20-107">Este tópico documenta um recurso que não é mais usado na versão atual dos metaarquivos do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="93a20-107">This topic documents a feature that is no longer used in the current version of Windows Media Metafiles.</span></span>

<span data-ttu-id="93a20-108">O elemento **Reference** contém uma lista de referências a URLs.</span><span class="sxs-lookup"><span data-stu-id="93a20-108">The **reference** element contains a list of references to URLs.</span></span> <span data-ttu-id="93a20-109">Cada item na lista tem o formato Ref *XX*  =  *URL*, em que *XX* é um inteiro e a *URL* é a URL de um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="93a20-109">Each item in the list has the form Ref *XX* = *URL*, where *XX* is an integer and *URL* is the URL of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="93a20-110">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="93a20-110">**Syntax**</span></span>


```XML
[reference]
RefXX = URL
RefXX = URL
   
<entity type="hellip"/>
```



<span data-ttu-id="93a20-111">Os inteiros representados por *XX* devem estar em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="93a20-111">The integers represented by *XX* must be in ascending order.</span></span> <span data-ttu-id="93a20-112">Ou seja, o número inteiro em cada linha deve ser maior que o inteiro na linha anterior.</span><span class="sxs-lookup"><span data-stu-id="93a20-112">That is, the integer in each line must be greater than the integer in the preceding line.</span></span>

<span data-ttu-id="93a20-113">Quando um programa cliente lê um elemento de referência, ele tenta se conectar ao arquivo de mídia representado pela primeira URL na lista.</span><span class="sxs-lookup"><span data-stu-id="93a20-113">When a client program reads a reference element, it attempts to connect to the media file represented by the first URL in the list.</span></span> <span data-ttu-id="93a20-114">Se isso falhar, o programa cliente tentará se conectar ao arquivo representado pela próxima URL na lista.</span><span class="sxs-lookup"><span data-stu-id="93a20-114">If that fails, the client program attempts to connect to the file represented by the next URL in the list.</span></span> <span data-ttu-id="93a20-115">O programa cliente continua a lista até que faça uma conexão bem-sucedida ou atinja o final da lista.</span><span class="sxs-lookup"><span data-stu-id="93a20-115">The client program continues down the list until it makes a successful connection or reaches the end of the list.</span></span> <span data-ttu-id="93a20-116">Observe que, se o programa cliente fizer uma conexão bem-sucedida, ele não lerá nenhuma das URLs subsequentes na lista.</span><span class="sxs-lookup"><span data-stu-id="93a20-116">Note that if the client program makes a successful connection, it does not read any of the subsequent URLs in the list.</span></span>

<span data-ttu-id="93a20-117">**Código de exemplo**</span><span class="sxs-lookup"><span data-stu-id="93a20-117">**Example Code**</span></span>

<span data-ttu-id="93a20-118">No exemplo a seguir, o programa cliente tentaria primeiro se conectar ao arquivo representado pela URL MMS.</span><span class="sxs-lookup"><span data-stu-id="93a20-118">In the following example, the client program would first attempt to connect to the file represented by the mms URL.</span></span> <span data-ttu-id="93a20-119">Se isso falhar, o programa cliente tentaria se conectar ao arquivo representado pela URL http.</span><span class="sxs-lookup"><span data-stu-id="93a20-119">If that failed, the client program would attempt to connect to the file represented by the http URL.</span></span>


```XML
[reference]
Ref01 = mms://example.com/MusicFile.wma
Ref02 = https://example.com/MusicFile.wma

```



## <a name="remarks"></a><span data-ttu-id="93a20-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="93a20-120">Remarks</span></span>

<span data-ttu-id="93a20-121">O formato de arquivo ASF abrange uma ampla variedade de tipos de mídia, incluindo áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="93a20-121">The ASF file format encompasses a wide variety of media types including audio and video.</span></span> <span data-ttu-id="93a20-122">Os arquivos ASF também usam várias extensões de nome de arquivo diferentes, incluindo. WMA e. wmv.</span><span class="sxs-lookup"><span data-stu-id="93a20-122">ASF files also use several different file name extensions, including .wma and .wmv.</span></span>

<span data-ttu-id="93a20-123">Os inteiros representados por *XX* devem estar em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="93a20-123">The integers represented by *XX* must be in ascending order.</span></span> <span data-ttu-id="93a20-124">Ou seja, o número inteiro em cada linha deve ser maior que o inteiro na linha anterior.</span><span class="sxs-lookup"><span data-stu-id="93a20-124">That is, the integer in each line must be greater than the integer in the preceding line.</span></span>

<span data-ttu-id="93a20-125">Quando um programa cliente lê um elemento de referência, ele tenta se conectar ao arquivo de mídia representado pela primeira URL na lista.</span><span class="sxs-lookup"><span data-stu-id="93a20-125">When a client program reads a reference element, it attempts to connect to the media file represented by the first URL in the list.</span></span> <span data-ttu-id="93a20-126">Se isso falhar, o programa cliente tentará se conectar ao arquivo representado pela próxima URL na lista.</span><span class="sxs-lookup"><span data-stu-id="93a20-126">If that fails, the client program attempts to connect to the file represented by the next URL in the list.</span></span> <span data-ttu-id="93a20-127">O programa cliente continua a lista até que faça uma conexão bem-sucedida ou atinja o final da lista.</span><span class="sxs-lookup"><span data-stu-id="93a20-127">The client program continues down the list until it makes a successful connection or reaches the end of the list.</span></span> <span data-ttu-id="93a20-128">Observe que, se o programa cliente fizer uma conexão bem-sucedida, ele não lerá nenhuma das URLs subsequentes na lista.</span><span class="sxs-lookup"><span data-stu-id="93a20-128">Note that if the client program makes a successful connection, it does not read any of the subsequent URLs in the list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93a20-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="93a20-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93a20-130">**Versões anteriores de metaarquivos do Windows Media (preterido)**</span><span class="sxs-lookup"><span data-stu-id="93a20-130">**Previous Versions of Windows Media Metafiles (deprecated)**</span></span>](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




