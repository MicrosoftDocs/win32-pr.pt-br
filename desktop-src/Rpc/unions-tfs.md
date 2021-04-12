---
title: Uniões de RPC
description: Uniões encapsuladas e não encapsuladas e seu formato com RPC (chamada de procedimento remoto).
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f35f0ff23132705330bf1f8566443ac8aa81d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454076"
---
# <a name="rpc-unions"></a><span data-ttu-id="9e3ab-103">Uniões de RPC</span><span class="sxs-lookup"><span data-stu-id="9e3ab-103">RPC unions</span></span>

<span data-ttu-id="9e3ab-104">As uniões encapsuladas e não encapsuladas compartilham um<> formato de braço de União comum \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="9e3ab-104">Both encapsulated and nonencapsulated unions share a common union\_arm\_selector<> format:</span></span>

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

<span data-ttu-id="9e3ab-105">O campo de braços de União \_<2> consiste em duas partes.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-105">The union\_arms<2> field consists of two parts.</span></span> <span data-ttu-id="9e3ab-106">Se a União for uma União de estilo MIDL 1,0, os quatro bits superiores conterão o alinhamento do braço Union (alinhamento do maior braço alinhado).</span><span class="sxs-lookup"><span data-stu-id="9e3ab-106">If the union is a MIDL 1.0 style union, the upper 4 bits contain the alignment of the union arm (alignment of greatest aligned arm).</span></span> <span data-ttu-id="9e3ab-107">Caso contrário, os 4 bits superiores são zero.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-107">Otherwise the upper 4 bits are zero.</span></span> <span data-ttu-id="9e3ab-108">Os 12 bits inferiores contêm o número de braços na União.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-108">The lower 12 bits contain the number of arms in the union.</span></span> <span data-ttu-id="9e3ab-109">Em outras palavras:</span><span class="sxs-lookup"><span data-stu-id="9e3ab-109">In other words:</span></span>

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

<span data-ttu-id="9e3ab-110">A descrição do deslocamento \_ para \_ \_ o arm<2> campos contêm um deslocamento relativo assinado para a descrição do tipo do ARM.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-110">The offset\_to\_arm\_description<2> fields contain a relative signed offset to the arm's type description.</span></span> <span data-ttu-id="9e3ab-111">No entanto, o campo está sobrecarregado com otimização para tipos simples.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-111">However, the field is overloaded with optimization for simple types.</span></span> <span data-ttu-id="9e3ab-112">Para isso, o byte superior desse campo de deslocamento é \_ \_ o byte da União mágica FC \_ (0x80) e o byte inferior do curto é o tipo de caractere de formato real do ARM.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-112">For these, the upper byte of this offset field is FC\_MAGIC\_UNION\_BYTE (0x80) and the lower byte of the short is the actual format character type of the arm.</span></span> <span data-ttu-id="9e3ab-113">Assim, há dois intervalos para os valores de deslocamento: "80 *XX*" significa que *XX* é uma cadeia de caracteres de formato de tipo; e todo o restante dentro do intervalo (80 FF..</span><span class="sxs-lookup"><span data-stu-id="9e3ab-113">As such, there are two ranges for the offset values: "80 *xx*" means that *xx* is a type format string; and everything else within range (80 FF ..</span></span> <span data-ttu-id="9e3ab-114">7F FF) significa um deslocamento real.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-114">7f FF) means an actual offset.</span></span> <span data-ttu-id="9e3ab-115">Isso faz com que os deslocamentos do intervalo <80 00..</span><span class="sxs-lookup"><span data-stu-id="9e3ab-115">This makes offsets from range <80 00 ..</span></span> <span data-ttu-id="9e3ab-116">80 FF > não disponíveis como deslocamentos.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-116">80 FF > unavailable as offsets.</span></span> <span data-ttu-id="9e3ab-117">O compilador verifica a partir da versão de MIDL 5.1.164.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-117">The compiler checks that as of MIDL version 5.1.164.</span></span>

<span data-ttu-id="9e3ab-118">A descrição padrão do \_ arm \_<2> o campo indica o tipo de braço de União para o ARM padrão, se houver.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-118">The default\_arm\_description<2> field indicates the type of union arm for the default arm, if any.</span></span> <span data-ttu-id="9e3ab-119">Se não houver um ARM padrão especificado para a União, a descrição padrão do \_ arm \_<2> campo será 0xFFFF e uma exceção será gerada se o \_ valor switch for não corresponder a nenhum dos valores de case do ARM.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-119">If there is no default arm specified for the union then the default\_arm\_description<2> field is 0xFFFF and an exception is raised if the switch\_is value does not match any of the arm case values.</span></span> <span data-ttu-id="9e3ab-120">Se o ARM padrão for especificado, mas vazio, a descrição padrão do \_ arm \_<2> campo será zero.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-120">If the default arm is specified but empty, then the default\_arm\_description<2> field is zero.</span></span> <span data-ttu-id="9e3ab-121">Caso contrário, a descrição padrão do \_ arm \_<2> campo tem a mesma semântica que o deslocamento \_ para a descrição do \_ ARM \_<2> campos.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-121">Otherwise the default\_arm\_description<2> field has the same semantics as the offset\_to\_arm\_description<2> fields.</span></span>

<span data-ttu-id="9e3ab-122">Veja a seguir um resumo:</span><span class="sxs-lookup"><span data-stu-id="9e3ab-122">The following is a summary:</span></span>

-   <span data-ttu-id="9e3ab-123">0-padrão vazio</span><span class="sxs-lookup"><span data-stu-id="9e3ab-123">0 - empty default</span></span>
-   <span data-ttu-id="9e3ab-124">FFFF-nenhum padrão</span><span class="sxs-lookup"><span data-stu-id="9e3ab-124">FFFF - no default</span></span>
-   <span data-ttu-id="9e3ab-125">80xx – tipo simples</span><span class="sxs-lookup"><span data-stu-id="9e3ab-125">80xx - simple type</span></span>
-   <span data-ttu-id="9e3ab-126">outro deslocamento relativo</span><span class="sxs-lookup"><span data-stu-id="9e3ab-126">other - relative offset</span></span>

## <a name="encapsulated-unions"></a><span data-ttu-id="9e3ab-127">Uniões encapsuladas</span><span class="sxs-lookup"><span data-stu-id="9e3ab-127">Encapsulated Unions</span></span>

<span data-ttu-id="9e3ab-128">Uma União encapsulada vem de uma sintaxe de União especial em IDL.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-128">An encapsulated union comes from a special union syntax in IDL.</span></span> <span data-ttu-id="9e3ab-129">Efetivamente, uma União encapsulada é uma estrutura de pacote com um campo discriminante no início da estrutura e a União como o único outro membro.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-129">Effectively, an encapsulated union is a bundle structure with a discriminant field at the beginning of the structure and the union as the only other member.</span></span>

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

<span data-ttu-id="9e3ab-130">Um tipo de opção de União encapsulada \_<1> campo tem duas partes.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-130">An encapsulated union's switch\_type<1> field has two parts.</span></span> <span data-ttu-id="9e3ab-131">O Nibble inferior fornece o tipo de comutador real e o Nibble superior fornece o incremento de memória para ultrapassar que é um valor que o ponteiro de memória deve ser incrementado para ignorar o \_ campo switch é, que inclui qualquer preenchimento entre o \_ campo switch is () da estrutura construída pelo stub e o campo Union real.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-131">The lower nibble provides the actual switch type, and the upper nibble provides the memory increment to step over that is an amount that the memory pointer must be incremented to skip past the switch\_is field, which includes any padding between the switch\_is() field of the stub-constructed structure and the actual union field.</span></span>

<span data-ttu-id="9e3ab-132">O tamanho da memória \_<2> campo é o tamanho somente da União e é idêntico a uniões não encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-132">The memory\_size<2> field is the size of the union only, and is identical to nonencapsulated unions.</span></span> <span data-ttu-id="9e3ab-133">Para obter o tamanho total da estrutura que contém a União, adicione o tamanho da memória \_<2> ao incremento de memória para intervir, ou seja, o Nibble superior do tipo de comutador \_<1> campo e, em seguida, alinhe pelo alinhamento correspondente ao incremento.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-133">To obtain the total size of the structure that contains the union, add memory\_size<2> to memory increment to step over, that is to the upper nibble of the switch\_type<1> field, then align by the alignment corresponding to the increment.</span></span>

## <a name="nonencapsulated-unions"></a><span data-ttu-id="9e3ab-134">Uniões não encapsuladas</span><span class="sxs-lookup"><span data-stu-id="9e3ab-134">Nonencapsulated Unions</span></span>

<span data-ttu-id="9e3ab-135">Uma União não encapsulada é uma situação típica em que uma União é um argumento ou campo e a opção é outro argumento ou campo, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-135">A nonencapsulated union is a typical situation where a union is one argument or field and the switch is another argument or field, respectively.</span></span>

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

<span data-ttu-id="9e3ab-136">Em que:</span><span class="sxs-lookup"><span data-stu-id="9e3ab-136">Where:</span></span>

<span data-ttu-id="9e3ab-137">O tipo de opção \_<campo 1> é um caractere de formato para o discriminante.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-137">The switch\_type<1> field is a format character for the discriminant.</span></span>

<span data-ttu-id="9e3ab-138">A opção \_ é o \_ descritor<> o campo é um descritor de correlação e tem 4 ou 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado.</span><span class="sxs-lookup"><span data-stu-id="9e3ab-138">The switch\_is\_descriptor<> field is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="9e3ab-139">No entanto, para a opção \_ é a \_ Descrição<>, se a União for inserida em uma estrutura, o campo de deslocamento da opção \_ é \_ Descrição<> é o deslocamento para o \_ campo switch é a partir da posição da União na estrutura (não do início da estrutura).</span><span class="sxs-lookup"><span data-stu-id="9e3ab-139">However, for the switch\_is\_description<>, if the union is embedded in a structure, the offset field of the switch\_is\_description<> is the offset to the switch\_is field from the union's position in the structure (not from the beginning of the structure).</span></span>

<span data-ttu-id="9e3ab-140">A descrição do deslocamento \_ para \_ \_ o tamanho e do \_ ARM<o \_ campo 2> fornece o deslocamento para a descrição do tamanho e do ARM da União, que é idêntica à das uniões encapsuladas e é compartilhada por todas as uniões não encapsuladas do mesmo tipo:</span><span class="sxs-lookup"><span data-stu-id="9e3ab-140">The offset\_to\_size\_and\_arm\_description<2> field gives the offset to the union's size and arm description, which is identical to that for encapsulated unions and is shared by all nonencapsulated unions of the same type :</span></span>

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 