---
description: ICE32 valida que chaves e chaves estrangeiras no arquivo. msi são do mesmo tamanho e tipos de definição de coluna.
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d6ff9e4de592ac073050b357aff0c63d984f0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753447"
---
# <a name="ice32"></a>ICE32

ICE32 valida que chaves e chaves estrangeiras no arquivo. msi são do mesmo tamanho e tipos de definição de coluna. Essa ação personalizada de ICE faz a comparação usando a [ \_ tabela de validação](-validation-table.md) e usando os tipos de definição que são retornados por [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo). Para obter mais informações, consulte [formato de definição de coluna](column-definition-format.md).

## <a name="result"></a>Resultado

O ICE32 posta erros se o arquivo. msi contém quaisquer chaves estrangeiras para chaves de um tipo de dados de coluna ou comprimento de coluna diferente.

## <a name="example"></a>Exemplo

ICE32 posta dois erros para o exemplo mostrado:

-   Há uma chave estrangeira e uma chave definida que diferem no tamanho.
-   Há uma chave estrangeira e uma chave definida que diferem em seu tipo de definição.

[ \_ Tabela de validação](-validation-table.md) (parcial)



| Tabela | Coluna  | KeyTable | KeyColumn |
|-------|---------|----------|-----------|
| Arquivo  | Versão | Arquivo     | 1         |
| Oscila  | Coluna8 | Oscila     | 1         |



 

Definições de coluna (parcial)



| Tabela | Coluna  | Tipo | Tamanho |
|-------|---------|------|------|
| Arquivo  | Arquivo    | s    | 72   |
| Arquivo  | Versão | S    | 32   |
| Oscila  | Column1 | i    | 2    |
| Oscila  | Coluna8 | S    | 32   |



 

A coluna versão da tabela de arquivos pode ser uma chave estrangeira para outro arquivo na tabela de arquivos. Isso ocorre com arquivos complementares. No entanto, a coluna Version só permite um comprimento de cadeia de caracteres 32, enquanto a coluna File permite um comprimento de cadeia de caracteres 72. Para corrigir esse erro, altere os comprimentos da cadeia de caracteres para correspondência.

Há uma chave estrangeira e uma chave definida que diferem em seus tipos de definição. Column8 da tabela de flap é listada como uma chave estrangeira para column1. Column8 é uma coluna de cadeia de caracteres e column1 é uma coluna de inteiros. Os pares chave estrangeira e chave devem ser definidos para que seus tipos de dados sejam correspondentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



