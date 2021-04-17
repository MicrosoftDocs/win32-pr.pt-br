---
description: No MOF, os números são dígitos que descrevem valores numéricos. O MOF fornece uma variedade de tipos de dados que são convertidos em automação e também permite que esses números estejam em formatos diferentes. A tabela a seguir lista os valores numéricos que o MOF suporta.
ms.assetid: 7a18ed36-9c12-42be-a4ee-0f6c0097b130
ms.tgt_platform: multiple
title: Números (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad348820e0294e76ba059a06b6daa6f1c916d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762408"
---
# <a name="numbers-wmi"></a><span data-ttu-id="22962-105">Números (WMI)</span><span class="sxs-lookup"><span data-stu-id="22962-105">Numbers (WMI)</span></span>

<span data-ttu-id="22962-106">No MOF, os números são dígitos que descrevem valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="22962-106">In MOF, numbers are digits that describe numerical values.</span></span> <span data-ttu-id="22962-107">O MOF fornece uma variedade de tipos de dados que são convertidos em automação e também permite que esses números estejam em formatos diferentes.</span><span class="sxs-lookup"><span data-stu-id="22962-107">MOF provides a variety of data types that translate into Automation, and also allows those numbers to be in different formats.</span></span> <span data-ttu-id="22962-108">A tabela a seguir lista os valores numéricos que o MOF suporta.</span><span class="sxs-lookup"><span data-stu-id="22962-108">The following table lists the numeric values that MOF supports.</span></span>



| <span data-ttu-id="22962-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="22962-109">Data type</span></span>  | <span data-ttu-id="22962-110">Tipo de automação</span><span class="sxs-lookup"><span data-stu-id="22962-110">Automation type</span></span> | <span data-ttu-id="22962-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="22962-111">Description</span></span>                                                                                                                                                             |
|------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22962-112">**sint8**</span><span class="sxs-lookup"><span data-stu-id="22962-112">**sint8**</span></span>  | <span data-ttu-id="22962-113">**\_I2 VT**</span><span class="sxs-lookup"><span data-stu-id="22962-113">**VT\_I2**</span></span>      | <span data-ttu-id="22962-114">Inteiro de 8 bits assinado.</span><span class="sxs-lookup"><span data-stu-id="22962-114">Signed 8-bit integer.</span></span><br/>                                                                                                                                        |
| <span data-ttu-id="22962-115">**sint16**</span><span class="sxs-lookup"><span data-stu-id="22962-115">**sint16**</span></span> | <span data-ttu-id="22962-116">**\_I2 VT**</span><span class="sxs-lookup"><span data-stu-id="22962-116">**VT\_I2**</span></span>      | <span data-ttu-id="22962-117">Inteiro de 16 bits assinado.</span><span class="sxs-lookup"><span data-stu-id="22962-117">Signed 16-bit integer.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="22962-118">**sint32**</span><span class="sxs-lookup"><span data-stu-id="22962-118">**sint32**</span></span> | <span data-ttu-id="22962-119">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="22962-119">VT\_I4</span></span>          | <span data-ttu-id="22962-120">Inteiro de 32 bits assinado.</span><span class="sxs-lookup"><span data-stu-id="22962-120">Signed 32-bit integer.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="22962-121">**sint64**</span><span class="sxs-lookup"><span data-stu-id="22962-121">**sint64**</span></span> | <span data-ttu-id="22962-122">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="22962-122">**VT\_BSTR**</span></span>    | <span data-ttu-id="22962-123">Número inteiro de 64 bits assinado no formulário de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="22962-123">Signed 64-bit integer in string form.</span></span> <span data-ttu-id="22962-124">Esse tipo segue o formato hexadecimal ou decimal de acordo com as regras C de American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="22962-124">This type follows hexadecimal or decimal format according to the American National Standards Institute (ANSI) C rules.</span></span><br/> |
| <span data-ttu-id="22962-125">**real32**</span><span class="sxs-lookup"><span data-stu-id="22962-125">**real32**</span></span> | <span data-ttu-id="22962-126">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="22962-126">**VT\_R4**</span></span>      | <span data-ttu-id="22962-127">valor de ponto flutuante de 4 bytes que segue o padrão IEEE (Institute of Electrical and Electronics Engineers, Inc.).</span><span class="sxs-lookup"><span data-stu-id="22962-127">4-byte floating-point value that follows the Institute of Electrical and Electronics Engineers, Inc. (IEEE) standard.</span></span><br/>                                        |
| <span data-ttu-id="22962-128">**real64**</span><span class="sxs-lookup"><span data-stu-id="22962-128">**real64**</span></span> | <span data-ttu-id="22962-129">**R8 de VT \_**</span><span class="sxs-lookup"><span data-stu-id="22962-129">**VT\_R8**</span></span>      | <span data-ttu-id="22962-130">valor de ponto flutuante de 8 bytes que segue o padrão IEEE.</span><span class="sxs-lookup"><span data-stu-id="22962-130">8-byte floating-point value that follows the IEEE standard.</span></span><br/>                                                                                                  |
| <span data-ttu-id="22962-131">**uint8**</span><span class="sxs-lookup"><span data-stu-id="22962-131">**uint8**</span></span>  | <span data-ttu-id="22962-132">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="22962-132">**VT\_UI1**</span></span>     | <span data-ttu-id="22962-133">Inteiro de 8 bits não assinado.</span><span class="sxs-lookup"><span data-stu-id="22962-133">Unsigned 8-bit integer.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="22962-134">**UInt16**</span><span class="sxs-lookup"><span data-stu-id="22962-134">**uint16**</span></span> | <span data-ttu-id="22962-135">**\_I4 VT**</span><span class="sxs-lookup"><span data-stu-id="22962-135">**VT\_I4**</span></span>      | <span data-ttu-id="22962-136">Inteiro de 16 bits sem sinal.</span><span class="sxs-lookup"><span data-stu-id="22962-136">Unsigned 16-bit integer.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="22962-137">**uint32**</span><span class="sxs-lookup"><span data-stu-id="22962-137">**uint32**</span></span> | <span data-ttu-id="22962-138">**\_I4 VT**</span><span class="sxs-lookup"><span data-stu-id="22962-138">**VT\_I4**</span></span>      | <span data-ttu-id="22962-139">Inteiro de 32 bits sem sinal.</span><span class="sxs-lookup"><span data-stu-id="22962-139">Unsigned 32-bit integer.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="22962-140">**uint64**</span><span class="sxs-lookup"><span data-stu-id="22962-140">**uint64**</span></span> | <span data-ttu-id="22962-141">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="22962-141">**VT\_BSTR**</span></span>    | <span data-ttu-id="22962-142">Inteiro de 64 bits sem sinal no formulário de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="22962-142">Unsigned 64-bit integer in string form.</span></span> <span data-ttu-id="22962-143">Esse tipo segue o formato hexadecimal ou decimal de acordo com as regras ANSI C.</span><span class="sxs-lookup"><span data-stu-id="22962-143">This type follows hexadecimal or decimal format according to ANSI C rules.</span></span><br/>                                           |



 

<span data-ttu-id="22962-144">Embora seja flexível, o código MOF encontra algumas alterações ao lidar com a automação:</span><span class="sxs-lookup"><span data-stu-id="22962-144">Although flexible, MOF code does encounter some changes when dealing with Automation:</span></span>

-   <span data-ttu-id="22962-145">Você deve codificar inteiros de 64 bits como cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="22962-145">You must encode 64-bit integers as strings.</span></span>

    <span data-ttu-id="22962-146">A automação não dá suporte a um tipo integral de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="22962-146">Automation does not support a 64-bit integral type.</span></span>

-   <span data-ttu-id="22962-147">Os tipos de automação nem sempre correspondem em tamanho de bits a tipos de dados MOF.</span><span class="sxs-lookup"><span data-stu-id="22962-147">Automation types do not always correspond in bit size to MOF data types.</span></span>

    <span data-ttu-id="22962-148">Por exemplo, a automação usa VT \_ i4 para retornar um valor de 16 bits não assinado.</span><span class="sxs-lookup"><span data-stu-id="22962-148">For example, Automation uses VT\_I4 to return an unsigned 16-bit value.</span></span> <span data-ttu-id="22962-149">Essa discrepância existe devido a problemas de extensão de conexão.</span><span class="sxs-lookup"><span data-stu-id="22962-149">This discrepancy exists because of sign-extension problems.</span></span> <span data-ttu-id="22962-150">Se a automação usou VT \_ i2 em vez de VT \_ I4, 65.536 pareceria ser o valor 1, causando problemas de tipo e intervalo.</span><span class="sxs-lookup"><span data-stu-id="22962-150">If Automation used VT\_I2 instead of VT\_I4, 65,536 would appear to be the value  1, causing type and range problems.</span></span> <span data-ttu-id="22962-151">Da mesma forma, a automação representa o tipo **UInt32** como VT \_ i4 porque não existe nenhum tipo inteiro maior para conter **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="22962-151">Similarly, Automation represents the **uint32** type as VT\_I4 because there exists no larger integer type to contain **uint32**.</span></span>

-   <span data-ttu-id="22962-152">Você não precisa alterar nenhuma representação para tipos de numeral de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="22962-152">You do not need to change any representation for 8-bit numeral types.</span></span>

    <span data-ttu-id="22962-153">A automação dá suporte \_ a VT UI1, um tipo de 8 bits não assinado.</span><span class="sxs-lookup"><span data-stu-id="22962-153">Automation supports VT\_UI1, an unsigned 8-bit type.</span></span>

<span data-ttu-id="22962-154">O MOF dá suporte a constantes longas.</span><span class="sxs-lookup"><span data-stu-id="22962-154">MOF supports long constants.</span></span> <span data-ttu-id="22962-155">Você declara uma constante longa usando uma série simples de dígitos com um sinal negativo opcional.</span><span class="sxs-lookup"><span data-stu-id="22962-155">You declare a long constant using a simple series of digits with an optional negative sign.</span></span> <span data-ttu-id="22962-156">Uma constante longa não pode exceder o tamanho da variável que está declarada para contê-la.</span><span class="sxs-lookup"><span data-stu-id="22962-156">A long constant cannot exceed the size of the variable that is declared to hold it.</span></span> <span data-ttu-id="22962-157">Alguns exemplos de constantes longas são 1000 e 12310.</span><span class="sxs-lookup"><span data-stu-id="22962-157">Some examples of long constants are 1000 and  12310.</span></span>

<span data-ttu-id="22962-158">O MOF também dá suporte a formatos numéricos alternativos.</span><span class="sxs-lookup"><span data-stu-id="22962-158">MOF also supports alternate numerical formats.</span></span> <span data-ttu-id="22962-159">A tabela a seguir lista os caracteres especiais que você deve usar para descrever as constantes hexadecimal, binária e octal.</span><span class="sxs-lookup"><span data-stu-id="22962-159">The following table lists the special characters you must use to describe hexadecimal, binary, and octal constants.</span></span>



| <span data-ttu-id="22962-160">Constante</span><span class="sxs-lookup"><span data-stu-id="22962-160">Constant</span></span>               | <span data-ttu-id="22962-161">Caractere especial</span><span class="sxs-lookup"><span data-stu-id="22962-161">Special character</span></span>     | <span data-ttu-id="22962-162">Exemplo</span><span class="sxs-lookup"><span data-stu-id="22962-162">Example</span></span>                   |
|------------------------|-----------------------|---------------------------|
| <span data-ttu-id="22962-163">Decimal</span><span class="sxs-lookup"><span data-stu-id="22962-163">Decimal</span></span><br/>     | <span data-ttu-id="22962-164">Nenhum</span><span class="sxs-lookup"><span data-stu-id="22962-164">None</span></span><br/>       | <span data-ttu-id="22962-165">Val = 65</span><span class="sxs-lookup"><span data-stu-id="22962-165">val = 65</span></span><br/>       |
| <span data-ttu-id="22962-166">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="22962-166">Hexadecimal</span></span><br/> | <span data-ttu-id="22962-167">prefixo 0x</span><span class="sxs-lookup"><span data-stu-id="22962-167">0x prefix</span></span><br/>  | <span data-ttu-id="22962-168">Val = 0x41</span><span class="sxs-lookup"><span data-stu-id="22962-168">val = 0x41</span></span><br/>     |
| <span data-ttu-id="22962-169">Octais</span><span class="sxs-lookup"><span data-stu-id="22962-169">Octal</span></span><br/>       | <span data-ttu-id="22962-170">0 à esquerda</span><span class="sxs-lookup"><span data-stu-id="22962-170">Leading 0</span></span><br/>  | <span data-ttu-id="22962-171">Val = 0101</span><span class="sxs-lookup"><span data-stu-id="22962-171">val = 0101</span></span><br/>     |
| <span data-ttu-id="22962-172">Binário</span><span class="sxs-lookup"><span data-stu-id="22962-172">Binary</span></span><br/>      | <span data-ttu-id="22962-173">B à direita</span><span class="sxs-lookup"><span data-stu-id="22962-173">Trailing B</span></span><br/> | <span data-ttu-id="22962-174">Val = 1000001B</span><span class="sxs-lookup"><span data-stu-id="22962-174">val = 1000001B</span></span><br/> |



 

<span data-ttu-id="22962-175">Você pode usar uma constante de ponto flutuante para representar notação científica, bem como frações, conforme mostrado a seguir:</span><span class="sxs-lookup"><span data-stu-id="22962-175">You can use a floating-point constant to represent scientific notation as well as fractions, as shown next:</span></span>

``` syntax
3.14
-3.14
-1.2778E+02
```

<span data-ttu-id="22962-176">O WMI considera constantes de ponto flutuante como tipos de **\_ R8 de VT** para automação.</span><span class="sxs-lookup"><span data-stu-id="22962-176">WMI considers floating-point constants as **VT\_R8** types for Automation.</span></span>

<span data-ttu-id="22962-177">O exemplo a seguir descreve as declarações de classe e de instância que ilustram como usar cada um dos tipos de dados numéricos para definir propriedades:</span><span class="sxs-lookup"><span data-stu-id="22962-177">The following example describes class and instance declarations that illustrate how to use each of the numeric data types to set properties:</span></span>

``` syntax
Class NumericDataClass
 {
   [key] uint8 Duint8;
   SInt8       Dchar;
   UInt16      Dtword;
   Sint16      Dinst16;
   UInt32      Ddword;
   Sint32      Dinst1;
   Sint32      Dinst2;
   Sint32      Dinst3;
   Sint32      Dinst4;
   Sint32      Dinst5;
   Real32      Dfloat;
   Real64      Ddouble1;
   Real64      Ddouble2;
 };

instance of NumericDataClass
 {
   Duint8   =  122;
   Dchar    = -128;
   Dtword   =  30;
   Dinst16  = -1445;
   Ddword   =  6987777;
   Dinst1   = -455589;
   Dinst2   =  23;
   Dinst3   =  03;         // Base 8
   Dinst4   =  0xFe;       // Base 16
   Dinst5   =  11b;        // Base 2
   Dfloat   =  3.1478;
   Ddouble1 =  99987.3654;
   Ddouble2 =  2.3e-2;
 };
```

 

 




