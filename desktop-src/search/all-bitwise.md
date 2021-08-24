---
description: As palavras-chave todos os bits e as chaves bit a bit são usadas para testar o bit em um tipo integral.
ms.assetid: 649f763f-45aa-4086-9e7f-b8934b5bd22c
title: Todos os bits e a bit a bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac133e04eae78fe9b943c1e354d9e4dcf451640ad60be1883eecc938ec1d418a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594716"
---
# <a name="all-bitwise-and-some-bitwise"></a>Todos os bits e a bit a bit

As palavras-chave **todos os** **bits e as chaves bit a** bit são usadas para testar o bit em um tipo integral. Se todos os bits de conjunto em uma propriedade corresponderem à máscara, **todos os bit a bit** serão verdadeiros. Se pelo menos um dos conjuntos de bits em uma propriedade corresponder à máscara, **um** valor de bit que for true será verdadeiro.

Os operadores podem ser aplicados a Propriedades escalares (valor único) e propriedades de vetor (valores múltiplos). O exemplo de código a seguir mostra como testar **valores de propriedade** com **todos os bits** e de bit a bit.


```sql
ALL array ALL BITWISE [values?]
ALL array SOME BITWISE [values?]
            
```



## <a name="comparison-operators"></a>Operadores de comparação

Os operadores de comparação com suporte para testes de bits BITais são listados na tabela a seguir.



| Operador de comparação | Descrição  |
|---------------------|--------------|
| =                   | Igual a     |
| ! = ou <>      | É diferente de |



 

A lógica dos testes em bits é listada na tabela a seguir.



| Teste e operador de comparação | Lógica                   |
|--------------------------------------|-------------------------|
| = TODOS OS BITS                        | Máscara de & de propriedade = máscara  |
| = ALGUNS BITS                       | Máscara de & de propriedade! = 0    |
| <> TODOS OS BITS                 | Máscara de & de propriedade! = máscara |
| <> ALGUNS BITS                | Máscara de & de propriedade = 0     |



 

A tabela verdadeira a seguir usa valores binários e hexadecimais de exemplo para demonstrar a lógica de testes bit-a-bit.



| Propriedade em binary (Hex) | Máscara em binário (Hex) | Máscara de & de propriedade = binary (Hex) | = ALGUNS BITS | = TODOS OS BITS |
|--------------------------|----------------------|--------------------------------|----------------|---------------|
| 0001 (0x1)               | 0001 (0x1)           | 0001 (0x1)                     | True           | True          |
| 0001 (0x1)               | 0011 (0x3)           | 0001 (0x1)                     | Verdadeiro           | Falso         |
| 0011 (0x3)               | 0001 (0x1)           | 0001 (0x1)                     | True           | True          |
| 0010 (0x2)               | 0001 (0x1)           | 0000 (0x0)                     | Falso          | Falso         |
| 11110000 (0xF0)          | 00000011 (0x03)      | 00000000 (0x00)                | Falso          | Falso         |
| 11110010 (0xF2)          | 11110010 (0xF2)      | 11110010 (0xF2)                | True           | True          |
| 11110010 (0xF2)          | 00000011 (0x03)      | 00000010 (0x02)                | Verdadeiro           | Falso         |



 

## <a name="example"></a>Exemplo

Veja a seguir um exemplo de predicado **All bit a bit** .


```sql
Select system.itemnamedisplay, system.FileAttributes from SystemIndex Where System.FileAttributes <> ALL BITWISE 0x4 AND Scope = 'file:c:\bitwise'
                
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados de texto não completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



