---
title: Parâmetro MSWMExt (preterido)
description: Parâmetro MSWMExt (preterido)
ms.assetid: cc52da1a-26d1-4321-b421-b0d6f44635cc
keywords:
- Metaarquivos do Windows Media, parâmetro MSWMExt
- metaarquivos, parâmetro MSWMExt
- Parâmetro MSWMExt
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 745ecfb2cf716e973aec3d574247e3e45d8f49ff
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365655"
---
# <a name="mswmext-parameter-deprecated"></a><span data-ttu-id="075a2-106">Parâmetro MSWMExt (preterido)</span><span class="sxs-lookup"><span data-stu-id="075a2-106">MSWMExt Parameter (deprecated)</span></span>

<span data-ttu-id="075a2-107">O parâmetro *MSWMExt* indica para um programa cliente o formato de um arquivo referenciado.</span><span class="sxs-lookup"><span data-stu-id="075a2-107">The *MSWMExt* parameter indicates to a client program the format of a referenced file.</span></span>

<span data-ttu-id="075a2-108">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="075a2-108">**Syntax**</span></span>


```XML

URL?MSWMExt=.
ext
```



<span data-ttu-id="075a2-109">**Código de exemplo**</span><span class="sxs-lookup"><span data-stu-id="075a2-109">**Example Code**</span></span>


```XML
[reference]
Ref01 = https://example.com/GenerateASFFile.aspx?MSWMExt=.asf

```



## <a name="remarks"></a><span data-ttu-id="075a2-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="075a2-110">Remarks</span></span>

<span data-ttu-id="075a2-111">Os programas cliente às vezes usam uma extensão de nome de arquivo ou um tipo MIME para determinar se um arquivo de mídia deve ser renderizado como um fluxo, renderizar o arquivo após um download completo ou se recusar a renderizar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="075a2-111">Client programs sometimes use a file name extension or a MIME type to determine whether to render a media file as a stream, render the file after a full download, or refuse to render the file at all.</span></span> <span data-ttu-id="075a2-112">Se um programa cliente não puder determinar como tratar um arquivo de mídia com base na extensão de nome de arquivo ou no tipo MIME, ele poderá determinar como tratar o arquivo inspecionando o parâmetro *MSWMExt* .</span><span class="sxs-lookup"><span data-stu-id="075a2-112">If a client program cannot determine how to treat a media file based on the file name extension or the MIME type, it can determine how to treat the file by inspecting the *MSWMExt* parameter.</span></span> <span data-ttu-id="075a2-113">Por exemplo, o cliente poderia tratar o arquivo como se tivesse uma extensão igual ao valor do parâmetro *MSWMExt* .</span><span class="sxs-lookup"><span data-stu-id="075a2-113">For example, the client could treat the file as if it had an extension equal to the value of the *MSWMExt* parameter.</span></span> <span data-ttu-id="075a2-114">Para obter mais informações sobre tipos MIME e extensões de nome de arquivo, consulte [extensões de nome de arquivo](file-name-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="075a2-114">For more information about MIME types and file name extensions, see [File Name Extensions](file-name-extensions.md).</span></span> <span data-ttu-id="075a2-115">Para obter mais informações sobre o parâmetro *MSWMExt* , consulte o artigo [236895](https://support.microsoft.com/kb/236895) na base de dados de conhecimento Microsoft.</span><span class="sxs-lookup"><span data-stu-id="075a2-115">For more information about the *MSWMExt* parameter, see article [236895](https://support.microsoft.com/kb/236895) in the Microsoft Knowledge Base.</span></span>

## <a name="related-topics"></a><span data-ttu-id="075a2-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="075a2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="075a2-117">**Versões anteriores de metaarquivos do Windows Media (preterido)**</span><span class="sxs-lookup"><span data-stu-id="075a2-117">**Previous Versions of Windows Media Metafiles (deprecated)**</span></span>](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




