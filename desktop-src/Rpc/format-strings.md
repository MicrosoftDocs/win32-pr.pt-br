---
title: Cadeias de caracteres de formato
description: Uma cadeia de caracteres de formato é um token interpretado que o mecanismo de NDR compreende. Cadeias de caracteres de formato costumam ser chamadas de MOPs; Esta documentação usa a cadeia de caracteres de formato de termo em todo o.
ms.assetid: 548283bd-023a-41dd-b1d0-661305d019e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563dd9e4145a7d83b2e49f180329c05c1d55155d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636211"
---
# <a name="format-strings"></a><span data-ttu-id="a6b3a-104">Cadeias de caracteres de formato</span><span class="sxs-lookup"><span data-stu-id="a6b3a-104">Format Strings</span></span>

<span data-ttu-id="a6b3a-105">Uma cadeia de caracteres de formato é um token interpretado que o mecanismo de NDR compreende.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-105">A format string is an interpreted token that the NDR engine understands.</span></span> <span data-ttu-id="a6b3a-106">Cadeias de caracteres de formato costumam ser chamadas de MOPs; Esta documentação usa a cadeia de caracteres de formato de termo em todo o.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-106">Format strings are often referred to as MOPs; this documentation uses the term format string throughout.</span></span>

<span data-ttu-id="a6b3a-107">Para ser mais preciso, um caractere de formato é um token interpretável individual (atômico).</span><span class="sxs-lookup"><span data-stu-id="a6b3a-107">To be more precise, a format character is an individual (atomic) interpretable token.</span></span> <span data-ttu-id="a6b3a-108">Cada caractere de formato tem um byte de tamanho.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-108">Each format character is one byte in size.</span></span> <span data-ttu-id="a6b3a-109">Uma cadeia de caracteres de formato é uma sequência de caracteres de formato ou caracteres de formato e dados numéricos.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-109">A format string is a sequence of format characters or format characters and numerical data.</span></span> <span data-ttu-id="a6b3a-110">O descritor de termo também é usado para nomear sequências comuns; por exemplo, uma cadeia de caracteres de formato de parâmetro ou um descritor de parâmetro é uma cadeia de caracteres de formato usada para descrever um parâmetro de uma rotina.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-110">The term descriptor is also used for naming common sequences; for example, a parameter format string or a parameter descriptor is a format string used to describe a parameter of a routine.</span></span>

<span data-ttu-id="a6b3a-111">Os caracteres de formato têm nomes simbólicos sugeridos como FC \_ longo ou FC \_ struct.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-111">Format characters have suggestive symbolic names like FC\_LONG or FC\_STRUCT.</span></span> <span data-ttu-id="a6b3a-112">Todos os caracteres de cadeia de formato usados pelo MIDL e pelo mecanismo de NDR são definidos no arquivo Ndrtypes. h.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-112">All format string characters used by MIDL and the NDR engine are defined in the Ndrtypes.h file.</span></span>

## <a name="format-string-tables"></a><span data-ttu-id="a6b3a-113">Formatar tabelas de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="a6b3a-113">Format String Tables</span></span>

<span data-ttu-id="a6b3a-114">Duas tabelas de cadeia de caracteres de formato primário são usadas pelo mecanismo: a tabela de cadeia de caracteres de formato de procedimento, **\_ \_ MIDL \_ ProcFormatString**, que mantém os descritores de procedimento; e a tabela de cadeia de caracteres de formato de tipo, **\_ \_ MIDL \_ TypeFormatString**, que mantém os descritores de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-114">Two primary format string tables are used by the engine: the procedure format string table, **\_\_MIDL\_ProcFormatString**, that keeps the procedure descriptors; and the type format string table, **\_\_MIDL\_TypeFormatString**, that keeps the data type descriptors.</span></span> <span data-ttu-id="a6b3a-115">O compilador gera ambos os arquivos stub principais ( \* \_ c. c, \* \_ s. c, \* \_ p. c).</span><span class="sxs-lookup"><span data-stu-id="a6b3a-115">The compiler generates both into the main stub files (\*\_c.c, \*\_s.c, \*\_p.c).</span></span> <span data-ttu-id="a6b3a-116">A tabela de cadeia de caracteres de formato de procedimento é usada principalmente por vários interpretadores, mas também é usada para a conversão de buffer, independentemente do modo de compilador.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-116">The procedure format string table is used mostly by various interpreters but it is also used for the buffer conversion regardless of the compiler mode.</span></span> <span data-ttu-id="a6b3a-117">A tabela de cadeia de caracteres de formato de tipo é usada ao chamar o mecanismo de NDR principal para indicar os tipos de dados específicos nos quais trabalhar.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-117">The type format string table is used when calling the core NDR engine to indicate specific data types to be worked on.</span></span>

## <a name="format-string-notation"></a><span data-ttu-id="a6b3a-118">Formatar notação de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="a6b3a-118">Format String Notation</span></span>

<span data-ttu-id="a6b3a-119">A notação usada neste documento segue as diretrizes de descrição de programação comuns, com uma barra ( \| ) usada para denotar construções alternativas e colchetes ( \[ \] ) usados para indicar elementos opcionais.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-119">The notation used in this document follows common programming description guidelines, with a bar ( \| ) used to denote alternative constructs and square brackets ( \[ \] ) used to indicate optional elements.</span></span> <span data-ttu-id="a6b3a-120">As cadeias de caracteres de formato são frequentemente empilhadas para facilitar a leitura (responsabilidade).</span><span class="sxs-lookup"><span data-stu-id="a6b3a-120">Format strings are frequently stacked up for readability (accountability).</span></span> <span data-ttu-id="a6b3a-121">Em todo este documento, o FC denota um único caractere de formato.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-121">Throughout this document, FC denotes a single format character.</span></span> <span data-ttu-id="a6b3a-122">Os caracteres de formato são apresentados em todos os limites, usando seus nomes simbólicos reais.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-122">Format characters are presented in all CAPS, using their actual symbolic names.</span></span> <span data-ttu-id="a6b3a-123">Outros campos arbitrários são representados por um nome e um tamanho.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-123">Other arbitrary fields are represented by a name and a size.</span></span>

<span data-ttu-id="a6b3a-124">Os colchetes angulares ( <> ) são usados para denotar os tamanhos dos descritores.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-124">Angle brackets ( <> ) are used to denote sizes of the descriptors.</span></span> <span data-ttu-id="a6b3a-125">As convenções mostradas na tabela a seguir são empregadas.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-125">The conventions shown in the following table are employed.</span></span>



| <span data-ttu-id="a6b3a-126">Notation</span><span class="sxs-lookup"><span data-stu-id="a6b3a-126">Notation</span></span>     | <span data-ttu-id="a6b3a-127">Significado</span><span class="sxs-lookup"><span data-stu-id="a6b3a-127">Meaning</span></span>                                                   |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="a6b3a-128"><*p*></span><span class="sxs-lookup"><span data-stu-id="a6b3a-128"><*n*></span></span>  | <span data-ttu-id="a6b3a-129">O tamanho do descritor é n bytes.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-129">The size of descriptor is n bytes.</span></span>                        |
| <>     | <span data-ttu-id="a6b3a-130">O tamanho do descritor varia.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-130">The size of descriptor varies.</span></span>                            |
| <span data-ttu-id="a6b3a-131">{<>}\*</span><span class="sxs-lookup"><span data-stu-id="a6b3a-131">{<>}\*</span></span> | <span data-ttu-id="a6b3a-132">O descritor é repetido qualquer número de vezes (0, 1, 2...).</span><span class="sxs-lookup"><span data-stu-id="a6b3a-132">The descriptor is repeated any number of times (0,1,2 …).</span></span> |



 

<span data-ttu-id="a6b3a-133">Os caracteres de formato a seguir têm um significado especial.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-133">The following format characters have a special meaning.</span></span>



| <span data-ttu-id="a6b3a-134">Caractere</span><span class="sxs-lookup"><span data-stu-id="a6b3a-134">Character</span></span> | <span data-ttu-id="a6b3a-135">Significado</span><span class="sxs-lookup"><span data-stu-id="a6b3a-135">Meaning</span></span>                                   |
|-----------|-------------------------------------------|
| <span data-ttu-id="a6b3a-136">extremidade de FC \_</span><span class="sxs-lookup"><span data-stu-id="a6b3a-136">FC\_END</span></span>   | <span data-ttu-id="a6b3a-137">Indica o fim de algumas cadeias de caracteres de formato.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-137">Indicates the end of some format strings.</span></span> |
| <span data-ttu-id="a6b3a-138">Pad do FC \_</span><span class="sxs-lookup"><span data-stu-id="a6b3a-138">FC\_PAD</span></span>   | <span data-ttu-id="a6b3a-139">Caractere de preenchimento não interpretado.</span><span class="sxs-lookup"><span data-stu-id="a6b3a-139">Uninterpreted pad character.</span></span>              |



 

 

 




