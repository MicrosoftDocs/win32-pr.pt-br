---
description: Tenho um arquivo AVI contendo um fluxo de vídeo do Windows Media.
ms.assetid: 0b4c5bf2-caa6-4e14-be5f-9e25ec918cf0
title: Tenho um arquivo AVI contendo um fluxo de vídeo do Windows Media. Como posso convertê-lo em um arquivo WMV?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c770a8355e92c6cfe052d86a17c6638a7a9948
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105765608"
---
# <a name="i-have-an-avi-file-containing-a-windows-media-video-stream-how-can-i-convert-it-to-a-wmv-file"></a><span data-ttu-id="85ede-104">Tenho um arquivo AVI contendo um fluxo de vídeo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="85ede-104">I have an AVI file containing a Windows Media Video stream.</span></span> <span data-ttu-id="85ede-105">Como posso convertê-lo em um arquivo WMV?</span><span class="sxs-lookup"><span data-stu-id="85ede-105">How can I convert it to a WMV file?</span></span>

<span data-ttu-id="85ede-106">As interfaces do codec de áudio e vídeo do Windows Media não fornecem métodos para criar arquivos usando o ASF (Advanced Systems Format), que é o formato usado para arquivos WMV.</span><span class="sxs-lookup"><span data-stu-id="85ede-106">The Windows Media Audio and Video codec interfaces do not provide methods to create files using the Advanced Systems Format (ASF), which is the format used for WMV files.</span></span> <span data-ttu-id="85ede-107">Se você quiser converter um arquivo (usando qualquer contêiner) em um arquivo ASF, deverá usar os objetos do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="85ede-107">If you want to convert a file (using any container) to an ASF file, you must use the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="85ede-108">Recupere os exemplos do Windows Media compactados do arquivo de origem e passe-os para o objeto do gravador como amostras de fluxo.</span><span class="sxs-lookup"><span data-stu-id="85ede-108">Retrieve the compressed Windows Media samples from the source file and pass them to the writer object as stream samples.</span></span> <span data-ttu-id="85ede-109">Para obter mais informações, consulte a documentação do SDK da série Windows Media Format 9 Series.</span><span class="sxs-lookup"><span data-stu-id="85ede-109">For more information, see the Windows Media Format 9 Series SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85ede-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="85ede-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85ede-111">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="85ede-111">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



