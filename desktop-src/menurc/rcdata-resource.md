---
title: Recurso RCDATA
description: Define um recurso de dados brutos para um aplicativo. Os recursos de dados brutos permitem a inclusão de dados binários diretamente no arquivo executável.
ms.assetid: 7535cb06-858b-4726-aaa5-43519f84d0e4
keywords:
- Menus de recurso RCDATA e outros recursos
topic_type:
- apiref
api_name:
- RCDATA
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f813bde1195d8adcad708c40857cc11b1e7b70f696455168e174a4bf2f6cf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847036"
---
# <a name="rcdata-resource"></a>Recurso RCDATA

Define um recurso de dados brutos para um aplicativo. Os recursos de dados brutos permitem a inclusão de dados binários diretamente no arquivo executável.

``` syntax
nameID RCDATA  [optional-statements] {raw-data  ...}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome exclusivo ou um valor inteiro sem sinal de 16 bits que identifica o recurso.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*
</dt> <dd>

Esse parâmetro pode ser zero ou mais das instruções a seguir.



| Instrução                                                        | Descrição                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CHARACTERISTICS**](characteristics-statement.md) *dword*     | Informações definidas pelo usuário sobre um recurso que pode ser usado por ferramentas que leem e escrevem arquivos de recurso. Para obter mais informações, consulte [**CARACTERÍSTICAS**](characteristics-statement.md). |
| [**Language**](language-statement.md) *language*, *sublanguage* | Idioma do recurso. Para obter mais informações, consulte [**LANGUAGE**](language-statement.md).                                                                                            |
| [**VERSION**](version-statement.md) *dword*                     | Número de versão definido pelo usuário para o recurso que pode ser usado por ferramentas que leem e escrevem arquivos de recurso. Para obter mais informações, consulte [**VERSION**](version-statement.md).              |



 

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*dados brutos*
</dt> <dd>

Dados brutos que consistem em um ou mais inteiros ou cadeias de caracteres. Inteiros podem ser especificados em formato decimal, octal ou hexadecimal. Para ser compatível com o Windows de 16 bits, os inteiros são armazenados como valores **WORD.** Você pode armazenar um inteiro como um **valor DWORD** qualificando o inteiro com o sufixo "L".

As cadeias de caracteres são entre aspas. RC não anexa automaticamente um caractere nulo de terminação a uma cadeia de caracteres. Cada cadeia de caracteres é uma sequência dos caracteres ANSI especificados, a menos que você a qualifique como uma cadeia de caracteres largos com o prefixo L.

O bloco de dados começa em um limite **DWORD** e o RC não executa nenhum preenchimento ou alinhamento de dados dentro do *bloco de dados* brutos. É sua responsabilidade garantir o alinhamento adequado dos dados dentro do bloco.

</dd> </dl>

Determinados atributos também têm suporte para compatibilidade com backward. Para obter mais informações, consulte [Common Resource Attributes](common-resource-attributes.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da **instrução RCDATA:**

``` syntax
resname RCDATA
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Aceleradores**](accelerators-resource.md)
</dt> <dt>

[**Características**](characteristics-statement.md)
</dt> <dt>

[**Língua**](language-statement.md)
</dt> <dt>

[**Menu**](menu-resource.md)
</dt> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> <dt>

[**Versão**](version-statement.md)
</dt> </dl>

 

 




