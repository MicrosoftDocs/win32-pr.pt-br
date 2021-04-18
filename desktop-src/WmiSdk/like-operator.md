---
description: O operador LIKE determina se uma cadeia de caracteres corresponde ou não a um padrão especificado.
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: Operador LIKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9091f44dd131d5d2c30d2d46aa4fc109dcdf02b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807200"
---
# <a name="like-operator"></a><span data-ttu-id="08b4d-103">Operador LIKE</span><span class="sxs-lookup"><span data-stu-id="08b4d-103">LIKE Operator</span></span>

<span data-ttu-id="08b4d-104">O operador LIKE determina se uma cadeia de caracteres corresponde ou não a um padrão especificado.</span><span class="sxs-lookup"><span data-stu-id="08b4d-104">The LIKE operator determines whether or not a character string matches a specified pattern.</span></span> <span data-ttu-id="08b4d-105">O padrão especificado pode conter exatamente os caracteres a serem correspondidos ou pode conter caracteres meta.</span><span class="sxs-lookup"><span data-stu-id="08b4d-105">The specified pattern can contain exactly the characters to match, or it can contain meta characters.</span></span> <span data-ttu-id="08b4d-106">Na verdade, o operador LIKE corresponde a subcadeias usando os caracteres curinga na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="08b4d-106">In effect, the LIKE operator matches substrings using the wildcard characters in the following table.</span></span>



| <span data-ttu-id="08b4d-107">Caractere</span><span class="sxs-lookup"><span data-stu-id="08b4d-107">Character</span></span>       | <span data-ttu-id="08b4d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="08b4d-108">Description</span></span>                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08b4d-109">\[ \]</span><span class="sxs-lookup"><span data-stu-id="08b4d-109">\[ \]</span></span>           | <span data-ttu-id="08b4d-110">Qualquer caractere dentro do intervalo especificado ( \[ a-f \] ) ou conjunto ( \[ abcdef \] ).</span><span class="sxs-lookup"><span data-stu-id="08b4d-110">Any one character within the specified range (\[a-f\]) or set (\[abcdef\]).</span></span>                                                                                                                 |
| ^               | <span data-ttu-id="08b4d-111">Qualquer caractere que não esteja dentro do intervalo ( \[ ^ a-f \] ) ou definido ( \[ ^ abcdef \] .)</span><span class="sxs-lookup"><span data-stu-id="08b4d-111">Any one character not within the range (\[^a-f\]) or set (\[^abcdef\].)</span></span>                                                                                                                     |
| %               | <span data-ttu-id="08b4d-112">Qualquer cadeia de caracteres igual a 0 (zero) ou mais.</span><span class="sxs-lookup"><span data-stu-id="08b4d-112">Any string of 0 (zero) or more characters.</span></span> <span data-ttu-id="08b4d-113">O exemplo a seguir localiza todas as instâncias em que "win" é encontrado em qualquer lugar no nome da classe: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"`</span><span class="sxs-lookup"><span data-stu-id="08b4d-113">The following example finds all instances where "Win" is found anywhere in the class name: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"`</span></span> |
| <span data-ttu-id="08b4d-114">\_ sublinhado</span><span class="sxs-lookup"><span data-stu-id="08b4d-114">\_ (underscore)</span></span> | <span data-ttu-id="08b4d-115">Qualquer caractere.</span><span class="sxs-lookup"><span data-stu-id="08b4d-115">Any one character.</span></span> <span data-ttu-id="08b4d-116">Qualquer sublinhado literal usado na cadeia de caracteres de consulta deve ser ignorado colocando-o dentro \[ \] (colchetes).</span><span class="sxs-lookup"><span data-stu-id="08b4d-116">Any literal underscore used in the query string must be escaped by placing it inside \[\] (square brackets).</span></span>                                                             |



 

<span data-ttu-id="08b4d-117">Por exemplo, o código de PowerShell a seguir recupera todas as instâncias da classe de **\_ OperatingSystem do Win32** cuja propriedade **Name** começa com **FirstName**:</span><span class="sxs-lookup"><span data-stu-id="08b4d-117">For example, the following Power shell code retrieves all instances of the **Win32\_operatingSystem** class whose **Name** property begins with **FirstName**:</span></span>

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

<span data-ttu-id="08b4d-118">Como o sublinhado é um caractere de meta, se o destino da consulta tiver um sublinhado, os \[ \] caracteres de escape deverão colocá-lo.</span><span class="sxs-lookup"><span data-stu-id="08b4d-118">Because the underscore is a meta character, if the query target has an underscore, the "\[\]" escape characters must surround it.</span></span> <span data-ttu-id="08b4d-119">Por exemplo, você pode consultar todas as classes que têm um sublinhado duplo no nome.</span><span class="sxs-lookup"><span data-stu-id="08b4d-119">For example, you can query for all the classes that have a double underscore in the name.</span></span>

<span data-ttu-id="08b4d-120">Para localizar todas as classes com um sublinhado duplo no nome, você deve escapar os dois sublinhados com \[ \] (colchetes), por exemplo:</span><span class="sxs-lookup"><span data-stu-id="08b4d-120">To locate all classes with a double underscore in the name, you must escape both underscores with \[\] (square brackets), for example:</span></span>

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

<span data-ttu-id="08b4d-121">Você pode negar uma instrução LIKE usando NOT; para fazer isso, certifique-se de inserir o não diretamente na frente do nome do campo.</span><span class="sxs-lookup"><span data-stu-id="08b4d-121">You can negate a LIKE statement using NOT; to do so, be sure to place the NOT directly in front of the field name.</span></span> <span data-ttu-id="08b4d-122">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="08b4d-122">For example:</span></span>

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a><span data-ttu-id="08b4d-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08b4d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08b4d-124">Operadores WQL</span><span class="sxs-lookup"><span data-stu-id="08b4d-124">WQL Operators</span></span>](wql-operators.md)
</dt> </dl>

 

 



