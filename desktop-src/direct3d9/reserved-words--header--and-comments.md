---
description: A tabela a seguir mostra quais palavras são reservadas e não devem ser usadas.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Palavras reservadas, cabeçalho e comentários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2696aaf6e635f08124e28392d0a8faf63c39a85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500259"
---
# <a name="reserved-words-header-and-comments"></a><span data-ttu-id="61173-103">Palavras reservadas, cabeçalho e comentários</span><span class="sxs-lookup"><span data-stu-id="61173-103">Reserved Words, Header, and Comments</span></span>

<span data-ttu-id="61173-104">A tabela a seguir mostra quais palavras são reservadas e não devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="61173-104">The table below shows which words are reserved and must not be used.</span></span>



|                  |          |           |
|------------------|----------|-----------|
| <span data-ttu-id="61173-105">ARRAY</span><span class="sxs-lookup"><span data-stu-id="61173-105">ARRAY</span></span>            | <span data-ttu-id="61173-106">DWORD</span><span class="sxs-lookup"><span data-stu-id="61173-106">DWORD</span></span>    | <span data-ttu-id="61173-107">UCHAR</span><span class="sxs-lookup"><span data-stu-id="61173-107">UCHAR</span></span>     |
| <span data-ttu-id="61173-108">BINARY</span><span class="sxs-lookup"><span data-stu-id="61173-108">BINARY</span></span>           | <span data-ttu-id="61173-109">FLOAT</span><span class="sxs-lookup"><span data-stu-id="61173-109">FLOAT</span></span>    | <span data-ttu-id="61173-110">ULONGLONG</span><span class="sxs-lookup"><span data-stu-id="61173-110">ULONGLONG</span></span> |
| <span data-ttu-id="61173-111">\_recurso binário</span><span class="sxs-lookup"><span data-stu-id="61173-111">BINARY\_RESOURCE</span></span> | <span data-ttu-id="61173-112">SDWORD</span><span class="sxs-lookup"><span data-stu-id="61173-112">SDWORD</span></span>   | <span data-ttu-id="61173-113">UNICODE</span><span class="sxs-lookup"><span data-stu-id="61173-113">UNICODE</span></span>   |
| <span data-ttu-id="61173-114">CHAR</span><span class="sxs-lookup"><span data-stu-id="61173-114">CHAR</span></span>             | <span data-ttu-id="61173-115">STRING</span><span class="sxs-lookup"><span data-stu-id="61173-115">STRING</span></span>   | <span data-ttu-id="61173-116">WORD</span><span class="sxs-lookup"><span data-stu-id="61173-116">WORD</span></span>      |
| <span data-ttu-id="61173-117">CSTRING</span><span class="sxs-lookup"><span data-stu-id="61173-117">CSTRING</span></span>          | <span data-ttu-id="61173-118">SWORD</span><span class="sxs-lookup"><span data-stu-id="61173-118">SWORD</span></span>    |           |
| <span data-ttu-id="61173-119">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="61173-119">DOUBLE</span></span>           | <span data-ttu-id="61173-120">TEMPLATE</span><span class="sxs-lookup"><span data-stu-id="61173-120">TEMPLATE</span></span> |           |



 

<span data-ttu-id="61173-121">O cabeçalho de comprimento variável é obrigatório e deve estar no início do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="61173-121">The variable-length header is compulsory and must be at the beginning of the data stream.</span></span> <span data-ttu-id="61173-122">O cabeçalho contém os dados a seguir.</span><span class="sxs-lookup"><span data-stu-id="61173-122">The header contains the following data.</span></span>



| <span data-ttu-id="61173-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="61173-123">Type</span></span>           | <span data-ttu-id="61173-124">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="61173-124">Required</span></span> | <span data-ttu-id="61173-125">Tamanho (em bytes)</span><span class="sxs-lookup"><span data-stu-id="61173-125">Size (in bytes)</span></span> | <span data-ttu-id="61173-126">Valor</span><span class="sxs-lookup"><span data-stu-id="61173-126">Value</span></span> | <span data-ttu-id="61173-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="61173-127">Description</span></span>                  |
|----------------|----------|-----------------|-------|------------------------------|
| <span data-ttu-id="61173-128">Número mágico</span><span class="sxs-lookup"><span data-stu-id="61173-128">Magic Number</span></span>   | <span data-ttu-id="61173-129">x</span><span class="sxs-lookup"><span data-stu-id="61173-129">x</span></span>        | <span data-ttu-id="61173-130">4</span><span class="sxs-lookup"><span data-stu-id="61173-130">4</span></span>               | <span data-ttu-id="61173-131">xof</span><span class="sxs-lookup"><span data-stu-id="61173-131">xof</span></span>   |                              |
| <span data-ttu-id="61173-132">Número da versão</span><span class="sxs-lookup"><span data-stu-id="61173-132">Version Number</span></span> | <span data-ttu-id="61173-133">x</span><span class="sxs-lookup"><span data-stu-id="61173-133">x</span></span>        | <span data-ttu-id="61173-134">2</span><span class="sxs-lookup"><span data-stu-id="61173-134">2</span></span>               | <span data-ttu-id="61173-135">03</span><span class="sxs-lookup"><span data-stu-id="61173-135">03</span></span>    | <span data-ttu-id="61173-136">Versão principal 3</span><span class="sxs-lookup"><span data-stu-id="61173-136">Major version 3</span></span>              |
|                |          |                 | <span data-ttu-id="61173-137">03</span><span class="sxs-lookup"><span data-stu-id="61173-137">03</span></span>    | <span data-ttu-id="61173-138">Versão secundária 3</span><span class="sxs-lookup"><span data-stu-id="61173-138">Minor version 3</span></span>              |
| <span data-ttu-id="61173-139">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="61173-139">Format Type</span></span>    | <span data-ttu-id="61173-140">x</span><span class="sxs-lookup"><span data-stu-id="61173-140">x</span></span>        | <span data-ttu-id="61173-141">4</span><span class="sxs-lookup"><span data-stu-id="61173-141">4</span></span>               | <span data-ttu-id="61173-142">txt</span><span class="sxs-lookup"><span data-stu-id="61173-142">txt</span></span>   | <span data-ttu-id="61173-143">Arquivo de texto</span><span class="sxs-lookup"><span data-stu-id="61173-143">Text File</span></span>                    |
|                |          |                 | <span data-ttu-id="61173-144">bin</span><span class="sxs-lookup"><span data-stu-id="61173-144">bin</span></span>   | <span data-ttu-id="61173-145">Arquivo binário</span><span class="sxs-lookup"><span data-stu-id="61173-145">Binary file</span></span>                  |
|                |          |                 | <span data-ttu-id="61173-146">tzip</span><span class="sxs-lookup"><span data-stu-id="61173-146">tzip</span></span>  | <span data-ttu-id="61173-147">Arquivo de texto compactado MSZip</span><span class="sxs-lookup"><span data-stu-id="61173-147">MSZip compressed text file</span></span>   |
|                |          |                 | <span data-ttu-id="61173-148">bzip</span><span class="sxs-lookup"><span data-stu-id="61173-148">bzip</span></span>  | <span data-ttu-id="61173-149">Arquivo binário compactado do MSZip</span><span class="sxs-lookup"><span data-stu-id="61173-149">MSZip compressed binary file</span></span> |
| <span data-ttu-id="61173-150">Tamanho do float</span><span class="sxs-lookup"><span data-stu-id="61173-150">Float Size</span></span>     | <span data-ttu-id="61173-151">x</span><span class="sxs-lookup"><span data-stu-id="61173-151">x</span></span>        | <span data-ttu-id="61173-152">0064</span><span class="sxs-lookup"><span data-stu-id="61173-152">0064</span></span>            |       | <span data-ttu-id="61173-153">floats de 64 bits</span><span class="sxs-lookup"><span data-stu-id="61173-153">64-bit floats</span></span>                |
|                | <span data-ttu-id="61173-154">x</span><span class="sxs-lookup"><span data-stu-id="61173-154">x</span></span>        | <span data-ttu-id="61173-155">"0032"</span><span class="sxs-lookup"><span data-stu-id="61173-155">"0032"</span></span>          |       | <span data-ttu-id="61173-156">floats de 32 bits</span><span class="sxs-lookup"><span data-stu-id="61173-156">32-bit floats</span></span>                |



 

<span data-ttu-id="61173-157">Os valores na tabela são delimitados por aspas para chamar a atenção para o número de caracteres em cada valor.</span><span class="sxs-lookup"><span data-stu-id="61173-157">The values in the table are delimited by quotes to call attention to the number of characters in each value.</span></span> <span data-ttu-id="61173-158">Aqueles com 4 bytes contêm quatro caracteres, aqueles com 2 bytes contêm dois caracteres.</span><span class="sxs-lookup"><span data-stu-id="61173-158">Those with 4 bytes contain four characters, those with 2 bytes contain two characters.</span></span>

<span data-ttu-id="61173-159">Os comentários são aplicáveis somente em arquivos de texto.</span><span class="sxs-lookup"><span data-stu-id="61173-159">Comments are applicable only in text files.</span></span> <span data-ttu-id="61173-160">Os comentários podem ocorrer em qualquer lugar no fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="61173-160">Comments can occur anywhere in the data stream.</span></span> <span data-ttu-id="61173-161">Um comentário começa com as barras duplas do estilo C++ (//) ou um sinal de sustenido ( \# ).</span><span class="sxs-lookup"><span data-stu-id="61173-161">A comment begins with either C++ style double-slashes (//), or a pound sign (\#).</span></span> <span data-ttu-id="61173-162">O comentário é executado na próxima linha nova.</span><span class="sxs-lookup"><span data-stu-id="61173-162">The comment runs to the next new line.</span></span> <span data-ttu-id="61173-163">O exemplo a seguir mostra comentários válidos.</span><span class="sxs-lookup"><span data-stu-id="61173-163">The following example shows valid comments.</span></span>


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a><span data-ttu-id="61173-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61173-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61173-165">Codificação de Texto</span><span class="sxs-lookup"><span data-stu-id="61173-165">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



