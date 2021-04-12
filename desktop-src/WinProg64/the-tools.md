---
title: As ferramentas
description: Este tópico descreve as ferramentas disponíveis para você usar o para tornar seu aplicativo 64-bit pronto. O Windows 10 está disponível para processadores baseados em x64 e ARM64.
ms.assetid: 457b7cc1-8517-4a36-9a0c-cf191ff3b374
keywords:
- Guia de programação do Windows de 64 bits – programação do Windows de 64 bits, ferramentas
- ferramentas de programação de 64 bits do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87fb315200ae32eb1e1441ed330be49aa02d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364290"
---
# <a name="the-tools"></a>As ferramentas

Este tópico descreve as ferramentas disponíveis para você usar o para tornar seu aplicativo 64-bit pronto. O Windows 10 está disponível para processadores baseados em x64 e ARM64.

## <a name="include-files"></a>Arquivos de inclusão

Os elementos da API são praticamente idênticos entre as janelas de 32 e 64 bits. Os arquivos de cabeçalho do Windows foram modificados para que possam ser usados para o código de 32 e 64 bits. Os novos tipos de 64 bits e as macros são definidos em um novo arquivo de cabeçalho, Basetsd. h, que está no conjunto de arquivos de cabeçalho incluídos pelo Windows. h. O Basetsd. h inclui as novas definições de tipo de dados para ajudar a tornar independente o tamanho do Word do código-fonte.

## <a name="new-data-types"></a>Novos tipos de dados

Os arquivos de cabeçalho do Windows contêm novos tipos de dados. Esses tipos são principalmente para compatibilidade de tipo com os tipos de dados de 32 bits. Os novos tipos fornecem exatamente a mesma digitação dos tipos existentes, enquanto ao mesmo tempo fornecem suporte para o Windows de 64 bits. Para obter mais informações, consulte [os novos tipos de dados](the-new-data-types.md) ou o arquivo de cabeçalho Basetsd. h.

## <a name="predefined-macros"></a>Macros predefinidas

O compilador define as macros a seguir para identificar a plataforma.



| Macro   | Significado                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------|
| \_WIN64 | Uma plataforma de 64 bits. Isso inclui x64 e ARM64.                                                        |
| \_WIN32 | Uma plataforma de 32 bits. Esse valor também é definido pelo compilador de 64 bits para compatibilidade com versões anteriores.<br/> |
| \_WIN16 | Uma plataforma de 16 bits                                                                                           |



 

As macros a seguir são específicas para a arquitetura.



| Macro      | Significado                |
|------------|------------------------|
| \_M \_ IA64  | Plataforma Intel Itanium |
| \_\_IX86 M  | plataforma x86           |
| \_M \_ x64   | plataforma x64           |
| \_\_ARM64 M | Plataforma ARM64         |



 

Não use essas macros, exceto o código específico da arquitetura, em vez disso, use \_ Win64, \_ Win32 e \_ WIN16 sempre que possível.

## <a name="helper-functions"></a>Funções auxiliares

As seguintes funções embutidas (definidas em Basetsd. h) podem ajudá-lo a converter com segurança valores de um tipo para outro.

``` syntax
void            * Handle64ToHandle( const void * POINTER_64 h ) 
void * POINTER_64 HandleToHandle64( const void *h )
long              HandleToLong(     const void *h )
unsigned long     HandleToUlong(    const void *h )
void            * IntToPtr(         const int i )
void            * LongToHandle(     const long h )
void            * LongToPtr(        const long l )
void            * Ptr64ToPtr(       const void * POINTER_64 p )
int               PtrToInt(         const void *p )
long              PtrToLong(        const void *p )
void * POINTER_64 PtrToPtr64(       const void *p )
short             PtrToShort(       const void *p )
unsigned int      PtrToUint(        const void *p )
unsigned long     PtrToUlong(       const void *p )
unsigned short    PtrToUshort(      const void *p )
void            * UIntToPtr(        const unsigned int ui )
void            * ULongToPtr(       const unsigned long ul )
```

> [!WARNING]
> **IntToPtr** Sign-estende o valor **int** , **UIntToPtr** zero-estende o valor **int não assinado** , **LongToPtr** de entrada-estende o valor **longo** e **ULongToPtr** zero estende o valor **longo não atribuído** .

 

## <a name="64-bit-compiler"></a>Compilador de 64 bits

Os compiladores de 64 bits podem ser usados para identificar o truncamento do ponteiro, as conversões incorretas de tipo e outros problemas específicos de 64 bits.

Quando o compilador é executado pela primeira vez, ele provavelmente gerará muitos avisos de truncamento de ponteiro ou de tipo incompatível, como o seguinte:

`warning C4311: 'type cast' : pointer truncation from 'unsigned char *' to 'unsigned long '`

Use esses avisos como um guia para tornar o código mais robusto. É uma boa prática eliminar todos os avisos, especialmente avisos de truncamento de ponteiro.

## <a name="64-bit-compiler-switches-and-warnings"></a>Opções e avisos do compilador de 64 bits

Observe que esse compilador habilita o modelo de dados LLP64.

Há uma opção de aviso para ajudar a portar para o LLP64. A opção-Wp64-w3 habilita os seguintes avisos:

-   C4305: aviso de truncamento. Por exemplo, "Return": truncamento de "Int64 não assinado" para "Long".
-   C4311: aviso de truncamento. Por exemplo, "tipo Cast": truncamento de ponteiro de "int \* \_ ptr64" para "int".
-   C4312: conversão para aviso de tamanho maior. Por exemplo, "tipo Cast": conversão de "int" para "int \* \_ ptr64" de tamanho maior.
-   C4318: passando comprimento zero. Por exemplo, passar constante zero como o comprimento para a função **memset** .
-   C4319: operador NOT. Por exemplo, "~": zero estendendo "sem sinal" longo para "Int64 não assinado" \_ de tamanho maior.
-   C4313: chamando a família de funções **printf** com especificadores e argumentos de tipo de conversão conflitantes. Por exemplo, "printf": "% p" na cadeia de caracteres de formato está em conflito com o argumento 2 do tipo " \_ Int64". Outro exemplo é a chamada printf ("% x", valor de ponteiro \_ ); isso causa um truncamento dos bits 32 superiores. A chamada correta é printf ("% p", valor de ponteiro \_ ).
-   C4244: igual ao C4242 de aviso existente. Por exemplo, "Return": conversão de " \_ Int64" para "int sem sinal", possível perda de dados.

## <a name="64-bit-linker-and-libraries"></a>Bibliotecas e vinculadores de 64 bits

Para compilar aplicativos, use o vinculador e as bibliotecas fornecidas pelo SDK do Windows. A maioria das bibliotecas de 32 bits tem uma versão de 64 bits correspondente, mas determinadas bibliotecas herdadas estão disponíveis somente em versões de 32 bits. O código que chama essas bibliotecas não será vinculado quando o aplicativo for compilado para o Windows de 64 bits.

 

 





