---
title: Convertendo para Visual Basic do C++
description: Convertendo para Visual Basic do C++
ms.assetid: fce7ea25-cb24-4cc4-8f36-0e8aed2f3ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba519cbdb0305fe3a2eae4cc8e658fdde1eac3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105750347"
---
# <a name="translating-to-visual-basic-from-c"></a><span data-ttu-id="19f3a-103">Convertendo para Visual Basic do C++</span><span class="sxs-lookup"><span data-stu-id="19f3a-103">Translating to Visual Basic from C++</span></span>

<span data-ttu-id="19f3a-104">Usando a linguagem de programação C++, os desenvolvedores podem acessar diretamente a memória que armazena uma variável específica.</span><span class="sxs-lookup"><span data-stu-id="19f3a-104">Using the C++ programming language, developers can directly access the memory that stores a particular variable.</span></span> <span data-ttu-id="19f3a-105">Os ponteiros de memória fornecem esse acesso direto.</span><span class="sxs-lookup"><span data-stu-id="19f3a-105">Memory pointers provide this direct access.</span></span> <span data-ttu-id="19f3a-106">No Visual Basic, os ponteiros são tratados para você.</span><span class="sxs-lookup"><span data-stu-id="19f3a-106">In Visual Basic, pointers are handled for you.</span></span> <span data-ttu-id="19f3a-107">Por exemplo, um parâmetro declarado como um ponteiro para um **int** em C++ é equivalente a um parâmetro declarado em Visual Basic como um  **inteiro** ByRef.</span><span class="sxs-lookup"><span data-stu-id="19f3a-107">For example, a parameter declared as a pointer to an **int** in C++ is equivalent to a parameter declared in Visual Basic as a **ByRef** **Integer**.</span></span>

<span data-ttu-id="19f3a-108">Um parâmetro declarado **como cadeia de caracteres** em Visual Basic é declarado como um ponteiro para um **BSTR** em C++.</span><span class="sxs-lookup"><span data-stu-id="19f3a-108">A parameter that is declared **As String** in Visual Basic is declared as a pointer to a **BSTR** in C++.</span></span> <span data-ttu-id="19f3a-109">Definir um ponteiro de cadeia de caracteres como **nulo** em C++ é equivalente a definir a cadeia de caracteres para a constante **vbNullString** em Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="19f3a-109">Setting a string pointer to **NULL** in C++ is equivalent to setting the string to the **vbNullString** constant in Visual Basic.</span></span> <span data-ttu-id="19f3a-110">A passagem de uma cadeia de caracteres de comprimento zero ("") para uma função criada para receber **NULL** não funciona, pois isso passa um ponteiro para uma cadeia de caracteres de comprimento zero em vez de um ponteiro zero.</span><span class="sxs-lookup"><span data-stu-id="19f3a-110">Passing in a zero-length string ("") to a function designed to receive **NULL** does not work, as this passes a pointer to a zero-length string instead of a zero pointer.</span></span>

<span data-ttu-id="19f3a-111">O C++ dá suporte a contêineres de dados, estruturas e uniões, que não têm equivalente em versões anteriores do Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="19f3a-111">C++ supports data containers, namely structures and unions, that have no equivalent in early versions of Visual Basic.</span></span> <span data-ttu-id="19f3a-112">Por esse motivo, os objetos COM normalmente encapsulam informações que geralmente são armazenadas em estruturas e uniões em classes de objetos.</span><span class="sxs-lookup"><span data-stu-id="19f3a-112">For this reason, COM objects typically wrap information that usually is stored in structures and unions in object classes.</span></span> <span data-ttu-id="19f3a-113">No entanto, alguns objetos COM podem conter estruturas, fazendo com que partes dos métodos ou funcionalidades do objeto fiquem inacessíveis para Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="19f3a-113">Some COM objects, however, may contain structures, causing portions of the object's methods or functionality to be inaccessible to Visual Basic.</span></span>

<span data-ttu-id="19f3a-114">Alguns tipos de dados C++ não têm suporte em Visual Basic, por exemplo, tipos não assinados e tipos de **HWND** .</span><span class="sxs-lookup"><span data-stu-id="19f3a-114">Some C++ data types are not supported in Visual Basic, for example unsigned types and **HWND** types.</span></span> <span data-ttu-id="19f3a-115">Os métodos que aceitam ou retornam esses tipos de dados não estão disponíveis no Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="19f3a-115">Methods that accept or return these data types are not available in Visual Basic.</span></span>

<span data-ttu-id="19f3a-116">Visual Basic usa tipos de dados compatíveis com a automação como seus tipos de dados internos.</span><span class="sxs-lookup"><span data-stu-id="19f3a-116">Visual Basic uses Automation-compatible data types as its internal data types.</span></span> <span data-ttu-id="19f3a-117">Portanto, os tipos de dados do C++ que são compatíveis com a automação também são compatíveis com Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="19f3a-117">Thus, C++ data types that are Automation-compatible are also compatible with Visual Basic.</span></span> <span data-ttu-id="19f3a-118">Os tipos de dados que não são compatíveis com a automação talvez não possam ser convertidos em Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="19f3a-118">Data types that are not Automation-compatible may not be able to be converted to Visual Basic.</span></span>

<span data-ttu-id="19f3a-119">A tabela a seguir lista os tipos de dados com suporte pelo Visual Basic e seus equivalentes **VarType** .</span><span class="sxs-lookup"><span data-stu-id="19f3a-119">The following table lists the data types are supported by Visual Basic and their **VARTYPE** equivalents.</span></span> <span data-ttu-id="19f3a-120">**VarType** é uma enumeração que lista os tipos de variantes de automação.</span><span class="sxs-lookup"><span data-stu-id="19f3a-120">**VARTYPE** is an enumeration that lists the Automation variant types.</span></span>



| <span data-ttu-id="19f3a-121">Tipo de dados do Visual Basic</span><span class="sxs-lookup"><span data-stu-id="19f3a-121">Visual Basic data type</span></span>  | <span data-ttu-id="19f3a-122">Devartyper equivalente</span><span class="sxs-lookup"><span data-stu-id="19f3a-122">VARTYPE equivalent</span></span>                |
|-------------------------|-----------------------------------|
| <span data-ttu-id="19f3a-123">**Inteiro**</span><span class="sxs-lookup"><span data-stu-id="19f3a-123">**Integer**</span></span><br/>  | <span data-ttu-id="19f3a-124">16 bits, assinado, VT \_ i2</span><span class="sxs-lookup"><span data-stu-id="19f3a-124">16 bit, signed, VT\_I2</span></span><br/> |
| <span data-ttu-id="19f3a-125">**Long**</span><span class="sxs-lookup"><span data-stu-id="19f3a-125">**Long**</span></span><br/>     | <span data-ttu-id="19f3a-126">32 bits, assinado, VT \_ i4</span><span class="sxs-lookup"><span data-stu-id="19f3a-126">32 bit, signed, VT\_I4</span></span><br/> |
| <span data-ttu-id="19f3a-127">**Data**</span><span class="sxs-lookup"><span data-stu-id="19f3a-127">**Date**</span></span><br/>     | <span data-ttu-id="19f3a-128">Data de VT \_</span><span class="sxs-lookup"><span data-stu-id="19f3a-128">VT\_DATE</span></span><br/>               |
| <span data-ttu-id="19f3a-129">**Moeda**</span><span class="sxs-lookup"><span data-stu-id="19f3a-129">**Currency**</span></span><br/> | <span data-ttu-id="19f3a-130">VT \_ Cy</span><span class="sxs-lookup"><span data-stu-id="19f3a-130">VT\_CY</span></span><br/>                 |
| <span data-ttu-id="19f3a-131">**Objeto**</span><span class="sxs-lookup"><span data-stu-id="19f3a-131">**Object**</span></span><br/>   | <span data-ttu-id="19f3a-132">\*expedição de VT \_</span><span class="sxs-lookup"><span data-stu-id="19f3a-132">\*VT\_DISPATCH</span></span><br/>         |
| <span data-ttu-id="19f3a-133">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19f3a-133">**String**</span></span><br/>   | <span data-ttu-id="19f3a-134">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="19f3a-134">VT\_BSTR</span></span><br/>               |
| <span data-ttu-id="19f3a-135">**Booliano**</span><span class="sxs-lookup"><span data-stu-id="19f3a-135">**Boolean**</span></span><br/>  | <span data-ttu-id="19f3a-136">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="19f3a-136">VT\_BOOL</span></span><br/>               |
| <span data-ttu-id="19f3a-137">**Moeda**</span><span class="sxs-lookup"><span data-stu-id="19f3a-137">**Currency**</span></span><br/> | <span data-ttu-id="19f3a-138">\_decimal VT</span><span class="sxs-lookup"><span data-stu-id="19f3a-138">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="19f3a-139">**Single**</span><span class="sxs-lookup"><span data-stu-id="19f3a-139">**Single**</span></span><br/>   | <span data-ttu-id="19f3a-140">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="19f3a-140">VT\_R4</span></span><br/>                 |
| <span data-ttu-id="19f3a-141">**Double**</span><span class="sxs-lookup"><span data-stu-id="19f3a-141">**Double**</span></span><br/>   | <span data-ttu-id="19f3a-142">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="19f3a-142">VT\_R8</span></span><br/>                 |
| <span data-ttu-id="19f3a-143">**Decimal**</span><span class="sxs-lookup"><span data-stu-id="19f3a-143">**Decimal**</span></span><br/>  | <span data-ttu-id="19f3a-144">\_decimal VT</span><span class="sxs-lookup"><span data-stu-id="19f3a-144">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="19f3a-145">**Byte**</span><span class="sxs-lookup"><span data-stu-id="19f3a-145">**Byte**</span></span><br/>     | <span data-ttu-id="19f3a-146">\_decimal VT</span><span class="sxs-lookup"><span data-stu-id="19f3a-146">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="19f3a-147">**Variante**</span><span class="sxs-lookup"><span data-stu-id="19f3a-147">**Variant**</span></span><br/>  | <span data-ttu-id="19f3a-148">variante do VT \_</span><span class="sxs-lookup"><span data-stu-id="19f3a-148">VT\_VARIANT</span></span><br/>            |



 

<span data-ttu-id="19f3a-149">Todos os parâmetros em Visual Basic, a menos que rotulado com a palavra-chave **ByVal**, sejam passados por referência (como ponteiros) em vez de por valor.</span><span class="sxs-lookup"><span data-stu-id="19f3a-149">All parameters in Visual Basic, unless labeled with the keyword **ByVal**, are passed by reference (as pointers) instead of by value.</span></span>

<span data-ttu-id="19f3a-150">C++ e Visual Basic diferem ligeiramente na forma como representam propriedades.</span><span class="sxs-lookup"><span data-stu-id="19f3a-150">C++ and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="19f3a-151">No C++, as propriedades são representadas como um conjunto de funções de acessador, uma que define o valor da propriedade e outra que recupera o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="19f3a-151">In C++, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="19f3a-152">Em Visual Basic, as propriedades são representadas como um único item que pode ser usado para recuperar ou definir o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="19f3a-152">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19f3a-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19f3a-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19f3a-154">Convertendo para Visual Basic</span><span class="sxs-lookup"><span data-stu-id="19f3a-154">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 





