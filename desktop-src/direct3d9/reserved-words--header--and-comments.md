---
description: A tabela a seguir mostra quais palavras são reservadas e não devem ser usadas.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Palavras reservadas, cabeçalho e comentários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8879d0dbb518f92f0d8a6c38793ab315ae48b73e
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343651"
---
# <a name="reserved-words-header-and-comments"></a><span data-ttu-id="2e779-103">Palavras reservadas, cabeçalho e comentários</span><span class="sxs-lookup"><span data-stu-id="2e779-103">Reserved Words, Header, and Comments</span></span>

<span data-ttu-id="2e779-104">A tabela a seguir mostra quais palavras são reservadas e não devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="2e779-104">The table below shows which words are reserved and must not be used.</span></span>

| <span data-ttu-id="2e779-105">Palavras reservadas</span><span class="sxs-lookup"><span data-stu-id="2e779-105">Reserved Words</span></span> | <span data-ttu-id="2e779-106">Palavras reservadas</span><span class="sxs-lookup"><span data-stu-id="2e779-106">Reserved Words</span></span> | <span data-ttu-id="2e779-107">Palavras reservadas</span><span class="sxs-lookup"><span data-stu-id="2e779-107">Reserved Words</span></span>|
|------------------|----------|-----------|
| <span data-ttu-id="2e779-108">ARRAY</span><span class="sxs-lookup"><span data-stu-id="2e779-108">ARRAY</span></span>            | <span data-ttu-id="2e779-109">DWORD</span><span class="sxs-lookup"><span data-stu-id="2e779-109">DWORD</span></span>    | <span data-ttu-id="2e779-110">UCHAR</span><span class="sxs-lookup"><span data-stu-id="2e779-110">UCHAR</span></span>     |
| <span data-ttu-id="2e779-111">BINARY</span><span class="sxs-lookup"><span data-stu-id="2e779-111">BINARY</span></span>           | <span data-ttu-id="2e779-112">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2e779-112">FLOAT</span></span>    | <span data-ttu-id="2e779-113">ULONGLONG</span><span class="sxs-lookup"><span data-stu-id="2e779-113">ULONGLONG</span></span> |
| <span data-ttu-id="2e779-114">\_recurso binário</span><span class="sxs-lookup"><span data-stu-id="2e779-114">BINARY\_RESOURCE</span></span> | <span data-ttu-id="2e779-115">SDWORD</span><span class="sxs-lookup"><span data-stu-id="2e779-115">SDWORD</span></span>   | <span data-ttu-id="2e779-116">UNICODE</span><span class="sxs-lookup"><span data-stu-id="2e779-116">UNICODE</span></span>   |
| <span data-ttu-id="2e779-117">CHAR</span><span class="sxs-lookup"><span data-stu-id="2e779-117">CHAR</span></span>             | <span data-ttu-id="2e779-118">STRING</span><span class="sxs-lookup"><span data-stu-id="2e779-118">STRING</span></span>   | <span data-ttu-id="2e779-119">WORD</span><span class="sxs-lookup"><span data-stu-id="2e779-119">WORD</span></span>      |
| <span data-ttu-id="2e779-120">CSTRING</span><span class="sxs-lookup"><span data-stu-id="2e779-120">CSTRING</span></span>          | <span data-ttu-id="2e779-121">SWORD</span><span class="sxs-lookup"><span data-stu-id="2e779-121">SWORD</span></span>    |           |
| <span data-ttu-id="2e779-122">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="2e779-122">DOUBLE</span></span>           | <span data-ttu-id="2e779-123">TEMPLATE</span><span class="sxs-lookup"><span data-stu-id="2e779-123">TEMPLATE</span></span> |           |



 

<span data-ttu-id="2e779-124">O cabeçalho de comprimento variável é obrigatório e deve estar no início do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="2e779-124">The variable-length header is compulsory and must be at the beginning of the data stream.</span></span> <span data-ttu-id="2e779-125">O cabeçalho contém os dados a seguir.</span><span class="sxs-lookup"><span data-stu-id="2e779-125">The header contains the following data.</span></span>



| <span data-ttu-id="2e779-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="2e779-126">Type</span></span>           | <span data-ttu-id="2e779-127">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2e779-127">Required</span></span> | <span data-ttu-id="2e779-128">Tamanho (em bytes)</span><span class="sxs-lookup"><span data-stu-id="2e779-128">Size (in bytes)</span></span> | <span data-ttu-id="2e779-129">Valor</span><span class="sxs-lookup"><span data-stu-id="2e779-129">Value</span></span> | <span data-ttu-id="2e779-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e779-130">Description</span></span>                  |
|----------------|----------|-----------------|-------|------------------------------|
| <span data-ttu-id="2e779-131">Número mágico</span><span class="sxs-lookup"><span data-stu-id="2e779-131">Magic Number</span></span>   | <span data-ttu-id="2e779-132">x</span><span class="sxs-lookup"><span data-stu-id="2e779-132">x</span></span>        | <span data-ttu-id="2e779-133">4</span><span class="sxs-lookup"><span data-stu-id="2e779-133">4</span></span>               | <span data-ttu-id="2e779-134">xof</span><span class="sxs-lookup"><span data-stu-id="2e779-134">xof</span></span>   |                              |
| <span data-ttu-id="2e779-135">Número da versão</span><span class="sxs-lookup"><span data-stu-id="2e779-135">Version Number</span></span> | <span data-ttu-id="2e779-136">x</span><span class="sxs-lookup"><span data-stu-id="2e779-136">x</span></span>        | <span data-ttu-id="2e779-137">2</span><span class="sxs-lookup"><span data-stu-id="2e779-137">2</span></span>               | <span data-ttu-id="2e779-138">03</span><span class="sxs-lookup"><span data-stu-id="2e779-138">03</span></span>    | <span data-ttu-id="2e779-139">Versão principal 3</span><span class="sxs-lookup"><span data-stu-id="2e779-139">Major version 3</span></span>              |
|                |          |                 | <span data-ttu-id="2e779-140">03</span><span class="sxs-lookup"><span data-stu-id="2e779-140">03</span></span>    | <span data-ttu-id="2e779-141">Versão secundária 3</span><span class="sxs-lookup"><span data-stu-id="2e779-141">Minor version 3</span></span>              |
| <span data-ttu-id="2e779-142">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="2e779-142">Format Type</span></span>    | <span data-ttu-id="2e779-143">x</span><span class="sxs-lookup"><span data-stu-id="2e779-143">x</span></span>        | <span data-ttu-id="2e779-144">4</span><span class="sxs-lookup"><span data-stu-id="2e779-144">4</span></span>               | <span data-ttu-id="2e779-145">txt</span><span class="sxs-lookup"><span data-stu-id="2e779-145">txt</span></span>   | <span data-ttu-id="2e779-146">Arquivo de texto</span><span class="sxs-lookup"><span data-stu-id="2e779-146">Text File</span></span>                    |
|                |          |                 | <span data-ttu-id="2e779-147">bin</span><span class="sxs-lookup"><span data-stu-id="2e779-147">bin</span></span>   | <span data-ttu-id="2e779-148">Arquivo binário</span><span class="sxs-lookup"><span data-stu-id="2e779-148">Binary file</span></span>                  |
|                |          |                 | <span data-ttu-id="2e779-149">tzip</span><span class="sxs-lookup"><span data-stu-id="2e779-149">tzip</span></span>  | <span data-ttu-id="2e779-150">Arquivo de texto compactado MSZip</span><span class="sxs-lookup"><span data-stu-id="2e779-150">MSZip compressed text file</span></span>   |
|                |          |                 | <span data-ttu-id="2e779-151">bzip</span><span class="sxs-lookup"><span data-stu-id="2e779-151">bzip</span></span>  | <span data-ttu-id="2e779-152">Arquivo binário compactado do MSZip</span><span class="sxs-lookup"><span data-stu-id="2e779-152">MSZip compressed binary file</span></span> |
| <span data-ttu-id="2e779-153">Tamanho do float</span><span class="sxs-lookup"><span data-stu-id="2e779-153">Float Size</span></span>     | <span data-ttu-id="2e779-154">x</span><span class="sxs-lookup"><span data-stu-id="2e779-154">x</span></span>        | <span data-ttu-id="2e779-155">0064</span><span class="sxs-lookup"><span data-stu-id="2e779-155">0064</span></span>            |       | <span data-ttu-id="2e779-156">Floats de 64 bits</span><span class="sxs-lookup"><span data-stu-id="2e779-156">64-bit floats</span></span>                |
|                | <span data-ttu-id="2e779-157">x</span><span class="sxs-lookup"><span data-stu-id="2e779-157">x</span></span>        | <span data-ttu-id="2e779-158">"0032"</span><span class="sxs-lookup"><span data-stu-id="2e779-158">"0032"</span></span>          |       | <span data-ttu-id="2e779-159">Floats de 32 bits</span><span class="sxs-lookup"><span data-stu-id="2e779-159">32-bit floats</span></span>                |



 

<span data-ttu-id="2e779-160">Os valores na tabela são delimitados por aspas para chamar a atenção para o número de caracteres em cada valor.</span><span class="sxs-lookup"><span data-stu-id="2e779-160">The values in the table are delimited by quotes to call attention to the number of characters in each value.</span></span> <span data-ttu-id="2e779-161">Aqueles com 4 bytes contêm quatro caracteres, aqueles com 2 bytes contêm dois caracteres.</span><span class="sxs-lookup"><span data-stu-id="2e779-161">Those with 4 bytes contain four characters, those with 2 bytes contain two characters.</span></span>

<span data-ttu-id="2e779-162">Os comentários são aplicáveis somente em arquivos de texto.</span><span class="sxs-lookup"><span data-stu-id="2e779-162">Comments are applicable only in text files.</span></span> <span data-ttu-id="2e779-163">Os comentários podem ocorrer em qualquer lugar no fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="2e779-163">Comments can occur anywhere in the data stream.</span></span> <span data-ttu-id="2e779-164">Um comentário começa com barras duplas no estilo C++ (//) ou um sinal de quilo \# ().</span><span class="sxs-lookup"><span data-stu-id="2e779-164">A comment begins with either C++ style double-slashes (//), or a pound sign (\#).</span></span> <span data-ttu-id="2e779-165">O comentário é executado para a próxima nova linha.</span><span class="sxs-lookup"><span data-stu-id="2e779-165">The comment runs to the next new line.</span></span> <span data-ttu-id="2e779-166">O exemplo a seguir mostra comentários válidos.</span><span class="sxs-lookup"><span data-stu-id="2e779-166">The following example shows valid comments.</span></span>


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a><span data-ttu-id="2e779-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e779-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e779-168">Codificação de texto</span><span class="sxs-lookup"><span data-stu-id="2e779-168">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



