---
description: Os modelos definem como o fluxo de dados é interpretado-os dados são modulados pela definição do modelo. Esta seção aborda os seguintes aspectos de um modelo e fornece um modelo de exemplo.
ms.assetid: f84978a8-8315-4626-be68-f00f3a72e5ac
title: Modelos (formato de arquivo X, codificação de texto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fccec46e72a73bb5ed4434fd252595e1b072ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645622"
---
# <a name="templates-x-file-format-text-encoding"></a><span data-ttu-id="e2cf4-104">Modelos (formato de arquivo X, codificação de texto)</span><span class="sxs-lookup"><span data-stu-id="e2cf4-104">Templates (X file format, text encoding)</span></span>

<span data-ttu-id="e2cf4-105">Os modelos definem como o fluxo de dados é interpretado-os dados são modulados pela definição do modelo.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-105">Templates define how the data stream is interpreted - the data is modulated by the template definition.</span></span> <span data-ttu-id="e2cf4-106">Esta seção aborda os seguintes aspectos de um modelo e fornece um modelo de exemplo.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-106">This section discusses the following aspects of a template and provides an example template.</span></span>

<span data-ttu-id="e2cf4-107">Há um modelo especial – o modelo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-107">There is one special template - the header template.</span></span> <span data-ttu-id="e2cf4-108">É recomendável que cada aplicativo defina um modelo de cabeçalho e use-o para definir informações específicas do aplicativo, como informações de versão.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-108">It is recommended that each application define a header template and use it to define application-specific information, such as version information.</span></span> <span data-ttu-id="e2cf4-109">Se estiver presente, esse cabeçalho será lido pela API de formato de arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-109">If present, this header is read by the .x file format API.</span></span> <span data-ttu-id="e2cf4-110">Se um membro flags estiver disponível, ele será usado para determinar como os dados a seguir são interpretados.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-110">If a flags member is available, it is used to determine how the following data is interpreted.</span></span> <span data-ttu-id="e2cf4-111">O membro flags, se definido, deve ser um DWORD.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-111">The flags member, if defined, should be a DWORD.</span></span> <span data-ttu-id="e2cf4-112">Um bit está definido no momento-bit 0.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-112">One bit is currently defined - bit 0.</span></span> <span data-ttu-id="e2cf4-113">Se esse bit estiver claro, os dados a seguir no arquivo serão binários.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-113">If this bit is clear, the following data in the file is binary.</span></span> <span data-ttu-id="e2cf4-114">Se definido, os dados a seguir são texto.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-114">If set, the following data is text.</span></span> <span data-ttu-id="e2cf4-115">Você pode usar vários objetos de dados de cabeçalho para alternar entre o binário e o texto dentro do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-115">You can use multiple header data objects to switch between binary and text within the file.</span></span>

## <a name="template-form-name-and-uuid"></a><span data-ttu-id="e2cf4-116">Formato, nome e UUID do modelo</span><span class="sxs-lookup"><span data-stu-id="e2cf4-116">Template Form, Name, and UUID</span></span>

<span data-ttu-id="e2cf4-117">Um modelo tem o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-117">A template has the following form.</span></span>


```
template <template-name> {
<UUID>
    <member 1>;
...
    <member n>;
[restrictions]
}
```



<span data-ttu-id="e2cf4-118">O nome do modelo é um nome alfanumérico que pode incluir o caractere de sublinhado ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="e2cf4-118">The template name is an alphanumeric name that can include the underscore character (\_).</span></span> <span data-ttu-id="e2cf4-119">Ele não deve começar com um dígito.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-119">It must not begin with a digit.</span></span> <span data-ttu-id="e2cf4-120">O UUID é um identificador universalmente exclusivo formatado para o padrão de ambiente de computação distribuído da Open Software Foundation e envolto por colchetes angulares (< >).</span><span class="sxs-lookup"><span data-stu-id="e2cf4-120">The UUID is a universally unique identifier formatted to the Open Software Foundation's Distributed Computing Environment standard and enclosed by angle brackets (< >).</span></span> <span data-ttu-id="e2cf4-121">Por exemplo: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-121">For example: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.</span></span>

## <a name="template-members"></a><span data-ttu-id="e2cf4-122">Membros do modelo</span><span class="sxs-lookup"><span data-stu-id="e2cf4-122">Template Members</span></span>

<span data-ttu-id="e2cf4-123">Os membros do modelo consistem em um tipo de dados nomeado seguido por um nome opcional ou uma matriz de um tipo de dados nomeado.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-123">Template members consist of a named data type followed by an optional name or an array of a named data type.</span></span> <span data-ttu-id="e2cf4-124">Os tipos de dados primitivos válidos são definidos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-124">Valid primitive data types are defined in the following table.</span></span>



| <span data-ttu-id="e2cf4-125">Type</span><span class="sxs-lookup"><span data-stu-id="e2cf4-125">Type</span></span>    | <span data-ttu-id="e2cf4-126">Tamanho</span><span class="sxs-lookup"><span data-stu-id="e2cf4-126">Size</span></span>                               |
|---------|------------------------------------|
| <span data-ttu-id="e2cf4-127">WORD</span><span class="sxs-lookup"><span data-stu-id="e2cf4-127">WORD</span></span>    | <span data-ttu-id="e2cf4-128">16 bits</span><span class="sxs-lookup"><span data-stu-id="e2cf4-128">16 bits</span></span>                            |
| <span data-ttu-id="e2cf4-129">DWORD</span><span class="sxs-lookup"><span data-stu-id="e2cf4-129">DWORD</span></span>   | <span data-ttu-id="e2cf4-130">32 bits</span><span class="sxs-lookup"><span data-stu-id="e2cf4-130">32 bits</span></span>                            |
| <span data-ttu-id="e2cf4-131">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e2cf4-131">FLOAT</span></span>   | <span data-ttu-id="e2cf4-132">IEEE float</span><span class="sxs-lookup"><span data-stu-id="e2cf4-132">IEEE float</span></span>                         |
| <span data-ttu-id="e2cf4-133">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="e2cf4-133">DOUBLE</span></span>  | <span data-ttu-id="e2cf4-134">64 bits</span><span class="sxs-lookup"><span data-stu-id="e2cf4-134">64 bits</span></span>                            |
| <span data-ttu-id="e2cf4-135">CHAR</span><span class="sxs-lookup"><span data-stu-id="e2cf4-135">CHAR</span></span>    | <span data-ttu-id="e2cf4-136">8 bits</span><span class="sxs-lookup"><span data-stu-id="e2cf4-136">8 bits</span></span>                             |
| <span data-ttu-id="e2cf4-137">UCHAR</span><span class="sxs-lookup"><span data-stu-id="e2cf4-137">UCHAR</span></span>   | <span data-ttu-id="e2cf4-138">8 bits</span><span class="sxs-lookup"><span data-stu-id="e2cf4-138">8 bits</span></span>                             |
| <span data-ttu-id="e2cf4-139">BYTE</span><span class="sxs-lookup"><span data-stu-id="e2cf4-139">BYTE</span></span>    | <span data-ttu-id="e2cf4-140">8 bits</span><span class="sxs-lookup"><span data-stu-id="e2cf4-140">8 bits</span></span>                             |
| <span data-ttu-id="e2cf4-141">STRING</span><span class="sxs-lookup"><span data-stu-id="e2cf4-141">STRING</span></span>  | <span data-ttu-id="e2cf4-142">Cadeia de caracteres terminada nula</span><span class="sxs-lookup"><span data-stu-id="e2cf4-142">NULL terminated string</span></span>             |
| <span data-ttu-id="e2cf4-143">CSTRING</span><span class="sxs-lookup"><span data-stu-id="e2cf4-143">CSTRING</span></span> | <span data-ttu-id="e2cf4-144">Cadeia de caracteres C formatada (sem suporte)</span><span class="sxs-lookup"><span data-stu-id="e2cf4-144">Formatted C string (not supported)</span></span> |
| <span data-ttu-id="e2cf4-145">UNICODE</span><span class="sxs-lookup"><span data-stu-id="e2cf4-145">UNICODE</span></span> | <span data-ttu-id="e2cf4-146">Cadeia de caracteres Unicode (sem suporte)</span><span class="sxs-lookup"><span data-stu-id="e2cf4-146">Unicode string (not supported)</span></span>     |



 

<span data-ttu-id="e2cf4-147">Tipos de dados adicionais definidos por modelos encontrados anteriormente no fluxo de dados também podem ser referenciados dentro de uma definição de modelo.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-147">Additional data types defined by templates encountered earlier in the data stream can also be referenced within a template definition.</span></span> <span data-ttu-id="e2cf4-148">Nenhuma referência progressiva é permitida.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-148">No forward references are allowed.</span></span>

<span data-ttu-id="e2cf4-149">Qualquer tipo de dados válido pode ser expresso como uma matriz na definição do modelo.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-149">Any valid data type can be expressed as an array in the template definition.</span></span> <span data-ttu-id="e2cf4-150">A sintaxe básica é mostrada no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-150">The basic syntax is shown in the following example.</span></span>


```
array <data-type> <name>[<dimension-size>];
```



<span data-ttu-id="e2cf4-151"><> de dimensão pode ser um inteiro ou uma referência nomeada a outro membro de modelo cujo valor seja substituído.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-151"><dimension-size> can either be an integer or a named reference to another template member whose value is then substituted.</span></span> <span data-ttu-id="e2cf4-152">As matrizes podem ser n-dimensional, em que n é determinado pelo número de colchetes emparelhados que se enquadram na instrução, como no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-152">Arrays can be n-dimensional, where n is determined by the number of paired square brackets trailing the statement, as in the following example.</span></span>


```
array DWORD FixedHerd[24];
array DWORD Herd[nCows];
array FLOAT Matrix4x4[4][4];
```



## <a name="template-restrictions"></a><span data-ttu-id="e2cf4-153">Restrições de modelo</span><span class="sxs-lookup"><span data-stu-id="e2cf4-153">Template Restrictions</span></span>

<span data-ttu-id="e2cf4-154">Os modelos podem ser abertos, fechados ou restritos.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-154">Templates can be open, closed, or restricted.</span></span> <span data-ttu-id="e2cf4-155">Essas restrições determinam quais tipos de dados podem aparecer na hierarquia imediata de um objeto de dados definido pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-155">These restrictions determine which data types can appear in the immediate hierarchy of a data object defined by the template.</span></span> <span data-ttu-id="e2cf4-156">Um modelo aberto não tem restrições, um modelo fechado rejeita todos os tipos de dados e um modelo restrito permite uma lista nomeada de tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-156">An open template has no restrictions, a closed template rejects all data types, and a restricted template allows a named list of data types.</span></span>

<span data-ttu-id="e2cf4-157">A sintaxe para indicar um modelo aberto é de três períodos entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-157">The syntax for indicating an open template is three periods enclosed by square brackets.</span></span>


```
[ ... ]
```



<span data-ttu-id="e2cf4-158">Uma lista separada por vírgulas de tipos de dados nomeados seguidos opcionalmente por seus UUIDs delimitados por colchetes indica um modelo restrito.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-158">A comma-separated list of named data types followed optionally by their UUIDs enclosed by square brackets indicates a restricted template.</span></span>


```
[ { data-type [ UUID ] , } ... ]
```



<span data-ttu-id="e2cf4-159">A ausência de qualquer um dos itens acima indica um modelo fechado.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-159">The absence of either of the above indicates a closed template.</span></span>

## <a name="template-example"></a><span data-ttu-id="e2cf4-160">Exemplo de modelo</span><span class="sxs-lookup"><span data-stu-id="e2cf4-160">Template Example</span></span>

<span data-ttu-id="e2cf4-161">O exemplo a seguir mostra um modelo.</span><span class="sxs-lookup"><span data-stu-id="e2cf4-161">The following shows an example template.</span></span>


```
template Mesh {
<3D82AB44-62DA-11cf-AB39-0020AF71E433>
DWORD nVertices;
array Vector vertices[nVertices];
DWORD nFaces;
array MeshFace faces[nFaces];
 [ ... ]                // An open template
}
template Vector {
<3D82AB5E-62DA-11cf-AB39-0020AF71E433>
FLOAT x;
FLOAT y;
FLOAT z;
}                        // A closed template
template FileSystem {
<UUID>
STRING name;
[ Directory <UUID>, File <UUID> ]    // A restricted template
}
```



## <a name="related-topics"></a><span data-ttu-id="e2cf4-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2cf4-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2cf4-163">Codificação de Texto</span><span class="sxs-lookup"><span data-stu-id="e2cf4-163">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



