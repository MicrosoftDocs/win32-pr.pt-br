---
title: Erros comuns do compilador
description: Esta seção ilustra os erros de compilador típicos que ocorrem durante a migração de uma base de código existente. Esses exemplos são de código HAL de nível de sistema, embora os conceitos sejam diretamente aplicáveis ao código de nível de usuário.
ms.assetid: bbb6a57f-281a-4a6e-a4b6-15846d0cf21f
keywords:
- erros de compilador 64-bit Windows programação
- migração de 64 bits Windows-programação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55d12e7c5566b5cb2b934eefb71b1b51858f278d3e408d3080cb1810f185dcfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071636"
---
# <a name="common-compiler-errors"></a>Erros comuns do compilador

Esta seção ilustra os erros de compilador típicos que ocorrem durante a migração de uma base de código existente. Esses exemplos são de código HAL de nível de sistema, embora os conceitos sejam diretamente aplicáveis ao código de nível de usuário.

## <a name="warning-c4311-example-1"></a>Exemplo de C4311 de aviso 1

' Type cast ': truncamento de ponteiro de ' void \* \_ \_ ptr64 ' para ' sem sinal longo

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

**PtrToUlong** é uma função ou macro embutida, dependendo do seu uso. Ele Trunca um ponteiro para um **ULONG**. Embora os ponteiros de 32 bits não sejam afetados, a metade superior de um ponteiro de 64 bits é truncada.

\_ \_ \_ A base de configuração \_ de PCI CIA QVA é declarada como um **pVoid**. A conversão **ULONG** funciona no mundo de 32 bits, mas resulta em um erro no mundo de 64 bits. A solução é obter um ponteiro de 64 bits para um **ULONG**, pois alterar a definição da União que pPciAddr->u. asulong é definido em alterações de código demais.

O uso da macro **PtrToUlong** para converter o **pVoid** de 64 bits para o **ULONG** necessário é permitido porque temos conhecimento sobre o valor específico da QVA de configuração de CIA \_ PCI \_ \_ \_ . Nesse caso, esse ponteiro nunca terá dados nos 32 bits superiores.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a>Exemplo de C4311 de aviso 2

' Type cast ': truncamento de ponteiro de ' struct \_ Error \_ frame \* \_ \_ ptr64 ' para ' sem sinal longo

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

O problema é que o último parâmetro para essa função é um ponteiro para uma estrutura de dados. Como PUncorrectableError é um ponteiro, ele muda de tamanho com o modelo de programação. O protótipo para **KeBugCheckEx** foi alterado para que o último parâmetro seja um **ULONG \_ PTR**. Como resultado, é necessário converter o ponteiro de função em um **\_ PTR**.

Você pode perguntar por que **pVoid** não foi usado como o último parâmetro. Dependendo do contexto da chamada, o último parâmetro pode ser algo diferente de um ponteiro ou talvez um código de erro.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a>Exemplo de C4244 de aviso 1

' = ': conversão de ' struct \_ Configuration \_ Component \* \_ \_ ptr64 ' para ' struct \_ Configuration \_ Component \* ', possível perda de dados

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

A função declara o componente variável como um componente PCONFIGURATION \_ . Posteriormente, a variável será usada na seguinte atribuição que aparece correta:

`Component = &CurrentEntry->ComponentEntry;`

No entanto, o componente de tipo PCONFIGURATION \_ é definido como:

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

A definição de tipo para o \_ componente PCONFIGURATION fornece um ponteiro de 32 bits nos modelos de 32 bits e 64 bits porque ele é declarado como **ponteiro \_ 32**. O designer original dessa estrutura sabia que ela será usada em um contexto de 32 bits no BIOS e definiu-a expressamente para esse uso. esse código funciona bem em Windows de 32 bits porque os ponteiros são de 32 bits. no Windows de 64 bits, ele não funciona porque o código está no contexto de 64 bits.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções
</dt> <dd>

Para contornar esse problema, use \_ o componente \* de configuração em vez do componente PCONFIGURATION-bit de 32 bits \_ . É importante entender claramente a finalidade do código. Se esse código for destinado a tocar o BIOS de 32 bits ou o espaço do sistema, essa correção não funcionará.

O **ponteiro \_ 32** é definido em Ntdef. h e Winnt. h.

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a>Exemplo de C4242 de aviso 2

' = ': conversão de ' \_ \_ Int64 ' para ' não assinado longo ', possível perda de dados

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

Esse aviso é gerado porque o cálculo está usando valores de 64 bits, nesse caso, aponta e coloca o resultado em um **ULONG** de 32 bits.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções
</dt> <dd>

Tipo converta o resultado do cálculo para um **ULONG** , conforme mostrado aqui:

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

Typecasting o resultado permite que o compilador saiba que você tem certeza sobre o resultado. Dito isso, certifique-se de que você entende o cálculo e realmente tem certeza de que ele caberá em um **ULONG** de 32 bits.

Se o resultado não couber em um **ULONG** de 32 bits, altere o tipo base da variável que irá conter o resultado.

</dd> </dl>

## <a name="warning-c4311---example-1"></a>Aviso C4311-exemplo 1

' Type cast ': truncamento de ponteiro de ' void \* \_ \_ ptr64 ' para ' unsinaled Long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

Essa função inteira lida com endereços como inteiros, exigindo a necessidade de digitar esses inteiros de forma portátil. Todas as variáveis locais, valores intermediários em cálculos e valores de retorno devem ser tipos portáteis.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções
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

**Pulong \_ PTR** é um ponteiro que é, em si, 32 bits para Windows de 32 bits e 64 bits para Windows de 64 bits. ele aponta para um inteiro não assinado, **ULONG \_ PTR**, que é de 32 bits para 32 bits Windows e 64 bits para Windows de 64 bits.

</dd> </dl>

## <a name="warning-c4311---example-2"></a>Aviso C4311-exemplo 2

' Type cast ': truncamento de ponteiro de ' void \* \_ \_ ptr64 ' para ' unsinaled Long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

Embora todos os valores de QVA (quase virtual address) sejam realmente valores de 32 bits nesse estágio e caibam em **ULONG**, ele é mais consistente para tratar todos os endereços como valores do **ULONG \_ PTR** quando possível.

O ponteiro PciIoSpaceBase contém o QVA que é criado na macro HAL \_ Make \_ QVA. Essa macro retorna um valor de 64 bits com os primeiros 32 bits definidos como zero para que o cálculo funcione. Poderíamos simplesmente deixar o código para truncar o ponteiro em um **ULONG**, mas essa prática não é recomendada para aprimorar a manutenção e a portabilidade do código. Por exemplo, o conteúdo de um QVA pode ser alterado no futuro para usar alguns dos bits superiores nesse nível, dividindo o código.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções
</dt> <dd>

Seja seguro e use **ULONG \_ PTR** para todos os endereços e matemáticas de ponteiros.

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a>Aviso C4311 exemplo 3

' Type cast ': truncamento de ponteiro de ' void \* \_ \_ ptr64 ' para ' unsinaled Long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

O compilador avisa sobre o endereço dos operadores (&) e SHIFT esquerda (<<) se eles são aplicados aos tipos de ponteiro. No código acima, Qva é um valor de **pVoid** . Precisamos converter isso em um tipo inteiro para executar a matemática. Como o código deve ser portátil, use **ULONG \_ PTR** em vez de **ULONG**.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a>Exemplo de C4311 de aviso 4

' Type cast ': truncamento de ponteiro de ' void \* \_ \_ ptr64 ' para ' unsinaled Long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar
</dt> <dd>

``` syntax
TranslatedAddress->LowPart = (ULONG)HalCreateQva(
*TranslatedAddress, va);
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

TranslatedAddress é uma União semelhante à seguinte:

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

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluções
</dt> <dd>

Sabendo o que o restante do código pode colocar em Highpart, podemos selecionar uma das soluções mostradas aqui.

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

A macro **PtrToUlong** trunca o ponteiro retornado por **HalCreateQva** para 32 bits. Sabemos que o QVA retornado por **HalCreateQva** tem os bits de 32 superiores definidos como zero e a próxima linha de código define TranslatedAddress->Highpart como zero.

Com cautela, poderíamos usar o seguinte:

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

Isso funciona neste exemplo: a macro **HalCreateQva** está retornando 64 bits, com os bits 32 superiores definidos como zero. Apenas tenha cuidado para não deixar os bits 32 superiores indefinidos em um ambiente de 32 bits, que essa segunda solução pode realmente fazer.

</dd> </dl>

## <a name="warning-c4311-example-5"></a>Exemplo de aviso C4311 5

'type cast': truncamento de ponteiro de 'void \* \_ \_ ptr64' para 'unsigned long'

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Código
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

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrição
</dt> <dd>

WindowRegisters->WindowBase é um ponteiro e agora tem 64 bits. O código diz para deslocar para a direita esse valor de 20 bits. O compilador não nos permitirá usar o operador de deslocamento à direita (>>) em um ponteiro; portanto, precisamos castiá-lo em algum tipo de inteiro.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solução
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

A transmissão para **um \_ PTR ULONG** é exatamente o que precisamos. O próximo problema é o Wbase. O Wbase é **um ULONG** e tem 32 bits. Nesse caso, sabemos que o ponteiro de 64 bits WindowRegisters->WindowBase é válido nos 32 bits inferiores mesmo depois de ser deslocado. Isso torna o uso da macro **PtrToUlong** aceitável, pois ele truncará o ponteiro de 64 bits em um ULONG de 32 **bits.** A **cast PVOID** é necessária porque **PtrToUlong** espera um argumento de ponteiro. Quando você vê o código do assembler resultante, toda essa transmissão de código C torna-se apenas um quad de carga, deslocamento para a direita e armazenamento longo.

</dd> </dl>

 

 




