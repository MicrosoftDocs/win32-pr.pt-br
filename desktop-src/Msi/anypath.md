---
description: O tipo de dados AnyPath é uma cadeia de caracteres de texto que contém um caminho completo ou um caminho relativo.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ab6265874616bb0bb1a2f61098cdbabfa8ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752664"
---
# <a name="anypath"></a><span data-ttu-id="5c277-103">AnyPath</span><span class="sxs-lookup"><span data-stu-id="5c277-103">AnyPath</span></span>

<span data-ttu-id="5c277-104">O tipo de dados AnyPath é uma cadeia de caracteres de texto que contém um caminho completo ou um caminho relativo.</span><span class="sxs-lookup"><span data-stu-id="5c277-104">The AnyPath data type is a text string containing either a full path or a relative path.</span></span> <span data-ttu-id="5c277-105">Ao especificar um caminho relativo, você pode incluir um nome de arquivo longo com o nome curto do arquivo separando os nomes curtos e longos com uma barra vertical ( \| ).</span><span class="sxs-lookup"><span data-stu-id="5c277-105">When specifying a relative path, you can include a long file name with the short file name by separating the short and long names with a vertical bar (\|).</span></span> <span data-ttu-id="5c277-106">Observe que você não pode especificar vários níveis de um diretório ou caminhos totalmente qualificados dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="5c277-106">Note that you cannot specify multiple levels of a directory or fully qualified paths in this way.</span></span> <span data-ttu-id="5c277-107">O caminho pode conter Propriedades delimitadas entre colchetes ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="5c277-107">The path may contain properties enclosed within square brackets (\[ \]).</span></span>

<span data-ttu-id="5c277-108">Exemplos de dados de AnyPath válidos:</span><span class="sxs-lookup"><span data-stu-id="5c277-108">Examples of valid AnyPath data:</span></span>

-   <span data-ttu-id="5c277-109">\\\\\\Temp do compartilhamento do servidor \\</span><span class="sxs-lookup"><span data-stu-id="5c277-109">\\\\server\\share\\temp</span></span>
-   <span data-ttu-id="5c277-110">c: \\ Temp</span><span class="sxs-lookup"><span data-stu-id="5c277-110">c:\\temp</span></span>
-   <span data-ttu-id="5c277-111">\\Temp</span><span class="sxs-lookup"><span data-stu-id="5c277-111">\\temp</span></span>
-   <span data-ttu-id="5c277-112">proje ~ 1 \| status do projeto</span><span class="sxs-lookup"><span data-stu-id="5c277-112">projec~1\|Project Status</span></span>

<span data-ttu-id="5c277-113">Exemplos de dados de AnyPath inválidos:</span><span class="sxs-lookup"><span data-stu-id="5c277-113">Examples of invalid AnyPath data:</span></span>

-   <span data-ttu-id="5c277-114">c: \\ temp \\ proje ~ 1 \| c: \\ Temp um \\ status do projeto</span><span class="sxs-lookup"><span data-stu-id="5c277-114">c:\\temp\\projec~1\|c:\\temp one\\Project Status</span></span>
-   <span data-ttu-id="5c277-115">\\temp \\ proje ~ 1 \| \\ Temp um \\ status do projeto</span><span class="sxs-lookup"><span data-stu-id="5c277-115">\\temp\\projec~1\|\\temp one\\Project Status</span></span>

 

 



