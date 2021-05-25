---
description: A tabela a seguir mostra quais palavras são reservadas e não devem ser usadas.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Palavras reservadas, cabeçalho e comentários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8879d0dbb518f92f0d8a6c38793ab315ae48b73e
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343651"
---
# <a name="reserved-words-header-and-comments"></a>Palavras reservadas, cabeçalho e comentários

A tabela a seguir mostra quais palavras são reservadas e não devem ser usadas.

| Palavras reservadas | Palavras reservadas | Palavras reservadas|
|------------------|----------|-----------|
| ARRAY            | DWORD    | UCHAR     |
| BINARY           | FLOAT    | ULONGLONG |
| \_recurso binário | SDWORD   | UNICODE   |
| CHAR             | STRING   | WORD      |
| CSTRING          | SWORD    |           |
| DOUBLE           | TEMPLATE |           |



 

O cabeçalho de comprimento variável é obrigatório e deve estar no início do fluxo de dados. O cabeçalho contém os dados a seguir.



| Tipo           | Obrigatório | Tamanho (em bytes) | Valor | Descrição                  |
|----------------|----------|-----------------|-------|------------------------------|
| Número mágico   | x        | 4               | xof   |                              |
| Número da versão | x        | 2               | 03    | Versão principal 3              |
|                |          |                 | 03    | Versão secundária 3              |
| Tipo de formato    | x        | 4               | txt   | Arquivo de texto                    |
|                |          |                 | bin   | Arquivo binário                  |
|                |          |                 | tzip  | Arquivo de texto compactado MSZip   |
|                |          |                 | bzip  | Arquivo binário compactado do MSZip |
| Tamanho do float     | x        | 0064            |       | Floats de 64 bits                |
|                | x        | "0032"          |       | Floats de 32 bits                |



 

Os valores na tabela são delimitados por aspas para chamar a atenção para o número de caracteres em cada valor. Aqueles com 4 bytes contêm quatro caracteres, aqueles com 2 bytes contêm dois caracteres.

Os comentários são aplicáveis somente em arquivos de texto. Os comentários podem ocorrer em qualquer lugar no fluxo de dados. Um comentário começa com barras duplas no estilo C++ (//) ou um sinal de quilo \# (). O comentário é executado para a próxima nova linha. O exemplo a seguir mostra comentários válidos.


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificação de texto](text-encoding.md)
</dt> </dl>

 

 



