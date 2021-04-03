---
description: Este tópico apresenta como imprimir de um programa nativo do Windows usando o GDI&\# 160; Imprimir&\# 160; API.
ms.assetid: C212DD92-2B90-45BC-8746-29C193FBDF69
title: 'Como: imprimir usando a API de impressão GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d6351e228297b5378b54879548b823f81894b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837147"
---
# <a name="how-to-print-using-the-gdi-print-api"></a><span data-ttu-id="d5070-103">Como: imprimir usando a API de impressão GDI</span><span class="sxs-lookup"><span data-stu-id="d5070-103">How To: Print Using the GDI Print API</span></span>

<span data-ttu-id="d5070-104">Este tópico apresenta como imprimir de um programa nativo do Windows usando a [API de impressão do GDI](gdi-printing.md).</span><span class="sxs-lookup"><span data-stu-id="d5070-104">This topic introduces how to print from a native Windows program using the [GDI Print API](gdi-printing.md).</span></span>

## <a name="overview"></a><span data-ttu-id="d5070-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="d5070-105">Overview</span></span>

<span data-ttu-id="d5070-106">A impressão geralmente é parte integrante de um programa nativo do Windows, portanto, não é um recurso que você pode adicionar facilmente depois de escrever o programa.</span><span class="sxs-lookup"><span data-stu-id="d5070-106">Printing is usually an integral part of a native Windows program, so it is not a feature that you can add easily after you have written the program.</span></span> <span data-ttu-id="d5070-107">Ao criar um programa para o Windows 7, você deve considerar o uso da [API de impressão XPS](xps-printing.md) para fornecer a funcionalidade de impressão, pois ela fornece a maior compatibilidade para o futuro.</span><span class="sxs-lookup"><span data-stu-id="d5070-107">When designing a program for Windows 7, you should consider using the [XPS Print API](xps-printing.md) to provide the printing functionality because it provides the most compatibility for the future.</span></span> <span data-ttu-id="d5070-108">Programas que devem ser executados no Windows Vista e em versões anteriores do Windows provavelmente usarão a [API de impressão GDI](gdi-printing.md) para fornecer a funcionalidade de impressão.</span><span class="sxs-lookup"><span data-stu-id="d5070-108">Programs that must run on Windows Vista and earlier versions of Windows will most likely use the [GDI Print API](gdi-printing.md) to provide printing functionality.</span></span> <span data-ttu-id="d5070-109">A API de impressão GDI também tem suporte no Windows 7, mas é mais limitada do que a API de impressão XPS.</span><span class="sxs-lookup"><span data-stu-id="d5070-109">The GDI Print API is also supported in Windows 7, but it is more limited than the XPS Print API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5070-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5070-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5070-111">Usando a impressão</span><span class="sxs-lookup"><span data-stu-id="d5070-111">Using Printing</span></span>](using-printing.md)
</dt> <dt>

[<span data-ttu-id="d5070-112">Como imprimir a partir de um aplicativo do Windows</span><span class="sxs-lookup"><span data-stu-id="d5070-112">How to print from a Windows application</span></span>](how-to--print-from-a-windows-application.md)
</dt> </dl>

 

 



