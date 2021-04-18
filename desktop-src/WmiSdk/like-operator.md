---
description: O operador LIKE determina se uma cadeia de caracteres corresponde ou não a um padrão especificado.
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: Operador LIKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9091f44dd131d5d2c30d2d46aa4fc109dcdf02b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807200"
---
# <a name="like-operator"></a>Operador LIKE

O operador LIKE determina se uma cadeia de caracteres corresponde ou não a um padrão especificado. O padrão especificado pode conter exatamente os caracteres a serem correspondidos ou pode conter caracteres meta. Na verdade, o operador LIKE corresponde a subcadeias usando os caracteres curinga na tabela a seguir.



| Caractere       | Descrição                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[ \]           | Qualquer caractere dentro do intervalo especificado ( \[ a-f \] ) ou conjunto ( \[ abcdef \] ).                                                                                                                 |
| ^               | Qualquer caractere que não esteja dentro do intervalo ( \[ ^ a-f \] ) ou definido ( \[ ^ abcdef \] .)                                                                                                                     |
| %               | Qualquer cadeia de caracteres igual a 0 (zero) ou mais. O exemplo a seguir localiza todas as instâncias em que "win" é encontrado em qualquer lugar no nome da classe: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"` |
| \_ sublinhado | Qualquer caractere. Qualquer sublinhado literal usado na cadeia de caracteres de consulta deve ser ignorado colocando-o dentro \[ \] (colchetes).                                                             |



 

Por exemplo, o código de PowerShell a seguir recupera todas as instâncias da classe de **\_ OperatingSystem do Win32** cuja propriedade **Name** começa com **FirstName**:

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

Como o sublinhado é um caractere de meta, se o destino da consulta tiver um sublinhado, os \[ \] caracteres de escape deverão colocá-lo. Por exemplo, você pode consultar todas as classes que têm um sublinhado duplo no nome.

Para localizar todas as classes com um sublinhado duplo no nome, você deve escapar os dois sublinhados com \[ \] (colchetes), por exemplo:

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

Você pode negar uma instrução LIKE usando NOT; para fazer isso, certifique-se de inserir o não diretamente na frente do nome do campo. Por exemplo:

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Operadores WQL](wql-operators.md)
</dt> </dl>

 

 



