---
title: User-Defined recurso
description: Uma instrução de definição de recurso definida pelo usuário define um recurso que contém dados específicos do aplicativo.
ms.assetid: b1cfec71-5733-4900-97f6-c1cbb350c728
keywords:
- recurso definido pelo usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b383b7c4d1f9acfc4ce6c9db24efa77f3bfed943c1f299186d42a1facee2b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472613"
---
# <a name="user-defined-resource"></a>User-Defined recurso

Uma instrução de definição de recurso definida pelo usuário define um recurso que contém dados específicos do aplicativo. Os dados podem ter qualquer formato e podem ser definidos como o conteúdo de um determinado arquivo (se o parâmetro *filename* for fornecido) ou como uma série de números e cadeias de caracteres (se o bloco de *dados brutos* for especificado).

``` syntax
nameID typeID filename
```

O *filename* especifica o nome de um arquivo que contém os dados binários do recurso. O conteúdo do arquivo é incluído como o recurso. O RC não interpreta os dados binários de forma alguma. É responsabilidade do programador garantir que os dados estejam corretamente alinhados à arquitetura do computador de destino.

Um recurso definido pelo usuário também pode ser definido completamente no script de recurso usando a seguinte sintaxe:

``` syntax
nameID typeID  {  raw-data  }
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome exclusivo ou um inteiro de 16 bits sem sinal que identifica o recurso.

</dd> <dt>

<span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*Identificação*
</dt> <dd>

Nome exclusivo ou um inteiro de 16 bits sem sinal que identifica o tipo de recurso. Se um número for fornecido, ele deverá ser maior que 255. Os números de 1 a 255 são reservados para tipos de recursos redefinidos existentes e futuros.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*
</dt> <dd>

Nome do arquivo que contém os dados do recurso. O parâmetro deve ser um nome de arquivo válido; Ele deve ser um caminho completo se o arquivo não estiver no diretório de trabalho atual.

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*dados brutos*
</dt> <dd>

Dados brutos que consistem em um ou mais números inteiros ou cadeias de caracteres. Os inteiros podem ser especificados em formato decimal, octal ou hexadecimal. para ser compatível com Windows de 16 bits, os inteiros são armazenados como valores de palavra. Você pode armazenar um inteiro como um valor DWORD qualificando o inteiro com o sufixo "L".

As cadeias de caracteres são colocadas entre aspas. O RC não acrescenta automaticamente um caractere nulo de terminação a uma cadeia de caracteres. Cada cadeia de caracteres é uma sequência dos caracteres ANSI especificados, a menos que você o qualifique como uma cadeia de caracteres largos com o prefixo "L".

O bloco de dados começa em um limite **DWORD** e o RC não executa nenhum preenchimento ou alinhamento de dados dentro do bloco de *dados brutos* . É responsabilidade do programador garantir o alinhamento adequado dos dados dentro do bloco.

</dd> </dl>

## <a name="example"></a>Exemplo

O exemplo a seguir mostra várias instruções definidas pelo usuário:

``` syntax
array   MYRES   data.res
14      300     custom.res
18 MYRES2
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

 

 




