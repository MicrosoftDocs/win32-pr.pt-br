---
description: O operador LIKE determina se uma cadeia de caracteres corresponde ou não a um padrão especificado.
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: Operador LIKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e5df500091fac8b15bcdcb448b7a97fc00dc62807ba854757e447f07e6f4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317865"
---
# <a name="like-operator"></a>Operador LIKE

O operador LIKE determina se uma cadeia de caracteres corresponde ou não a um padrão especificado. O padrão especificado pode conter exatamente os caracteres a corresponder ou pode conter metadados. Na verdade, o operador LIKE corresponde a substrings usando os caracteres curinga na tabela a seguir.



| Caractere       | Descrição                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[ \]           | Qualquer caractere dentro do intervalo especificado ( \[ a-f \] ) ou set ( \[ abcdef \] ).                                                                                                                 |
| ^               | Qualquer caractere que não está dentro do intervalo ( \[ ^a-f \] ) ou definido ( \[ ^abcdef \] .)                                                                                                                     |
| %               | Qualquer cadeia de caracteres de 0 (zero) ou mais caracteres. O exemplo a seguir localiza todas as instâncias em que "Win" é encontrado em qualquer lugar no nome da classe: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"` |
| \_ (sublinhado) | Qualquer caractere. Qualquer sublinhado literal usado na cadeia de caracteres de consulta deve ser escapado colocando-o dentro \[ \] (colchetes).                                                             |



 

Por exemplo, o código do Power Shell a seguir recupera todas as instâncias da classe **\_ operatingSystem Win32** cuja propriedade **Name** começa com **FirstName**:

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

Como o sublinhado é um caractere meta, se o destino da consulta tiver um sublinhado, os \[ \] caracteres de escape " deverão envelhá-lo. Por exemplo, você pode consultar todas as classes que têm um sublinhado duplo no nome.

Para localizar todas as classes com um sublinhado duplo no nome, você deve escapar ambos os sublinhados com \[ \] (colchetes), por exemplo:

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

Você pode negar uma instrução LIKE usando NOT; para fazer isso, coloque NOT diretamente na frente do nome do campo. Por exemplo:

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Operadores WQL](wql-operators.md)
</dt> </dl>

 

 



