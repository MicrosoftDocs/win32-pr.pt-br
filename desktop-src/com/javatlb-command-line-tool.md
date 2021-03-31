---
title: Ferramenta de Command-Line de JavaTLB
description: Ferramenta de Command-Line de JavaTLB
ms.assetid: b46d7bcc-ccd9-4242-9b19-f398d2cb8f91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0214648f7ad86613d6b35e3084021e2be24aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637211"
---
# <a name="javatlb-command-line-tool"></a><span data-ttu-id="4ddda-103">Ferramenta de Command-Line de JavaTLB</span><span class="sxs-lookup"><span data-stu-id="4ddda-103">JavaTLB Command-Line Tool</span></span>

<span data-ttu-id="4ddda-104">JavaTLB é um componente do Visual J++ 5,0.</span><span class="sxs-lookup"><span data-stu-id="4ddda-104">JavaTLB is a component of Visual J++ 5.0.</span></span> <span data-ttu-id="4ddda-105">JavaTLB é um aplicativo de linha de comando que gera arquivos de classe para um objeto COM.</span><span class="sxs-lookup"><span data-stu-id="4ddda-105">JavaTLB is a command-line application that generates class files for a COM object.</span></span> <span data-ttu-id="4ddda-106">Os métodos que contêm tipos de dados que não podem ser representados de forma precisa e segura em Java não são convertidos.</span><span class="sxs-lookup"><span data-stu-id="4ddda-106">Methods that contain data types that cannot be accurately and safely represented in Java are not converted.</span></span>

<span data-ttu-id="4ddda-107">Diferentemente do [Assistente da biblioteca de tipos Java](java-type-library-wizard.md), o JavaTLB não gera um arquivo de resumo contendo as informações da biblioteca de tipos do Java.</span><span class="sxs-lookup"><span data-stu-id="4ddda-107">Unlike the [Java Type Library Wizard](java-type-library-wizard.md), JavaTLB does not generate a summary file containing the Java type library information.</span></span>

<span data-ttu-id="4ddda-108">Para gerar arquivos de classe Java para um único objeto COM, a partir do prompt de comando, execute:</span><span class="sxs-lookup"><span data-stu-id="4ddda-108">To generate Java class files for a single COM object, from the command prompt run:</span></span>

<span data-ttu-id="4ddda-109"> *nome de arquivo* javatlb</span><span class="sxs-lookup"><span data-stu-id="4ddda-109">**javatlb** *filename*</span></span>

<span data-ttu-id="4ddda-110">em que *filename* é o nome do arquivo que contém a biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="4ddda-110">where *filename* is the name of the file that contains the type library.</span></span> <span data-ttu-id="4ddda-111">Esse arquivo pode ter qualquer uma das seguintes extensões de nome de arquivo:. tlb,. olb,. ocx,. dll ou. exe.</span><span class="sxs-lookup"><span data-stu-id="4ddda-111">This file may have any of the following file name extensions: .tlb, .olb, .ocx, .dll, or .exe.</span></span>

<span data-ttu-id="4ddda-112">Para gerar arquivos de classe Java para vários objetos COM, a partir do prompt de comando, execute:</span><span class="sxs-lookup"><span data-stu-id="4ddda-112">To generate Java class files for multiple COM objects, from the command prompt run:</span></span>

<span data-ttu-id="4ddda-113">\**javatlb @ \* \* \* textfile*</span><span class="sxs-lookup"><span data-stu-id="4ddda-113">\**javatlb @\*\*\*TextFile*</span></span>

<span data-ttu-id="4ddda-114">em que *textfile* é o nome de um arquivo de texto que contém uma lista dos arquivos que contêm as bibliotecas de tipos do objeto com.</span><span class="sxs-lookup"><span data-stu-id="4ddda-114">where *TextFile* is the name of a text file that contains a list of the files containing the COM object's type libraries.</span></span>

> [!Note]  
> <span data-ttu-id="4ddda-115">No Visual J++ 6,0, a ferramenta de linha de comando JavaTLB é substituída pela [ferramenta Jactivex](jactivex-command-line-tool.md).</span><span class="sxs-lookup"><span data-stu-id="4ddda-115">In Visual J++ 6.0, the JavaTLB command-line tool is replaced by the [JActiveX tool](jactivex-command-line-tool.md).</span></span> <span data-ttu-id="4ddda-116">Para obter mais informações, consulte a documentação do Visual J++ 6,0.</span><span class="sxs-lookup"><span data-stu-id="4ddda-116">For more information, see the Visual J++ 6.0 documentation.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4ddda-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4ddda-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ddda-118">Convertendo para Java</span><span class="sxs-lookup"><span data-stu-id="4ddda-118">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




