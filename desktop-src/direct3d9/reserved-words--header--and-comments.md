---
description: A tabela a seguir mostra quais palavras são reservadas e não devem ser usadas.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Palavras reservadas, cabeçalho e comentários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f583084b3faa4777a5fe6031cc247fdb99c27cc1fb23c6a5676e60afe00aba20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044274"
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
| Tamanho do float     | x        | 0064            |       | floats de 64 bits                |
|                | x        | "0032"          |       | floats de 32 bits                |



 

Os valores na tabela são delimitados por aspas para chamar a atenção para o número de caracteres em cada valor. Aqueles com 4 bytes contêm quatro caracteres, aqueles com 2 bytes contêm dois caracteres.

Os comentários são aplicáveis somente em arquivos de texto. Os comentários podem ocorrer em qualquer lugar no fluxo de dados. Um comentário começa com as barras duplas do estilo C++ (//) ou um sinal de sustenido ( \# ). O comentário é executado na próxima linha nova. O exemplo a seguir mostra comentários válidos.


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificação de texto](text-encoding.md)
</dt> </dl>

 

 



