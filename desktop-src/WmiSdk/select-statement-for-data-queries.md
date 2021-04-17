---
description: Descreva a instrução SELECT para uma consulta de dados.
ms.assetid: 9c1a164e-4728-4fbe-8a49-b571005a46ec
ms.tgt_platform: multiple
title: Instrução SELECT para consultas de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06905cfd9ef5e55022b3fc2275ed705a670a0ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763092"
---
# <a name="select-statement-for-data-queries"></a>Instrução SELECT para consultas de dados

Você pode usar uma variedade de instruções SELECT para consultar informações. As instruções podem ser instruções básicas ou podem ser mais restritivas para restringir o conjunto de resultados retornado pela consulta.

O exemplo a seguir é uma instrução SELECT básica que é usada para consultar dados.


```sql
SELECT * FROM Class
```



Essa instrução retorna instâncias da classe especificada e de qualquer uma de suas subclasses. Todas as propriedades do sistema e definidas pelo usuário para as classes são incluídas. Se uma propriedade do sistema não for relevante para uma consulta específica, ela conterá **NULL**.

Você pode usar várias técnicas para reduzir a largura de banda necessária para recuperar o conjunto de resultados, se a execução da consulta resultar em muita sobrecarga e o usuário estiver interessado apenas em um subconjunto das propriedades. Primeiro, as consultas podem substituir o asterisco pelas propriedades desejadas.

O exemplo a seguir mostra como consultar propriedades específicas.


```sql
SELECT property_1, property_2, property_3 FROM class
```



O conjunto de resultados inclui todas as propriedades do sistema e as propriedades não do sistema especificadas.

Outra técnica para restringir o escopo do conjunto de resultados de uma consulta é usar a propriedade do sistema de [**\_ \_ classe**](wmi-system-properties.md) . Por padrão, as consultas retornam todas as instâncias da classe especificada e suas subclasses. Você pode usar a propriedade do sistema de **\_ \_ classe** para solicitar apenas instâncias da classe especificada, excluindo suas subclasses.

O exemplo a seguir mostra como usar a propriedade do sistema de [**\_ \_ classe**](wmi-system-properties.md) em uma cláusula WHERE.


```sql
SELECT * FROM Device WHERE __CLASS = "Device"
```



Você também pode usar a propriedade do sistema de [**\_ \_ classe**](wmi-system-properties.md) para restringir o conjunto de resultados a instâncias de subclasses específicas.

O exemplo a seguir mostra como restringir o conjunto de resultados para instâncias de subclasses específicas.


```sql
SELECT * FROM Device WHERE __CLASS = "Modem" OR __CLASS = "Keyboard"
```



> [!Note]  
> Se você construir uma consulta com um caminho inválido para um objeto inserido, sua consulta não retornará um erro ou nenhum resultado.

 

O exemplo a seguir retorna uma instância de **MainClass**, supondo que uma instância de **MainClass** exista contendo o objeto inserido **EmbedObj** com uma propriedade **P \_ UInt32** igual a "70011".


```sql
SELECT * FROM MainClass WHERE EmbedObj.P_Uint32 = 70011
```



O exemplo a seguir não retorna nenhum resultado e não retorna um erro, supondo que o objeto inserido **EmbedObj** na instância de **MainClass** não tenha uma propriedade **inválida**.


```sql
SELECT * FROM MainClass WHERE StrongEmbedObj.INVALID = 70011
```



 

 



