---
description: O ICE32 valida que as chaves e as chaves estrangeiras no arquivo .msi são dos mesmos tipos de definição de coluna e tamanho.
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12e9361cd091afea3444858e64e043b87b779c2313f0ba16bb0ec6cf58fad265
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528616"
---
# <a name="ice32"></a>ICE32

O ICE32 valida que as chaves e as chaves estrangeiras no arquivo .msi são dos mesmos tipos de definição de coluna e tamanho. Essa ação personalizada ICE faz a comparação usando a tabela [ \_ Validação](-validation-table.md) e usando os tipos de definição retornados por [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo). Para obter mais informações, consulte [Formato de definição de coluna](column-definition-format.md).

## <a name="result"></a>Resultado

ICE32 posta erros se o arquivo .msi contém chaves estrangeiras para chaves de um tipo de dados de coluna ou comprimento de coluna diferente.

## <a name="example"></a>Exemplo

ICE32 posta dois erros para o exemplo mostrado:

-   Há uma chave estrangeira e uma chave definidas que diferem em tamanho.
-   Há uma chave estrangeira e uma chave definidas que diferem em seu tipo de definição.

[ \_ Tabela de validação](-validation-table.md) (parcial)



| Tabela | Coluna  | Keytable | KeyColumn |
|-------|---------|----------|-----------|
| Arquivo  | Versão | Arquivo     | 1         |
| Aba  | Coluna8 | Aba     | 1         |



 

Definições de coluna (parcial)



| Tabela | Coluna  | Tipo | Tamanho |
|-------|---------|------|------|
| Arquivo  | Arquivo    | s    | 72   |
| Arquivo  | Versão | S    | 32   |
| Aba  | Column1 | i    | 2    |
| Aba  | Coluna8 | S    | 32   |



 

A coluna Versão da tabela Arquivo pode ser uma chave estrangeira para outro arquivo na tabela Arquivo. Isso ocorre com arquivos de adoção. No entanto, a coluna Versão permite apenas um comprimento de cadeia de caracteres 32, enquanto a coluna Arquivo permite um comprimento de cadeia de caracteres 72. Para corrigir esse erro, altere os comprimentos da cadeia de caracteres para corresponder.

Há uma chave estrangeira e uma chave definidas que diferem em seus tipos de definição. Column8 da Tabela de Colcha é listada como uma chave estrangeira para Column1. Column8 é uma coluna de cadeia de caracteres e Column1 é uma coluna de inteiro. Os pares chave estrangeira e chave devem ser definidos para que seus tipos de dados sejam corresponderem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



