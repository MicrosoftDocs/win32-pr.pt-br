---
title: Recurso RCDATA
description: Define um recurso de dados brutos para um aplicativo. Os recursos de dados brutos permitem a inclusão de dados binários diretamente no arquivo executável.
ms.assetid: 7535cb06-858b-4726-aaa5-43519f84d0e4
keywords:
- Menus de recursos do RCDATA e outros recursos
topic_type:
- apiref
api_name:
- RCDATA
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44de0e71e3ba744f668535950224129b91bc3653
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916806"
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

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instruções opcionais*
</dt> <dd>

Esse parâmetro pode ser zero ou mais das instruções a seguir.



| Instrução                                                        | Descrição                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Características**](characteristics-statement.md) *DWORD*     | Informações definidas pelo usuário sobre um recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos. Para obter mais informações, consulte [**características**](characteristics-statement.md). |
| [](language-statement.md) *Idioma* do idioma, *subidioma* | Idioma do recurso. Para obter mais informações, consulte [**Language**](language-statement.md).                                                                                            |
| [](version-statement.md) *DWORD* da versão                     | Número de versão definido pelo usuário para o recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos. Para obter mais informações, consulte [**versão**](version-statement.md).              |



 

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*dados brutos*
</dt> <dd>

Dados brutos que consistem em um ou mais números inteiros ou cadeias de caracteres. Os inteiros podem ser especificados em formato decimal, octal ou hexadecimal. Para ser compatível com o Windows de 16 bits, os inteiros são armazenados como valores de **palavra** . Você pode armazenar um inteiro como um valor **DWORD** qualificando o inteiro com o sufixo "L".

As cadeias de caracteres são colocadas entre aspas. O RC não acrescenta automaticamente um caractere nulo de terminação a uma cadeia de caracteres. Cada cadeia de caracteres é uma sequência dos caracteres ANSI especificados, a menos que você o qualifique como uma cadeia de caracteres largos com o prefixo L.

O bloco de dados começa em um limite **DWORD** e o RC não executa nenhum preenchimento ou alinhamento de dados dentro do bloco de *dados brutos* . É sua responsabilidade garantir o alinhamento adequado dos dados dentro do bloco.

</dd> </dl>

Alguns atributos também têm suporte para compatibilidade com versões anteriores. Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da instrução **RCDATA** :

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

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**CARACTERÍSTICAS**](characteristics-statement.md)
</dt> <dt>

[**LANGUAGE**](language-statement.md)
</dt> <dt>

[**ADICIONARMENU**](menu-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**VERSION**](version-statement.md)
</dt> </dl>

 

 




