---
title: Erros comuns do compilador
description: Esta seção ilustra os erros de compilador típicos que ocorrem durante a migração de uma base de código existente. Esses exemplos são de código HAL de nível de sistema, embora os conceitos sejam diretamente aplicáveis ao código de nível de usuário.
ms.assetid: bbb6a57f-281a-4a6e-a4b6-15846d0cf21f
keywords:
- erros do compilador programação do Windows de 64 bits
- Programação de migração de 64 bits do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a84a5f5f58f2cab7555ce3401ed6fae0af240f4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104294616"
---
# <a name="common-compiler-errors"></a><span data-ttu-id="abe92-106">Erros comuns do compilador</span><span class="sxs-lookup"><span data-stu-id="abe92-106">Common Compiler Errors</span></span>

<span data-ttu-id="abe92-107">Esta seção ilustra os erros de compilador típicos que ocorrem durante a migração de uma base de código existente.</span><span class="sxs-lookup"><span data-stu-id="abe92-107">This section illustrates the typical compiler errors that occur when migrating an existing code base.</span></span> <span data-ttu-id="abe92-108">Esses exemplos são de código HAL de nível de sistema, embora os conceitos sejam diretamente aplicáveis ao código de nível de usuário.</span><span class="sxs-lookup"><span data-stu-id="abe92-108">These examples happen to be from system-level HAL code, although the concepts are directly applicable to user-level code.</span></span>

## <a name="warning-c4311-example-1"></a><span data-ttu-id="abe92-109">Exemplo de C4311 de aviso 1</span><span class="sxs-lookup"><span data-stu-id="abe92-109">Warning C4311 Example 1</span></span>

<span data-ttu-id="abe92-110">' Type cast ': truncamento de ponteiro de ' void \* \_ \_ ptr64 ' para ' sem sinal longo</span><span class="sxs-lookup"><span data-stu-id="abe92-110">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long</span></span>

<dl> <dt>

<span data-ttu-id="abe92-111"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar</span><span class="sxs-lookup"><span data-stu-id="abe92-111"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span data-ttu-id="abe92-112"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="abe92-112"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="abe92-113">**PtrToUlong** é uma função ou macro embutida, dependendo do seu uso.</span><span class="sxs-lookup"><span data-stu-id="abe92-113">**PtrToUlong** is an inline function or macro, depending on your usage.</span></span> <span data-ttu-id="abe92-114">Ele Trunca um ponteiro para um **ULONG**.</span><span class="sxs-lookup"><span data-stu-id="abe92-114">It truncates a pointer to a **ULONG**.</span></span> <span data-ttu-id="abe92-115">Embora os ponteiros de 32 bits não sejam afetados, a metade superior de um ponteiro de 64 bits é truncada.</span><span class="sxs-lookup"><span data-stu-id="abe92-115">Although 32-bit pointers are not affected, the upper half of a 64-bit pointer is truncated.</span></span>

<span data-ttu-id="abe92-116">\_ \_ \_ A base de configuração \_ de PCI CIA QVA é declarada como um **pVoid**.</span><span class="sxs-lookup"><span data-stu-id="abe92-116">CIA\_PCI\_CONFIG\_BASE\_QVA is declared as a **PVOID**.</span></span> <span data-ttu-id="abe92-117">A conversão **ULONG** funciona no mundo de 32 bits, mas resulta em um erro no mundo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="abe92-117">The **ULONG** cast works in the 32-bit world, but results in an error in the 64-bit world.</span></span> <span data-ttu-id="abe92-118">A solução é obter um ponteiro de 64 bits para um **ULONG**, pois alterar a definição da União que pPciAddr->u. asulong é definido em alterações de código demais.</span><span class="sxs-lookup"><span data-stu-id="abe92-118">The solution is to get a 64-bit pointer to a **ULONG**, because changing the definition of the union that pPciAddr->u.AsULONG is defined in changes too much code.</span></span>

<span data-ttu-id="abe92-119">O uso da macro **PtrToUlong** para converter o **pVoid** de 64 bits para o **ULONG** necessário é permitido porque temos conhecimento sobre o valor específico da QVA de configuração de CIA \_ PCI \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="abe92-119">Using the macro **PtrToUlong** to convert the 64-bit **PVOID** to the needed **ULONG** is allowed because we have knowledge about the specific value of CIA\_PCI\_CONFIG\_BASE\_QVA.</span></span> <span data-ttu-id="abe92-120">Nesse caso, esse ponteiro nunca terá dados nos 32 bits superiores.</span><span class="sxs-lookup"><span data-stu-id="abe92-120">In this case, this pointer will never have data in the upper 32 bits.</span></span>

</dd> <dt>

<span data-ttu-id="abe92-121"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções</span><span class="sxs-lookup"><span data-stu-id="abe92-121"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a><span data-ttu-id="abe92-122">Exemplo de C4311 de aviso 2</span><span class="sxs-lookup"><span data-stu-id="abe92-122">Warning C4311 Example 2</span></span>

<span data-ttu-id="abe92-123">' Type cast ': truncamento de ponteiro de ' struct \_ Error \_ frame \* \_ \_ ptr64 ' para ' sem sinal longo</span><span class="sxs-lookup"><span data-stu-id="abe92-123">'type cast' : pointer truncation from 'struct \_ERROR\_FRAME \*\_\_ptr64 ' to 'unsigned long</span></span>

<dl> <dt>

<span data-ttu-id="abe92-124"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar</span><span class="sxs-lookup"><span data-stu-id="abe92-124"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span data-ttu-id="abe92-125"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="abe92-125"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="abe92-126">O problema é que o último parâmetro para essa função é um ponteiro para uma estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="abe92-126">The problem is that the last parameter to this function is a pointer to a data structure.</span></span> <span data-ttu-id="abe92-127">Como PUncorrectableError é um ponteiro, ele muda de tamanho com o modelo de programação.</span><span class="sxs-lookup"><span data-stu-id="abe92-127">Because PUncorrectableError is a pointer, it changes size with the programming model.</span></span> <span data-ttu-id="abe92-128">O protótipo para **KeBugCheckEx** foi alterado para que o último parâmetro seja um **ULONG \_ PTR**.</span><span class="sxs-lookup"><span data-stu-id="abe92-128">The prototype for **KeBugCheckEx** was changed so that the last parameter is a **ULONG\_PTR**.</span></span> <span data-ttu-id="abe92-129">Como resultado, é necessário converter o ponteiro de função em um **\_ PTR**.</span><span class="sxs-lookup"><span data-stu-id="abe92-129">As a result, it's necessary to cast the function pointer to a **ULONG\_PTR**.</span></span>

<span data-ttu-id="abe92-130">Você pode perguntar por que **pVoid** não foi usado como o último parâmetro.</span><span class="sxs-lookup"><span data-stu-id="abe92-130">You might ask why **PVOID** was not used as the last parameter.</span></span> <span data-ttu-id="abe92-131">Dependendo do contexto da chamada, o último parâmetro pode ser algo diferente de um ponteiro ou talvez um código de erro.</span><span class="sxs-lookup"><span data-stu-id="abe92-131">Depending on the context of the call, the last parameter may be something other than a pointer or perhaps an error code.</span></span>

</dd> <dt>

<span data-ttu-id="abe92-132"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções</span><span class="sxs-lookup"><span data-stu-id="abe92-132"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a><span data-ttu-id="abe92-133">Exemplo de C4244 de aviso 1</span><span class="sxs-lookup"><span data-stu-id="abe92-133">Warning C4244 Example 1</span></span>

<span data-ttu-id="abe92-134">' = ': conversão de ' struct \_ Configuration \_ Component \* \_ \_ ptr64 ' para ' struct \_ Configuration \_ Component \* ', possível perda de dados</span><span class="sxs-lookup"><span data-stu-id="abe92-134">'=' : conversion from 'struct \_CONFIGURATION\_COMPONENT \*\_\_ptr64 ' to 'struct \_CONFIGURATION\_COMPONENT \*', possible loss of data</span></span>

<dl> <dt>

<span data-ttu-id="abe92-135"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar</span><span class="sxs-lookup"><span data-stu-id="abe92-135"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span data-ttu-id="abe92-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="abe92-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="abe92-137">A função declara o componente variável como um componente PCONFIGURATION \_ .</span><span class="sxs-lookup"><span data-stu-id="abe92-137">The function declares the variable Component as a PCONFIGURATION\_COMPONENT.</span></span> <span data-ttu-id="abe92-138">Posteriormente, a variável será usada na seguinte atribuição que aparece correta:</span><span class="sxs-lookup"><span data-stu-id="abe92-138">Later, the variable is used in the following assignment that appears correct:</span></span>

`Component = &CurrentEntry->ComponentEntry;`

<span data-ttu-id="abe92-139">No entanto, o componente de tipo PCONFIGURATION \_ é definido como:</span><span class="sxs-lookup"><span data-stu-id="abe92-139">However, the type PCONFIGURATION\_COMPONENT is defined as:</span></span>

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

<span data-ttu-id="abe92-140">A definição de tipo para o \_ componente PCONFIGURATION fornece um ponteiro de 32 bits nos modelos de 32 bits e 64 bits porque ele é declarado como **ponteiro \_ 32**.</span><span class="sxs-lookup"><span data-stu-id="abe92-140">The type definition for PCONFIGURATION\_COMPONENT provides a 32-bit pointer in both 32-bit and 64-bit models because it is declared **POINTER\_32**.</span></span> <span data-ttu-id="abe92-141">O designer original dessa estrutura sabia que ela será usada em um contexto de 32 bits no BIOS e definiu-a expressamente para esse uso.</span><span class="sxs-lookup"><span data-stu-id="abe92-141">The original designer of this structure knew it was going to be used in a 32-bit context in the BIOS and expressly defined it for that use.</span></span> <span data-ttu-id="abe92-142">Esse código funciona bem em janelas de 32 bits porque os ponteiros são de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="abe92-142">This code works fine in 32-bit Windows because the pointers happen to be 32-bit.</span></span> <span data-ttu-id="abe92-143">No Windows de 64 bits, ele não funciona porque o código está no contexto de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="abe92-143">In 64-bit Windows, it does not work because the code is in 64-bit context.</span></span>

</dd> <dt>

<span data-ttu-id="abe92-144"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções</span><span class="sxs-lookup"><span data-stu-id="abe92-144"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="abe92-145">Para contornar esse problema, use \_ o componente \* de configuração em vez do componente PCONFIGURATION-bit de 32 bits \_ .</span><span class="sxs-lookup"><span data-stu-id="abe92-145">To work around this problem, use CONFIGURATION\_COMPONENT \* rather than the 32-bit PCONFIGURATION\_COMPONENT .</span></span> <span data-ttu-id="abe92-146">É importante entender claramente a finalidade do código.</span><span class="sxs-lookup"><span data-stu-id="abe92-146">It is important to clearly understand the purpose of the code.</span></span> <span data-ttu-id="abe92-147">Se esse código for destinado a tocar o BIOS de 32 bits ou o espaço do sistema, essa correção não funcionará.</span><span class="sxs-lookup"><span data-stu-id="abe92-147">If this code is intended to touch 32-bit BIOS or System space, this fix will not work.</span></span>

<span data-ttu-id="abe92-148">O **ponteiro \_ 32** é definido em Ntdef. h e Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="abe92-148">**POINTER\_32** is defined in Ntdef.h and Winnt.h.</span></span>

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a><span data-ttu-id="abe92-149">Exemplo de C4242 de aviso 2</span><span class="sxs-lookup"><span data-stu-id="abe92-149">Warning C4242 Example 2</span></span>

<span data-ttu-id="abe92-150">' = ': conversão de ' \_ \_ Int64 ' para ' não assinado longo ', possível perda de dados</span><span class="sxs-lookup"><span data-stu-id="abe92-150">'=' : conversion from '\_\_int64 ' to 'unsigned long ', possible loss of data</span></span>

<dl> <dt>

<span data-ttu-id="abe92-151"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar</span><span class="sxs-lookup"><span data-stu-id="abe92-151"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
ARC_STATUS HalpCopyNVRamBuffer (
IN PCHAR NvDestPtr,
IN PCHAR NvSrcPtr,
IN ULONG Length )
{

ULONG PageSelect1, ByteSelect1;

ByteSelect1 = (NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;

ByteSelect1 = (NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;
```

</dd> <dt>

<span data-ttu-id="abe92-152"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="abe92-152"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="abe92-153">Esse aviso é gerado porque o cálculo está usando valores de 64 bits, nesse caso, aponta e coloca o resultado em um **ULONG** de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="abe92-153">This warning is generated because the calculation is using 64-bit values, in this case pointers, and placing the result in a 32-bit **ULONG**.</span></span>

</dd> <dt>

<span data-ttu-id="abe92-154"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções</span><span class="sxs-lookup"><span data-stu-id="abe92-154"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="abe92-155">Tipo converta o resultado do cálculo para um **ULONG** , conforme mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="abe92-155">Type cast the result of the calculation to a **ULONG** as shown here:</span></span>

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

<span data-ttu-id="abe92-156">Typecasting o resultado permite que o compilador saiba que você tem certeza sobre o resultado.</span><span class="sxs-lookup"><span data-stu-id="abe92-156">Typecasting the result lets the compiler know you are sure about the result.</span></span> <span data-ttu-id="abe92-157">Dito isso, certifique-se de que você entende o cálculo e realmente tem certeza de que ele caberá em um **ULONG** de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="abe92-157">That being said, make certain you understand the calculation and really are sure it will fit in a 32-bit **ULONG**.</span></span>

<span data-ttu-id="abe92-158">Se o resultado não couber em um **ULONG** de 32 bits, altere o tipo base da variável que irá conter o resultado.</span><span class="sxs-lookup"><span data-stu-id="abe92-158">If the result may not fit in a 32-bit **ULONG**, change the base type of the variable that will hold the result.</span></span>

</dd> </dl>

## <a name="warning-c4311---example-1"></a><span data-ttu-id="abe92-159">Aviso C4311-exemplo 1</span><span class="sxs-lookup"><span data-stu-id="abe92-159">Warning C4311 - Example 1</span></span>

<span data-ttu-id="abe92-160">' Type cast ': truncamento de ponteiro de ' void \* \_ \_ ptr64 ' para ' unsinaled Long '</span><span class="sxs-lookup"><span data-stu-id="abe92-160">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="abe92-161"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar</span><span class="sxs-lookup"><span data-stu-id="abe92-161"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
ULONG HalpMapDebugPort(
IN ULONG ComPort,
OUT PULONG ReadQva,
OUT PULONG WriteQva)
{
ULONG ComPortAddress;

ULONG PortQva;

// Compute the port address, based on the desired com port.

switch( ComPort ){
case 1:
   ComPortAddress = COM1_ISA_PORT_ADDRESS;
   break;

case 2:
default:
   ComPortAddress = COM2_ISA_PORT_ADDRESS;
}
PortQva = (ULONG)HAL_MAKE_QVA(CIA_PCI_SPARSE_IO_PHYSICAL) + ComPortAddress;

// Return the QVAs for read and write access.

*ReadQva = PortQva;
*WriteQva = PortQva;

return ComPortAddress;
}
```

</dd> <dt>

<span data-ttu-id="abe92-162"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="abe92-162"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="abe92-163">Essa função inteira lida com endereços como inteiros, exigindo a necessidade de digitar esses inteiros de forma portátil.</span><span class="sxs-lookup"><span data-stu-id="abe92-163">This entire function deals with addresses as integers, necessitating the need to type those integers in a portable way.</span></span> <span data-ttu-id="abe92-164">Todas as variáveis locais, valores intermediários em cálculos e valores de retorno devem ser tipos portáteis.</span><span class="sxs-lookup"><span data-stu-id="abe92-164">All the local variables, intermediate values in calculations, and return values should be portable types.</span></span>

</dd> <dt>

<span data-ttu-id="abe92-165"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções</span><span class="sxs-lookup"><span data-stu-id="abe92-165"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

``` syntax
ULONG_PTR HalpMapDebugPort(
IN ULONG ComPort,
OUT PULONG_PTR ReadQva,
OUT PULONG_PTR WriteQva)
{
ULONG_PTR ComPortAddress;

ULONG_PTR PortQva;

// Compute the port address, based on the desired com port.

switch( ComPort ){
case 1:
   ComPortAddress = COM1_ISA_PORT_ADDRESS;
   break;

case 2:
default:
   ComPortAddress = COM2_ISA_PORT_ADDRESS;
}

PortQva = (ULONG_PTR)HAL_MAKE_QVA(CIA_PCI_SPARSE_IO_PHYSICAL) + ComPortAddress;

// Return the QVAs for read and write access.

*ReadQva = PortQva;
*WriteQva = PortQva;

return ComPortAddress;
}
```

<span data-ttu-id="abe92-166">**Pulong \_ PTR** é um ponteiro que é, em si, 32 bits para janelas de 32 bits e 64 bits para o Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="abe92-166">**PULONG\_PTR** is a pointer that is itself 32 bits for 32-bit Windows and 64 bits for 64-bit Windows.</span></span> <span data-ttu-id="abe92-167">Ele aponta para um inteiro não assinado, **ULONG \_ PTR**, que é de 32 bits para Windows de 32 bits e 64 bits para o Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="abe92-167">It points to an unsigned integer, **ULONG\_PTR**, that is 32 bits for 32-bit Windows and 64 bits for 64-bit Windows.</span></span>

</dd> </dl>

## <a name="warning-c4311---example-2"></a><span data-ttu-id="abe92-168">Aviso C4311-exemplo 2</span><span class="sxs-lookup"><span data-stu-id="abe92-168">Warning C4311 - Example 2</span></span>

<span data-ttu-id="abe92-169">' Type cast ': truncamento de ponteiro de ' void \* \_ \_ ptr64 ' para ' unsinaled Long '</span><span class="sxs-lookup"><span data-stu-id="abe92-169">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="abe92-170"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar</span><span class="sxs-lookup"><span data-stu-id="abe92-170"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
BOOLEAN
HalpMapIoSpace (
VOID
)
{
PVOID PciIoSpaceBase;
PciIoSpaceBase = HAL_MAKE_QVA( CIA_PCI_SPARSE_IO_PHYSICAL );

//Map base addresses in QVA space.

HalpCMOSRamBase = (PVOID)((ULONG)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);
```

</dd> <dt>

<span data-ttu-id="abe92-171"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="abe92-171"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="abe92-172">Embora todos os valores de QVA (quase virtual address) sejam realmente valores de 32 bits nesse estágio e caibam em **ULONG**, ele é mais consistente para tratar todos os endereços como valores do **ULONG \_ PTR** quando possível.</span><span class="sxs-lookup"><span data-stu-id="abe92-172">Even though all QVA (Quasi Virtual Address) values are really 32-bit values at this stage and will fit in a **ULONG**, it is more consistent to treat all addresses as **ULONG\_PTR** values when possible.</span></span>

<span data-ttu-id="abe92-173">O ponteiro PciIoSpaceBase contém o QVA que é criado na macro HAL \_ Make \_ QVA.</span><span class="sxs-lookup"><span data-stu-id="abe92-173">The pointer PciIoSpaceBase holds the QVA that is created in the macro HAL\_MAKE\_QVA.</span></span> <span data-ttu-id="abe92-174">Essa macro retorna um valor de 64 bits com os primeiros 32 bits definidos como zero para que o cálculo funcione.</span><span class="sxs-lookup"><span data-stu-id="abe92-174">This macro returns a 64-bit value with the top 32 bits set to zero so the math will work.</span></span> <span data-ttu-id="abe92-175">Poderíamos simplesmente deixar o código para truncar o ponteiro em um **ULONG**, mas essa prática não é recomendada para aprimorar a manutenção e a portabilidade do código.</span><span class="sxs-lookup"><span data-stu-id="abe92-175">We could simply leave the code to truncate the pointer into a **ULONG**, but this practice is discouraged to enhance code maintainability and portability.</span></span> <span data-ttu-id="abe92-176">Por exemplo, o conteúdo de um QVA pode ser alterado no futuro para usar alguns dos bits superiores nesse nível, dividindo o código.</span><span class="sxs-lookup"><span data-stu-id="abe92-176">For example, the contents of a QVA might change in the future to use some of the upper bits at this level, breaking the code.</span></span>

</dd> <dt>

<span data-ttu-id="abe92-177"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções</span><span class="sxs-lookup"><span data-stu-id="abe92-177"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="abe92-178">Seja seguro e use **ULONG \_ PTR** para todos os endereços e matemáticas de ponteiros.</span><span class="sxs-lookup"><span data-stu-id="abe92-178">Be safe and use **ULONG\_PTR** for all address and pointer math.</span></span>

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a><span data-ttu-id="abe92-179">Aviso C4311 exemplo 3</span><span class="sxs-lookup"><span data-stu-id="abe92-179">Warning C4311 Example 3</span></span>

<span data-ttu-id="abe92-180">' Type cast ': truncamento de ponteiro de ' void \* \_ \_ ptr64 ' para ' unsinaled Long '</span><span class="sxs-lookup"><span data-stu-id="abe92-180">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="abe92-181"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar</span><span class="sxs-lookup"><span data-stu-id="abe92-181"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
PVOID
HalDereferenceQva(
PVOID Qva,
INTERFACE_TYPE InterfaceType,
ULONG BusNumber)

if ( ((ULONG) Qva & QVA_SELECTORS) == QVA_ENABLE ) {

return( (PVOID)( (ULONG)Qva << IO_BIT_SHIFT ) );
} 
else {
return (Qva);
}
```

</dd> <dt>

<span data-ttu-id="abe92-182"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="abe92-182"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="abe92-183">O compilador avisa sobre o endereço dos operadores (&) e SHIFT esquerda (<<) se eles são aplicados aos tipos de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="abe92-183">The compiler warns about the address of (&) and left shift (<<) operators if they are applied to pointer types.</span></span> <span data-ttu-id="abe92-184">No código acima, Qva é um valor de **pVoid** .</span><span class="sxs-lookup"><span data-stu-id="abe92-184">In the above code, Qva is a **PVOID** value.</span></span> <span data-ttu-id="abe92-185">Precisamos converter isso em um tipo inteiro para executar a matemática.</span><span class="sxs-lookup"><span data-stu-id="abe92-185">We need to cast that to an integer type to perform the math.</span></span> <span data-ttu-id="abe92-186">Como o código deve ser portátil, use **ULONG \_ PTR** em vez de **ULONG**.</span><span class="sxs-lookup"><span data-stu-id="abe92-186">Because the code must be portable, use **ULONG\_PTR** instead of **ULONG**.</span></span>

</dd> <dt>

<span data-ttu-id="abe92-187"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções</span><span class="sxs-lookup"><span data-stu-id="abe92-187"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a><span data-ttu-id="abe92-188">Exemplo de C4311 de aviso 4</span><span class="sxs-lookup"><span data-stu-id="abe92-188">Warning C4311 Example 4</span></span>

<span data-ttu-id="abe92-189">' Type cast ': truncamento de ponteiro de ' void \* \_ \_ ptr64 ' para ' unsinaled Long '</span><span class="sxs-lookup"><span data-stu-id="abe92-189">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="abe92-190"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar</span><span class="sxs-lookup"><span data-stu-id="abe92-190"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
TranslatedAddress->LowPart = (ULONG)HalCreateQva(
*TranslatedAddress, va);
```

</dd> <dt>

<span data-ttu-id="abe92-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="abe92-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="abe92-192">TranslatedAddress é uma União semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="abe92-192">TranslatedAddress is a union that looks something like the following:</span></span>

``` syntax
typedef union
   Struct {
      ULONG LowPart;
      LONG Highpart;
   }
   LONGLONG QuadPart;
}
```

</dd> <dt>

<span data-ttu-id="abe92-193"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções</span><span class="sxs-lookup"><span data-stu-id="abe92-193"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="abe92-194">Sabendo o que o restante do código pode colocar em Highpart, podemos selecionar uma das soluções mostradas aqui.</span><span class="sxs-lookup"><span data-stu-id="abe92-194">Knowing what the rest of the code might place in Highpart, we can select either of the solutions shown here.</span></span>

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

<span data-ttu-id="abe92-195">A macro **PtrToUlong** trunca o ponteiro retornado por **HalCreateQva** para 32 bits.</span><span class="sxs-lookup"><span data-stu-id="abe92-195">The **PtrToUlong** macro truncates the pointer returned by **HalCreateQva** to 32 bits.</span></span> <span data-ttu-id="abe92-196">Sabemos que o QVA retornado por **HalCreateQva** tem os bits de 32 superiores definidos como zero e a próxima linha de código define TranslatedAddress->Highpart como zero.</span><span class="sxs-lookup"><span data-stu-id="abe92-196">We know that the QVA returned by **HalCreateQva** has the upper 32 bits set to zero and the very next line of code sets TranslatedAddress->Highpart to zero.</span></span>

<span data-ttu-id="abe92-197">Com cautela, poderíamos usar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="abe92-197">With caution, we could use the following:</span></span>

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

<span data-ttu-id="abe92-198">Isso funciona neste exemplo: a macro **HalCreateQva** está retornando 64 bits, com os bits 32 superiores definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="abe92-198">This works in this example: the **HalCreateQva** macro is returning 64 bits, with the upper 32 bits set to zero.</span></span> <span data-ttu-id="abe92-199">Apenas tenha cuidado para não deixar os bits 32 superiores indefinidos em um ambiente de 32 bits, que essa segunda solução pode realmente fazer.</span><span class="sxs-lookup"><span data-stu-id="abe92-199">Just be careful not to leave the upper 32 bits undefined in a 32-bit environment, which this second solution may actually do.</span></span>

</dd> </dl>

## <a name="warning-c4311-example-5"></a><span data-ttu-id="abe92-200">Exemplo de aviso C4311 5</span><span class="sxs-lookup"><span data-stu-id="abe92-200">Warning C4311 Example 5</span></span>

<span data-ttu-id="abe92-201">' Type cast ': truncamento de ponteiro de ' void \* \_ \_ ptr64 ' para ' unsinaled Long '</span><span class="sxs-lookup"><span data-stu-id="abe92-201">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="abe92-202"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar</span><span class="sxs-lookup"><span data-stu-id="abe92-202"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
VOID
HalpCiaProgramDmaWindow(
PWINDOW_CONTROL_REGISTERS WindowRegisters,
PVOID MapRegisterBase
)
{
CIA_WBASE Wbase;

Wbase.all = 0;
Wbase.Wen = 1;
Wbase.SgEn = 1;
Wbase.Wbase = (ULONG)(WindowRegisters->WindowBase) >> 20;
```

</dd> <dt>

<span data-ttu-id="abe92-203"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="abe92-203"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="abe92-204">WindowRegisters->WindowBase é um ponteiro e agora é de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="abe92-204">WindowRegisters->WindowBase is a pointer and is now 64 bits.</span></span> <span data-ttu-id="abe92-205">O código diz para alternar para a direita esse valor 20 bits.</span><span class="sxs-lookup"><span data-stu-id="abe92-205">The code says to right-shift this value 20 bits.</span></span> <span data-ttu-id="abe92-206">O compilador não nos permitirá usar o operador right-shift (>>) em um ponteiro; Portanto, precisamos convertê-lo em algum tipo de inteiro.</span><span class="sxs-lookup"><span data-stu-id="abe92-206">The compiler will not let us use the right-shift (>>) operator on a pointer; therefore, we need to cast it to some sort of integer.</span></span>

</dd> <dt>

<span data-ttu-id="abe92-207"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções</span><span class="sxs-lookup"><span data-stu-id="abe92-207"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

<span data-ttu-id="abe92-208">A conversão para um **ULONG \_ PTR** é exatamente o que precisamos.</span><span class="sxs-lookup"><span data-stu-id="abe92-208">Casting to a **ULONG\_PTR** is just what we need.</span></span> <span data-ttu-id="abe92-209">O próximo problema é o Wbase.</span><span class="sxs-lookup"><span data-stu-id="abe92-209">The next problem is Wbase.</span></span> <span data-ttu-id="abe92-210">Wbase é um **ULONG** e é de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="abe92-210">Wbase is a **ULONG** and is 32 bits.</span></span> <span data-ttu-id="abe92-211">Nesse caso, sabemos que o ponteiro de 64 bits WindowRegisters->WindowBase é válido na parte inferior 32 bits mesmo depois de ser deslocado.</span><span class="sxs-lookup"><span data-stu-id="abe92-211">In this case, we know that the 64-bit pointer WindowRegisters->WindowBase is valid in the lower 32 bits even after being shifted.</span></span> <span data-ttu-id="abe92-212">Isso usa a macro **PtrToUlong** aceitável, pois ele truncará o ponteiro de 64 bits em um **ULONG** de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="abe92-212">This makes use of the **PtrToUlong** macro acceptable, because it will truncate the 64-bit pointer into a 32-bit **ULONG**.</span></span> <span data-ttu-id="abe92-213">A conversão **pVoid** é necessária porque o **PtrToUlong** espera um argumento de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="abe92-213">The **PVOID** cast is necessary because **PtrToUlong** expects a pointer argument.</span></span> <span data-ttu-id="abe92-214">Quando você examina o código resultante do Assembler, toda essa conversão de código C se torna apenas uma carga Quad, Shift Right e Store Long.</span><span class="sxs-lookup"><span data-stu-id="abe92-214">When you look at the resulting assembler code, all this C code casting becomes just a load quad, shift right, and store long.</span></span>

</dd> </dl>

 

 




