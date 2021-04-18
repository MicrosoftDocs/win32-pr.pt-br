---
description: Como fazer descompactar fluxos de um arquivo AVI ou outro arquivo sobre o qual não tenho informações de formato?
ms.assetid: 980f52f4-17a4-4871-9269-f9e0b97416c6
title: Como fazer descompactar fluxos de um arquivo AVI ou outro arquivo sobre o qual não tenho informações de formato?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad230c36097a93b3d2d41ddffb35600d0616ea5f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105793611"
---
# <a name="how-do-i-decompress-streams-from-an-avi-file-or-other-file-about-which-i-have-no-format-information"></a><span data-ttu-id="a3976-103">Como fazer descompactar fluxos de um arquivo AVI ou outro arquivo sobre o qual não tenho informações de formato?</span><span class="sxs-lookup"><span data-stu-id="a3976-103">How do I decompress streams from an AVI file or other file about which I have no format information?</span></span>

<span data-ttu-id="a3976-104">Sem informações de formato, incluindo dados de formato estendidos, não é possível descompactar dados que foram codificados com um codec do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a3976-104">Without format information, including extended format data, you cannot decompress data that was encoded with a Windows Media codec.</span></span> <span data-ttu-id="a3976-105">Os codecs foram projetados para criar fluxos de dados para uso com o contêiner de arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="a3976-105">The codecs were designed to create data streams for use with the Advanced Systems Format (ASF) file container.</span></span> <span data-ttu-id="a3976-106">A seção de cabeçalho de um arquivo ASF armazena as informações de formato de todos os fluxos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="a3976-106">The header section of an ASF file stores the format information for all of the streams in the file.</span></span> <span data-ttu-id="a3976-107">Ao usar o conteúdo codificado usando um dos codecs de áudio e vídeo do Windows Media fora de um arquivo ASF, você deve garantir que as informações de formato estejam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a3976-107">When you use content encoded using one of the Windows Media Audio and Video codecs outside of an ASF file, you must ensure that the format information is available.</span></span> <span data-ttu-id="a3976-108">A maneira de fazer isso varia de um contêiner para outro.</span><span class="sxs-lookup"><span data-stu-id="a3976-108">The way to do this varies from one container to another.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3976-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3976-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3976-110">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="a3976-110">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



