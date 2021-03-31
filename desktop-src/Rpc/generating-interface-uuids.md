---
title: Gerando UUIDs de interface
description: Gerando UUIDs (identificadores exclusivos universal) de interface e usando Uuidgen.
ms.assetid: a973b7f9-71c5-46a0-aa0c-51f150560dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c5f727ed3e37139d4da50f84c3929bff333156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635803"
---
# <a name="generating-interface-uuids"></a><span data-ttu-id="124cc-103">Gerando UUIDs de interface</span><span class="sxs-lookup"><span data-stu-id="124cc-103">Generating Interface UUIDs</span></span>

<span data-ttu-id="124cc-104">Esta seção apresenta informações sobre identificadores exclusivos universais (UUIDs) e o utilitário Uuidgen nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="124cc-104">This section presents information on Universal Unique Identifiers (UUIDs) and the Uuidgen utility in the following topics:</span></span>

-   [<span data-ttu-id="124cc-105">O que é um UUID?</span><span class="sxs-lookup"><span data-stu-id="124cc-105">What is a UUID?</span></span>](#what-is-a-uuid)
-   [<span data-ttu-id="124cc-106">Usando Uuidgen</span><span class="sxs-lookup"><span data-stu-id="124cc-106">Using Uuidgen</span></span>](#using-uuidgen)

## <a name="what-is-a-uuid"></a><span data-ttu-id="124cc-107">O que é um UUID?</span><span class="sxs-lookup"><span data-stu-id="124cc-107">What is a UUID?</span></span>

<span data-ttu-id="124cc-108">Todas as interfaces devem ser identificadas exclusivamente em uma rede para que os clientes possam encontrá-las.</span><span class="sxs-lookup"><span data-stu-id="124cc-108">All interfaces must be uniquely identified on a network so that clients can find them.</span></span> <span data-ttu-id="124cc-109">Em redes pequenas, o nome da interface sozinha pode ser suficiente para identificá-la.</span><span class="sxs-lookup"><span data-stu-id="124cc-109">On small networks, the interface's name alone may be sufficient to identify it.</span></span> <span data-ttu-id="124cc-110">No entanto, isso geralmente não é viável em redes grandes.</span><span class="sxs-lookup"><span data-stu-id="124cc-110">However, that is usually not feasible on large networks.</span></span> <span data-ttu-id="124cc-111">Portanto, os desenvolvedores normalmente atribuem um identificador exclusivo universal (UUID, intercambiável com o termo GUID ou identificador global exclusivo) para cada interface.</span><span class="sxs-lookup"><span data-stu-id="124cc-111">Therefore, developers typically assign a Universal Unique Identifier (UUID, interchangeable with the term GUID, or Globally Unique Identifier) to each interface.</span></span> <span data-ttu-id="124cc-112">Um UUID é uma cadeia de caracteres que contém um conjunto de dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="124cc-112">A UUID is a string that contains a set of hexadecimal digits.</span></span> <span data-ttu-id="124cc-113">Cada interface tem um UUID diferente.</span><span class="sxs-lookup"><span data-stu-id="124cc-113">Each interface has a different UUID.</span></span> <span data-ttu-id="124cc-114">Para obter detalhes, consulte [UUID de cadeia de caracteres](string-uuid.md).</span><span class="sxs-lookup"><span data-stu-id="124cc-114">For details, see [String UUID](string-uuid.md).</span></span>

<span data-ttu-id="124cc-115">A representação textual de um UUID é uma cadeia de caracteres que consiste em 8 dígitos hexadecimais seguidos por um hífen, seguido por três grupos separados por hífen de 4 dígitos hexadecimais, seguidos por um hífen, seguido por 12 dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="124cc-115">The textual representation of a UUID is a string consisting of 8 hexadecimal digits followed by a hyphen, followed by three hyphen-separated groups of 4 hexadecimal digits, followed by a hyphen, followed by 12 hexadecimal digits.</span></span> <span data-ttu-id="124cc-116">O exemplo a seguir é uma cadeia de caracteres UUID válida:</span><span class="sxs-lookup"><span data-stu-id="124cc-116">The following example is a valid UUID string:</span></span>

<span data-ttu-id="124cc-117">ba209999-0c6c-11d2-97cf-00c04f8eea45</span><span class="sxs-lookup"><span data-stu-id="124cc-117">ba209999-0c6c-11d2-97cf-00c04f8eea45</span></span>

<span data-ttu-id="124cc-118">Os UUIDs vazios são referidos como UUIDs Nil em vez de UUIDs **nulos** .</span><span class="sxs-lookup"><span data-stu-id="124cc-118">Empty UUIDs are referred to as nil UUIDs rather than **NULL** UUIDs.</span></span> <span data-ttu-id="124cc-119">O termo nil indica qualquer coisa que seja zero, em branco, vazio ou não inicializado.</span><span class="sxs-lookup"><span data-stu-id="124cc-119">The term nil indicates anything that is zero, blank, empty, or uninitialized.</span></span> <span data-ttu-id="124cc-120">Uma cadeia de caracteres vazia, um registro de banco de dados vazio ou um UUID não inicializado são exemplos de valores nulos.</span><span class="sxs-lookup"><span data-stu-id="124cc-120">An empty string, an empty database record, or an uninitialized UUID are all examples of nil values.</span></span>

> [!Note]  
> <span data-ttu-id="124cc-121">O valor **NULL** é o valor especificado zero.</span><span class="sxs-lookup"><span data-stu-id="124cc-121">The value **NULL** is the specific value zero.</span></span> <span data-ttu-id="124cc-122">Ele é frequentemente usado em programação C e C++ em conjunto com ponteiros.</span><span class="sxs-lookup"><span data-stu-id="124cc-122">It is often used in C and C++ programming in conjunction with pointers.</span></span> <span data-ttu-id="124cc-123">Nil é um termo mais geral do que **NULL**.</span><span class="sxs-lookup"><span data-stu-id="124cc-123">Nil is a more general term than **NULL**.</span></span> <span data-ttu-id="124cc-124">Os UUIDs de interface de objeto não inicializados sempre devem ser chamados de UUIDs **nulos** em vez de UUIDs NULL.</span><span class="sxs-lookup"><span data-stu-id="124cc-124">Uninitialized object interface UUIDs should always be referred to as nil UUIDs rather than **NULL** UUIDs.</span></span>

 

## <a name="using-uuidgen"></a><span data-ttu-id="124cc-125">Usando Uuidgen</span><span class="sxs-lookup"><span data-stu-id="124cc-125">Using Uuidgen</span></span>

<span data-ttu-id="124cc-126">A Microsoft fornece um programa utilitário chamado Uuidgen para gerar os UUIDs.</span><span class="sxs-lookup"><span data-stu-id="124cc-126">Microsoft provides a utility program called Uuidgen to generate your UUIDs.</span></span> <span data-ttu-id="124cc-127">O utilitário Uuidgen gera o UUID no formato de arquivo IDL ou no formato C-Language.</span><span class="sxs-lookup"><span data-stu-id="124cc-127">The Uuidgen utility generates the UUID in IDL file format or C-language format.</span></span>

<span data-ttu-id="124cc-128">Ao executar o utilitário Uuidgen na linha de comando, você pode usar as seguintes opções de comando.</span><span class="sxs-lookup"><span data-stu-id="124cc-128">When you run the Uuidgen utility from the command line, you can use the following command switches.</span></span>



| <span data-ttu-id="124cc-129">Comutador Uuidgen</span><span class="sxs-lookup"><span data-stu-id="124cc-129">Uuidgen switch</span></span>           | <span data-ttu-id="124cc-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="124cc-130">Description</span></span>                                                                |
|--------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="124cc-131">**/I**</span><span class="sxs-lookup"><span data-stu-id="124cc-131">**/I**</span></span>                   | <span data-ttu-id="124cc-132">Gera UUID para um modelo de interface IDL.</span><span class="sxs-lookup"><span data-stu-id="124cc-132">Outputs UUID to an IDL interface template.</span></span>                                 |
| <span data-ttu-id="124cc-133">**/s**</span><span class="sxs-lookup"><span data-stu-id="124cc-133">**/s**</span></span>                   | <span data-ttu-id="124cc-134">Gera UUID como uma estrutura C inicializada.</span><span class="sxs-lookup"><span data-stu-id="124cc-134">Outputs UUID as an initialized C structure.</span></span>                                |
| <span data-ttu-id="124cc-135">**/o** < *nome do arquivo*></span><span class="sxs-lookup"><span data-stu-id="124cc-135">**/o**<*filename*></span></span> | <span data-ttu-id="124cc-136">Redireciona a saída para um arquivo; especificado imediatamente após a opção **/o** .</span><span class="sxs-lookup"><span data-stu-id="124cc-136">Redirects output to a file; specified immediately after the **/o** switch.</span></span> |
| <span data-ttu-id="124cc-137">**/n** < *número* de></span><span class="sxs-lookup"><span data-stu-id="124cc-137">**/n**<*number*></span></span>   | <span data-ttu-id="124cc-138">Especifica o número de UUIDs a serem gerados.</span><span class="sxs-lookup"><span data-stu-id="124cc-138">Specifies the number of UUIDs to generate.</span></span>                                 |
| <span data-ttu-id="124cc-139">**/v**</span><span class="sxs-lookup"><span data-stu-id="124cc-139">**/v**</span></span>                   | <span data-ttu-id="124cc-140">Exibe informações de versão sobre Uuidgen.</span><span class="sxs-lookup"><span data-stu-id="124cc-140">Displays version information about Uuidgen.</span></span>                                |
| <span data-ttu-id="124cc-141">**/h** ou **?**</span><span class="sxs-lookup"><span data-stu-id="124cc-141">**/h** or **?**</span></span>          | <span data-ttu-id="124cc-142">Exibe o resumo da opção de comando.</span><span class="sxs-lookup"><span data-stu-id="124cc-142">Displays command-option summary.</span></span>                                           |



 

<span data-ttu-id="124cc-143">Normalmente, você usará o utilitário Uuidgen, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="124cc-143">Typically, you will use the Uuidgen utility as shown in the following example.</span></span>

<span data-ttu-id="124cc-144">**Uuidgen-i-oMyApp. idl**</span><span class="sxs-lookup"><span data-stu-id="124cc-144">**uuidgen -i -oMyApp.idl**</span></span>

<span data-ttu-id="124cc-145">Esse comando gera um UUID e o armazena em um arquivo MIDL que você pode usar como modelo.</span><span class="sxs-lookup"><span data-stu-id="124cc-145">This command generates a UUID and stores it in a MIDL file that you can use as a template.</span></span> <span data-ttu-id="124cc-146">Quando o comando anterior é executado, o conteúdo de MyApp. idl é semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="124cc-146">When the preceding command is executed, the contents of MyApp.idl are similar to the following:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

<span data-ttu-id="124cc-147">A próxima etapa seria substituir o nome do espaço reservado, INTERFACENAME, pelo nome real da sua interface.</span><span class="sxs-lookup"><span data-stu-id="124cc-147">The next step would be to replace the placeholder name, INTERFACENAME, with the actual name of your interface.</span></span>

 

 




