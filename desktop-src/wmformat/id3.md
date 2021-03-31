---
title: Suporte a ID3
description: ID3 é uma organização que definiu um conjunto de padrões para incluir metadados em arquivos de áudio MPEG (camada 3).
ms.assetid: 8c1f1114-48d8-4dce-b7ab-0293265a875c
keywords:
- SDK do Windows Media Format, suporte a ID3
- ASF (Advanced Systems Format), suporte a ID3
- ASF (formato de sistemas avançados), suporte a ID3
- metadados, ID3
- ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f356dae63b1d3672b584bb61956f478b67a697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636858"
---
# <a name="id3-support"></a><span data-ttu-id="e357c-108">Suporte a ID3</span><span class="sxs-lookup"><span data-stu-id="e357c-108">ID3 Support</span></span>

<span data-ttu-id="e357c-109">ID3 é uma organização que definiu um conjunto de padrões para incluir metadados em arquivos de áudio MPEG (camada 3).</span><span class="sxs-lookup"><span data-stu-id="e357c-109">ID3 is an organization that has defined a set of standards for including metadata in MPEG Layer-3 (MP3) audio files.</span></span> <span data-ttu-id="e357c-110">Os objetos do Windows Media Format SDK fornecem suporte para atributos compatíveis de ID3.</span><span class="sxs-lookup"><span data-stu-id="e357c-110">The objects of the Windows Media Format SDK provide support for ID3 compatible attributes.</span></span> <span data-ttu-id="e357c-111">Há suporte para três versões de ID3 distintas: ID3v1. x, ID3v 2.2 e ID3v 2.3/v2, 4.</span><span class="sxs-lookup"><span data-stu-id="e357c-111">Three distinct ID3 versions are supported: ID3v1.x, ID3v2.2, and ID3v2.3/v2,4.</span></span> <span data-ttu-id="e357c-112">Para obter uma lista dos atributos que correspondem a quadros ID3, consulte [suporte a marcas ID3](id3-tag-support.md).</span><span class="sxs-lookup"><span data-stu-id="e357c-112">For a list of the attributes that equate to ID3 frames, see [ID3 Tag Support](id3-tag-support.md).</span></span>

<span data-ttu-id="e357c-113">Salvo indicação em contrário, nenhuma validação dos dados de quadro ID3 é executada pelos objetos deste SDK.</span><span class="sxs-lookup"><span data-stu-id="e357c-113">Unless otherwise noted, no validation of ID3 frame data is performed by the objects of this SDK.</span></span> <span data-ttu-id="e357c-114">Por exemplo, o atributo de metadados [**WM/música \_ sincronizado**](wm-lyrics-synchronised.md) armazena as músicas de música com carimbos de data/hora correspondentes.</span><span class="sxs-lookup"><span data-stu-id="e357c-114">For example, the metadata attribute [**WM/Lyrics\_Synchronised**](wm-lyrics-synchronised.md) stores the song lyrics with corresponding time stamps.</span></span> <span data-ttu-id="e357c-115">Ao gravar um atributo **\_ sincronizado do WM/música** , os objetos desse SDK não verificarão se os carimbos de data/hora estão em ordem cronológica ou realizam a validação de qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="e357c-115">When writing a **WM/Lyrics\_Synchronised** attribute, the objects of this SDK will not check to ensure that the time stamps are in chronological order or perform validation of any kind.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e357c-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e357c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e357c-117">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="e357c-117">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="e357c-118">**Recursos de metadados**</span><span class="sxs-lookup"><span data-stu-id="e357c-118">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="e357c-119">**Trabalhando com metadados**</span><span class="sxs-lookup"><span data-stu-id="e357c-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




