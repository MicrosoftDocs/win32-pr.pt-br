---
title: Atributos de matriz e de Sized-Pointer
description: O MIDL fornece um rico conjunto de recursos para passar matrizes de dados e ponteiros para dados. Você pode usar esses atributos para especificar características de matrizes e vários níveis de ponteiros.
ms.assetid: 482be83f-eb09-40a0-8dd6-a0cbf5dc4485
keywords:
- MIDL de IDL, atributos, matriz e ponteiro de tamanho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f9ba435d5c413ea152c2bc9b492486ccc1be94
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823716"
---
# <a name="array-and-sized-pointer-attributes"></a>Atributos de matriz e de Sized-Pointer

O MIDL fornece um rico conjunto de recursos para passar matrizes de dados e ponteiros para dados. Você pode usar esses atributos para especificar características de matrizes e vários níveis de ponteiros.



| Atributo                       | Uso                                                                                                                                                                                                |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**o tamanho \_ é**](size-is.md)     | Especifica a quantidade de memória a ser alocada para ponteiros de tamanho, ponteiros de tamanho para ponteiros de tamanho e matrizes de dimensão única ou multidimensional.                                                         |
| [**máximo \_ é**](max-is.md)       | O valor máximo para um índice de matriz.                                                                                                                                                                |
| [**comprimento \_ é**](length-is.md) | O número de elementos da matriz a serem transmitidos.                                                                                                                                                      |
| [**primeiro \_ é**](first-is.md)   | O índice do primeiro elemento de matriz a ser transmitido.                                                                                                                                              |
| [**último \_ é**](last-is.md)     | Fornece o índice do último elemento de matriz a ser transmitido.                                                                                                                                         |
| [**string**](string.md)        | Indica que a matriz de [**caracteres**](char-idl.md)unidimensionais, [**WCHAR \_ t**](wchar-t.md), [**byte**](byte.md) (ou equivalente) ou o ponteiro para tal matriz deve ser manipulada como uma cadeia de caracteres. |
| [**amplitude**](range.md)          | Especifica um intervalo de valores permitidos para argumentos ou campos cujos valores são definidos em tempo de execução.                                                                                                       |



 

O MIDL dá suporte a três tipos de ponteiros: ponteiros de referência, ponteiros exclusivos e ponteiros completos. Esses ponteiros são especificados pelos atributos de ponteiro [**ref**](ref.md), [**Unique**](unique.md)e [**PTR**](ptr.md).

Um atributo de ponteiro pode ser aplicado como um atributo de tipo; como um atributo de campo que se aplica a um membro de estrutura, um membro de União ou um parâmetro; ou como um atributo de função que se aplica ao tipo de retorno da função. O atributo pointer também pode aparecer com a palavra-chave [**\_ default do ponteiro**](pointer-default.md) .

Para permitir que um parâmetro de ponteiro seja alterado no valor durante uma função remota, você deve fornecer outro nível de indireção fornecendo vários declaradores de ponteiro. O atributo de ponteiro explícito aplicado ao parâmetro afeta apenas o Declarador de ponteiro mais à direita para o parâmetro. Quando há vários declaradores de ponteiro em uma declaração de parâmetro, os outros declaradores assumem como padrão o atributo pointer especificado pelo atributo [**\_ default do ponteiro**](pointer-default.md) . Para aplicar diferentes atributos de ponteiro a vários declaradores de ponteiro, você deve definir tipos intermediários que especificam os atributos de ponteiro explícitos.

## <a name="default-pointer-attribute-values"></a>Valores de Pointer-Attribute padrão

Quando nenhum atributo de ponteiro está associado a um ponteiro que é um parâmetro, presume-se que o ponteiro seja um ponteiro de [**referência**](ref.md) .

Quando nenhum atributo de ponteiro está associado a um ponteiro que é membro de uma estrutura ou União, o compilador MIDL atribui atributos de ponteiro usando as seguintes regras de prioridade (1 é a mais alta):

1.  Atributos aplicados explicitamente ao tipo de ponteiro
2.  Atributos aplicados explicitamente ao parâmetro ou ao membro do ponteiro
3.  O [**atributo \_ padrão de ponteiro**](pointer-default.md) no arquivo IDL que define o tipo
4.  O [**atributo \_ padrão de ponteiro**](pointer-default.md) no arquivo IDL que importa o tipo
5.  [**PTR**](ptr.md) (modo uso); [**exclusivo**](unique.md) (modo Microsoft RPC padrão)

Quando o arquivo IDL é compilado no modo padrão, os arquivos importados podem herdar atributos de ponteiro de Importando arquivos. Esse recurso não está disponível quando você compila usando a opção/[**uso**](-osf.md) . Para obter mais informações, consulte [**importar**](import.md).

## <a name="function-return-types"></a>Tipos de retorno de função

Um ponteiro retornado por uma função deve ser um ponteiro [**exclusivo**](unique.md) ou um ponteiro completo. O compilador MIDL relatará um erro se um resultado de função for um ponteiro de referência, explicitamente ou por padrão. O ponteiro retornado sempre indica um novo armazenamento.

As funções que retornam um valor de ponteiro podem especificar um atributo de ponteiro como um atributo de função. Se um atributo de ponteiro não estiver presente, o ponteiro de resultado da função usará o valor fornecido como o atributo [**\_ padrão do ponteiro**](pointer-default.md) .

## <a name="pointer-attributes-in-type-definitions"></a>Atributos de ponteiro em definições de tipo

Quando você especifica um atributo de ponteiro no nível superior de uma instrução [**typedef**](typedef.md) , o atributo especificado é aplicado ao Declarador de ponteiro, conforme esperado. Quando nenhum atributo de ponteiro é especificado, os declaradores de ponteiro no nível superior de uma instrução typedef herdam o tipo de atributo pointer quando usado.

A IDL de DCE não permite que o mesmo atributo de ponteiro seja explicitamente aplicado duas vezes — por exemplo, na declaração de [**typedef**](typedef.md) e na lista de atributos de parâmetro. Quando você usa o modo padrão (extensões da Microsoft) do compilador MIDL, essa restrição é reduzida.

Para obter uma discussão sobre como usar matrizes MIDL e ponteiros em chamadas de procedimento remoto, consulte [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).

 

 