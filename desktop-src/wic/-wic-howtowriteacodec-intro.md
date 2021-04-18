---
description: O Windows Imaging Component (WIC) é uma plataforma extensível para geração de imagens digitais nos sistemas operacionais Windows Vista e Windows 7.
ms.assetid: ffcd5239-ae2d-436f-9402-8c10a79256c3
title: Introdução (como escrever um codec de WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776bf9f2c0cb5df8b45ce04d55f20d40d05a12a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815458"
---
# <a name="introduction-how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="e1bbe-103">Introdução (como escrever um codec de WIC-Enabled)</span><span class="sxs-lookup"><span data-stu-id="e1bbe-103">Introduction (How to Write a WIC-Enabled Codec)</span></span>

<span data-ttu-id="e1bbe-104">O Windows Imaging Component (WIC) é uma plataforma extensível para geração de imagens digitais nos sistemas operacionais Windows Vista e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e1bbe-104">The Windows Imaging Component (WIC) is an extensible platform for digital imaging on the Windows Vista and Windows 7 operating systems.</span></span> <span data-ttu-id="e1bbe-105">O WIC também está disponível no Windows XP e no Windows Server 2003, como parte do Microsoft .NET Framework 3,0 ou como um componente separado que você pode redistribuir.</span><span class="sxs-lookup"><span data-stu-id="e1bbe-105">WIC is also available on Windows XP and Windows Server 2003, either as part of Microsoft .NET Framework 3.0 or as a separate component that you can redistribute.</span></span> <span data-ttu-id="e1bbe-106">Qualquer aplicativo que use o WIC pode acessar, exibir, processar e imprimir imagens em qualquer formato de imagem que forneça um codec habilitado para WIC, usando um único conjunto de interfaces consistentes que eliminam a necessidade de conhecimento especializado de formatos específicos.</span><span class="sxs-lookup"><span data-stu-id="e1bbe-106">Any application using the WIC can access, display, process, and print images in any image format that provides a WIC-enabled codec, using a single set of consistent interfaces that eliminate the need for specialized knowledge of specific formats.</span></span>

<span data-ttu-id="e1bbe-107">O Windows Vista Explorer, a Galeria de fotos do Windows Vista, a Galeria de fotos ao vivo e o Visualizador de fotos do Windows 7 são criados no WIC.</span><span class="sxs-lookup"><span data-stu-id="e1bbe-107">The Windows Vista Explorer, Windows Vista Photo Gallery, Live Photo Gallery, and Windows 7 Photo Viewer are built on WIC.</span></span> <span data-ttu-id="e1bbe-108">Depois que um codec habilitado para WIC é instalado em um sistema Windows Vista ou Windows 7, o sistema operacional fornece o mesmo nível de suporte para o formato de imagem associado para os formatos de imagem padrão fornecidos com a plataforma.</span><span class="sxs-lookup"><span data-stu-id="e1bbe-108">After a WIC-enabled codec is installed on a Windows Vista or Windows 7 system, the operating system provides the same level of support for the associated image format as for the standard image formats that ship with the platform.</span></span> <span data-ttu-id="e1bbe-109">Como você escreve o codec para seu próprio formato de imagem, você pode garantir uma qualidade consistente onde quer que seu formato de imagem seja usado, além de obter os benefícios do suporte completo à plataforma.</span><span class="sxs-lookup"><span data-stu-id="e1bbe-109">Because you write the codec for your own image format, you can ensure consistent quality wherever your image format is used, and you get the benefits of full platform support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1bbe-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1bbe-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e1bbe-111">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="e1bbe-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e1bbe-112">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="e1bbe-112">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="e1bbe-113">Como funciona o Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="e1bbe-113">How The Windows Imaging Component Works</span></span>](-wic-howwicworks.md)
</dt> <dt>

<span data-ttu-id="e1bbe-114">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="e1bbe-114">How to Write a WIC-Enabled CODEC</span></span>
</dt> <dt>

[<span data-ttu-id="e1bbe-115">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="e1bbe-115">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



