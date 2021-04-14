---
description: O tipo de dados filename é uma cadeia de caracteres de texto que contém um nome de arquivo ou pasta.
ms.assetid: af59e1b8-0699-4031-895f-415752611e21
title: Nome de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fc049fa0808efc180afbd715e311a124bfdada9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502368"
---
# <a name="filename"></a><span data-ttu-id="5bf1a-103">Nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="5bf1a-103">Filename</span></span>

<span data-ttu-id="5bf1a-104">O tipo de dados filename é uma cadeia de caracteres de texto que contém um nome de arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-104">The Filename data type is a text string containing a file name or folder.</span></span> <span data-ttu-id="5bf1a-105">Por padrão, o nome do arquivo é considerado para usar a sintaxe de nome de arquivo curto; ou seja, nome de oito caracteres, ponto final (.) e extensão de 3 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-105">By default, the file name is assumed to use short file name syntax; that is, eight-character name, period (.), and 3-character extension.</span></span> <span data-ttu-id="5bf1a-106">Um nome de arquivo curto sempre deve ser fornecido porque a propriedade [**SHORTFILENAMES**](shortfilenames.md) pode ser definida ou o volume de destino para a instalação pode dar suporte apenas a nomes de arquivo curtos.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-106">A short file name must always be provided because the [**SHORTFILENAMES**](shortfilenames.md) property may be set or the target volume for the installation may only support short file names.</span></span>

<span data-ttu-id="5bf1a-107">Para incluir um nome de arquivo longo com o nome de arquivo curto, separe-o do nome de arquivo curto com uma barra vertical ( \| ).</span><span class="sxs-lookup"><span data-stu-id="5bf1a-107">To include a long file name with the short file name, separate it from the short file name with a vertical bar (\|).</span></span>

<span data-ttu-id="5bf1a-108">Por exemplo, as duas cadeias de caracteres a seguir são válidas:</span><span class="sxs-lookup"><span data-stu-id="5bf1a-108">For example, the following two strings are valid:</span></span>

-   <span data-ttu-id="5bf1a-109">status.txt</span><span class="sxs-lookup"><span data-stu-id="5bf1a-109">status.txt</span></span>
-   <span data-ttu-id="5bf1a-110">proje ~ Status.txt do projeto de1.txt\|</span><span class="sxs-lookup"><span data-stu-id="5bf1a-110">projec~1.txt\|Project Status.txt</span></span>

<span data-ttu-id="5bf1a-111">Nomes de arquivo curtos e longos não devem conter os seguintes caracteres:</span><span class="sxs-lookup"><span data-stu-id="5bf1a-111">Short and long file names must not contain the following characters:</span></span>

-   <span data-ttu-id="5bf1a-112">barra (/) ou ( \\ )</span><span class="sxs-lookup"><span data-stu-id="5bf1a-112">slash (/) or (\\)</span></span>
-   <span data-ttu-id="5bf1a-113">ponto de interrogação (?)</span><span class="sxs-lookup"><span data-stu-id="5bf1a-113">question mark (?)</span></span>
-   <span data-ttu-id="5bf1a-114">barra vertical ( \| )</span><span class="sxs-lookup"><span data-stu-id="5bf1a-114">vertical bar (\|)</span></span>
-   <span data-ttu-id="5bf1a-115">colchete angular direito (>)</span><span class="sxs-lookup"><span data-stu-id="5bf1a-115">right angle bracket (>)</span></span>
-   <span data-ttu-id="5bf1a-116">colchete angular esquerdo (<)</span><span class="sxs-lookup"><span data-stu-id="5bf1a-116">left angle bracket (<)</span></span>
-   <span data-ttu-id="5bf1a-117">dois pontos (:)</span><span class="sxs-lookup"><span data-stu-id="5bf1a-117">colon (:)</span></span>
-   <span data-ttu-id="5bf1a-118">asterisco ( \* )</span><span class="sxs-lookup"><span data-stu-id="5bf1a-118">asterisk (\*)</span></span>
-   <span data-ttu-id="5bf1a-119">aspas (")</span><span class="sxs-lookup"><span data-stu-id="5bf1a-119">quotation mark (")</span></span>

<span data-ttu-id="5bf1a-120">Além disso, nomes de arquivo curtos não devem conter os seguintes caracteres:</span><span class="sxs-lookup"><span data-stu-id="5bf1a-120">In addition, short file names must not contain the following characters:</span></span>

-   <span data-ttu-id="5bf1a-121">sinal de mais (+)</span><span class="sxs-lookup"><span data-stu-id="5bf1a-121">plus sign (+)</span></span>
-   <span data-ttu-id="5bf1a-122">vírgula (,)</span><span class="sxs-lookup"><span data-stu-id="5bf1a-122">comma (,)</span></span>
-   <span data-ttu-id="5bf1a-123">ponto e vírgula (;)</span><span class="sxs-lookup"><span data-stu-id="5bf1a-123">semicolon (;)</span></span>
-   <span data-ttu-id="5bf1a-124">sinal de igual (=)</span><span class="sxs-lookup"><span data-stu-id="5bf1a-124">equals sign (=)</span></span>
-   <span data-ttu-id="5bf1a-125">colchete esquerdo ( \[ )</span><span class="sxs-lookup"><span data-stu-id="5bf1a-125">left square bracket (\[)</span></span>
-   <span data-ttu-id="5bf1a-126">colchete direito ( \] )</span><span class="sxs-lookup"><span data-stu-id="5bf1a-126">right square bracket (\])</span></span>

<span data-ttu-id="5bf1a-127">Nenhum espaço é permitido antes do separador de barra vertical ( \| ) para a sintaxe de nome de arquivo curto/arquivo longo.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-127">No space is allowed preceding the vertical bar (\|) separator for the short file name/long file name syntax.</span></span> <span data-ttu-id="5bf1a-128">Nomes de arquivo curtos não podem incluir um espaço, embora um nome de arquivo longo possa.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-128">Short file names may not include a space, although a long file name may.</span></span> <span data-ttu-id="5bf1a-129">Um espaço pode existir após o separador somente se o nome de arquivo longo do nome do arquivo começar com o espaço.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-129">A space can exist after the separator only if the long file name of the file name begins with the space.</span></span> <span data-ttu-id="5bf1a-130">Nenhuma sintaxe de caminho completo é permitida.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-130">No full-path syntax is allowed.</span></span>

> [!Note]  
> <span data-ttu-id="5bf1a-131">O formato da coluna FileName da tabela [MsiEmbeddedUI](msiembeddedui-table.md) é como o tipo de dados Format FileName, exceto que o separador da barra vertical ( \| ) para a sintaxe nome curto do arquivo/nome de arquivo longo não está disponível.</span><span class="sxs-lookup"><span data-stu-id="5bf1a-131">The format of the FileName column of the [MsiEmbeddedUI](msiembeddedui-table.md) table is like the format Filename data type except that the vertical bar (\|) separator for the short file name/long file name syntax is not available.</span></span>

 

 

 



