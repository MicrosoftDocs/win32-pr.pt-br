---
title: Arquivos de resposta
description: Como alternativa à colocação de todas as opções na linha de comando, o compilador MIDL aceita arquivos de resposta que contêm opções e argumentos.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL compiler MIDL , arquivos de resposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9b4d079e92dff3c25f8a38c6c73073a548ea91
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387065"
---
# <a name="response-files"></a><span data-ttu-id="0df0d-104">Arquivos de resposta</span><span class="sxs-lookup"><span data-stu-id="0df0d-104">Response Files</span></span>

<span data-ttu-id="0df0d-105">Como alternativa à colocação de todas as opções na linha de comando, o compilador MIDL aceita arquivos de resposta que contêm opções e argumentos.</span><span class="sxs-lookup"><span data-stu-id="0df0d-105">As an alternative to placing all the options on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="0df0d-106">Um arquivo de resposta é um arquivo de texto que contém uma ou mais opções de linha de comando do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="0df0d-106">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="0df0d-107">Ao contrário de uma linha de comando, um arquivo de resposta permite várias linhas de opções e nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="0df0d-107">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="0df0d-108">Isso pode ser útil devido a limitações do seu ambiente de build ou como uma conveniência para o processo de build.</span><span class="sxs-lookup"><span data-stu-id="0df0d-108">This may be useful due to limitations of your build environment or as a convenience for your build process.</span></span> <span data-ttu-id="0df0d-109">Você pode especificar um arquivo de resposta MIDL como:</span><span class="sxs-lookup"><span data-stu-id="0df0d-109">You can specify a MIDL response file as:</span></span>

<span data-ttu-id="0df0d-110">**midl** **\@ filename**</span><span class="sxs-lookup"><span data-stu-id="0df0d-110">**midl** **\@filename**</span></span>

<dl> <dt>

<span data-ttu-id="0df0d-111"><span id="filename"></span><span id="FILENAME"></span>*Filename*</span><span class="sxs-lookup"><span data-stu-id="0df0d-111"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="0df0d-112">Especifica o nome do arquivo de resposta.</span><span class="sxs-lookup"><span data-stu-id="0df0d-112">Specifies the name of the response file.</span></span> <span data-ttu-id="0df0d-113">O nome do arquivo de resposta deve seguir imediatamente o caractere @ sem espaço em branco entre o caractere @ e o nome do arquivo de resposta.</span><span class="sxs-lookup"><span data-stu-id="0df0d-113">The response file name must immediately follow the @ character with no white space between the @ character and the response file name.</span></span>

</dd> </dl>

<span data-ttu-id="0df0d-114">As opções em um arquivo de resposta são interpretadas como se elas estavam presentes nesse local na linha de comando MIDL.</span><span class="sxs-lookup"><span data-stu-id="0df0d-114">Options in a response file are interpreted as if they were present at that place in the MIDL command line.</span></span> <span data-ttu-id="0df0d-115">Cada argumento em um arquivo de resposta deve começar e terminar na mesma linha.</span><span class="sxs-lookup"><span data-stu-id="0df0d-115">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="0df0d-116">Não é possível usar o caractere de linha invertida ( \\ ) para concatenar linhas.</span><span class="sxs-lookup"><span data-stu-id="0df0d-116">You cannot use the backslash character (\\) to concatenate lines.</span></span>

<span data-ttu-id="0df0d-117">O MIDL dá suporte a argumentos de linha de comando que incluem um ou mais arquivos de resposta, combinados com outras opções de linha de comando:</span><span class="sxs-lookup"><span data-stu-id="0df0d-117">MIDL supports command-line arguments that include one or more response files, combined with other command-line switches:</span></span>

<span data-ttu-id="0df0d-118">**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**</span><span class="sxs-lookup"><span data-stu-id="0df0d-118">**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**</span></span>

<span data-ttu-id="0df0d-119">O compilador MIDL não dá suporte a arquivos de resposta aninhados.</span><span class="sxs-lookup"><span data-stu-id="0df0d-119">The MIDL compiler does not support nested response files.</span></span>

 

 




