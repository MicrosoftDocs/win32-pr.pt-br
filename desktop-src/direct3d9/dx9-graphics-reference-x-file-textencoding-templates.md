---
description: Os modelos definem como o fluxo de dados é interpretado-os dados são modulados pela definição do modelo. Esta seção aborda os seguintes aspectos de um modelo e fornece um modelo de exemplo.
ms.assetid: f84978a8-8315-4626-be68-f00f3a72e5ac
title: Modelos (formato de arquivo X, codificação de texto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fccec46e72a73bb5ed4434fd252595e1b072ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645622"
---
# <a name="templates-x-file-format-text-encoding"></a>Modelos (formato de arquivo X, codificação de texto)

Os modelos definem como o fluxo de dados é interpretado-os dados são modulados pela definição do modelo. Esta seção aborda os seguintes aspectos de um modelo e fornece um modelo de exemplo.

Há um modelo especial – o modelo de cabeçalho. É recomendável que cada aplicativo defina um modelo de cabeçalho e use-o para definir informações específicas do aplicativo, como informações de versão. Se estiver presente, esse cabeçalho será lido pela API de formato de arquivo. x. Se um membro flags estiver disponível, ele será usado para determinar como os dados a seguir são interpretados. O membro flags, se definido, deve ser um DWORD. Um bit está definido no momento-bit 0. Se esse bit estiver claro, os dados a seguir no arquivo serão binários. Se definido, os dados a seguir são texto. Você pode usar vários objetos de dados de cabeçalho para alternar entre o binário e o texto dentro do arquivo.

## <a name="template-form-name-and-uuid"></a>Formato, nome e UUID do modelo

Um modelo tem o seguinte formato.


```
template <template-name> {
<UUID>
    <member 1>;
...
    <member n>;
[restrictions]
}
```



O nome do modelo é um nome alfanumérico que pode incluir o caractere de sublinhado ( \_ ). Ele não deve começar com um dígito. O UUID é um identificador universalmente exclusivo formatado para o padrão de ambiente de computação distribuído da Open Software Foundation e envolto por colchetes angulares (< >). Por exemplo: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.

## <a name="template-members"></a>Membros do modelo

Os membros do modelo consistem em um tipo de dados nomeado seguido por um nome opcional ou uma matriz de um tipo de dados nomeado. Os tipos de dados primitivos válidos são definidos na tabela a seguir.



| Type    | Tamanho                               |
|---------|------------------------------------|
| WORD    | 16 bits                            |
| DWORD   | 32 bits                            |
| FLOAT   | IEEE float                         |
| DOUBLE  | 64 bits                            |
| CHAR    | 8 bits                             |
| UCHAR   | 8 bits                             |
| BYTE    | 8 bits                             |
| STRING  | Cadeia de caracteres terminada nula             |
| CSTRING | Cadeia de caracteres C formatada (sem suporte) |
| UNICODE | Cadeia de caracteres Unicode (sem suporte)     |



 

Tipos de dados adicionais definidos por modelos encontrados anteriormente no fluxo de dados também podem ser referenciados dentro de uma definição de modelo. Nenhuma referência progressiva é permitida.

Qualquer tipo de dados válido pode ser expresso como uma matriz na definição do modelo. A sintaxe básica é mostrada no exemplo a seguir.


```
array <data-type> <name>[<dimension-size>];
```



<> de dimensão pode ser um inteiro ou uma referência nomeada a outro membro de modelo cujo valor seja substituído. As matrizes podem ser n-dimensional, em que n é determinado pelo número de colchetes emparelhados que se enquadram na instrução, como no exemplo a seguir.


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



Uma lista separada por vírgulas de tipos de dados nomeados seguidos opcionalmente por seus UUIDs delimitados por colchetes indica um modelo restrito.


```
[ { data-type [ UUID ] , } ... ]
```



A ausência de qualquer um dos itens acima indica um modelo fechado.

## <a name="template-example"></a>Exemplo de modelo

O exemplo a seguir mostra um modelo.


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

[Codificação de Texto](text-encoding.md)
</dt> </dl>

 

 



