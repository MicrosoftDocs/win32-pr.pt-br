---
description: Os modelos definem como o fluxo de dados é interpretado – os dados são modulares pela definição do modelo. Esta seção aborda os seguintes aspectos de um modelo e fornece um modelo de exemplo.
ms.assetid: f84978a8-8315-4626-be68-f00f3a72e5ac
title: Modelos (formato de arquivo X, codificação de texto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e164b92c6c5738ad98b138941b1b2fda6c332068
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881031"
---
# <a name="templates-x-file-format-text-encoding"></a>Modelos (formato de arquivo X, codificação de texto)

Os modelos definem como o fluxo de dados é interpretado – os dados são modulares pela definição do modelo. Esta seção aborda os seguintes aspectos de um modelo e fornece um modelo de exemplo.

Há um modelo especial – o modelo de header. É recomendável que cada aplicativo defina um modelo de header e use-o para definir informações específicas do aplicativo, como informações de versão. Se estiver presente, esse header será lido pela API de formato de arquivo .x. Se um membro de sinalizadores estiver disponível, ele será usado para determinar como os dados a seguir são interpretados. O membro de sinalizadores, se definido, deve ser um DWORD. Um bit está definido no momento – bit 0. Se esse bit estiver claro, os dados a seguir no arquivo serão binários. Se definido, os dados a seguir serão texto. Você pode usar vários objetos de dados de header para alternar entre binário e texto dentro do arquivo.

## <a name="template-form-name-and-uuid"></a>Formulário de modelo, nome e UUID

Um modelo tem o seguinte formulário.


```
template <template-name> {
<UUID>
    <member 1>;
...
    <member n>;
[restrictions]
}
```



O nome do modelo é um nome alfanumérico que pode incluir o caractere de sublinhado ( \_ ). Ele não deve começar com um dígito. O UUID é um identificador universal exclusivo formatado para o padrão de Ambiente de Computação Distribuída da Open Software Foundation e entre colchetes angulares (< >). Por exemplo: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.

## <a name="template-members"></a>Membros do modelo

Os membros do modelo consistem em um tipo de dados nomeado seguido por um nome opcional ou uma matriz de um tipo de dados nomeado. Os tipos de dados primitivos válidos são definidos na tabela a seguir.



| Tipo    | Tamanho                               |
|---------|------------------------------------|
| WORD    | 16 bits                            |
| DWORD   | 32 bits                            |
| FLOAT   | Float do IEEE                         |
| DOUBLE  | 64 bits                            |
| CHAR    | 8 bits                             |
| UCHAR   | 8 bits                             |
| BYTE    | 8 bits                             |
| STRING  | Cadeia de caracteres terminada em NULL             |
| CSTRING | Cadeia de caracteres C formatada (sem suporte) |
| UNICODE | Cadeia de caracteres Unicode (sem suporte)     |



 

Tipos de dados adicionais definidos por modelos encontrados anteriormente no fluxo de dados também podem ser referenciados em uma definição de modelo. Nenhuma referência de encaminhamento é permitida.

Qualquer tipo de dados válido pode ser expresso como uma matriz na definição do modelo. A sintaxe básica é mostrada no exemplo a seguir.


```
array <data-type> <name>[<dimension-size>];
```



&lt;dimension-size pode ser um inteiro ou uma referência nomeada para outro membro de &gt; modelo cujo valor é substituído. As matrizes podem ser ndimensionais, em que n é determinado pelo número de colchetes emparelhados à frente da instrução, como no exemplo a seguir.


```
array DWORD FixedHerd[24];
array DWORD Herd[nCows];
array FLOAT Matrix4x4[4][4];
```



## <a name="template-restrictions"></a>Restrições de modelo

Os modelos podem ser abertos, fechados ou restritos. Essas restrições determinam quais tipos de dados podem aparecer na hierarquia imediata de um objeto de dados definido pelo modelo. Um modelo aberto não tem restrições, um modelo fechado rejeita todos os tipos de dados e um modelo restrito permite uma lista nomeada de tipos de dados.

A sintaxe para indicar um modelo aberto é de três períodos entre colchetes.


```
[ ... ]
```



Uma lista separada por vírgulas de tipos de dados nomeados seguida opcionalmente por seus UUIDs entre colchetes indica um modelo restrito.


```
[ { data-type [ UUID ] , } ... ]
```



A ausência de qualquer um dos modelos acima indica um modelo fechado.

## <a name="template-example"></a>Exemplo de modelo

A seguir, é possível ver um modelo de exemplo.


```
template Mesh {
<3D82AB44-62DA-11cf-AB39-0020AF71E433>
DWORD nVertices;
array Vector vertices[nVertices];
DWORD nFaces;
array MeshFace faces[nFaces];
 [ ... ]                // An open template
}
template Vector {
<3D82AB5E-62DA-11cf-AB39-0020AF71E433>
FLOAT x;
FLOAT y;
FLOAT z;
}                        // A closed template
template FileSystem {
<UUID>
STRING name;
[ Directory <UUID>, File <UUID> ]    // A restricted template
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificação de texto](text-encoding.md)
</dt> </dl>

 

 



