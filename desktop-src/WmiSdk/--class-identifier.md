---
description: A classe de identificador bem conhecida \_ \_ refere-se a uma pseudo propriedade em cada objeto WMI que indica a classe do objeto atual.
ms.assetid: a1d0e934-c5b5-4554-9d6e-3881064419ca
ms.tgt_platform: multiple
title: Identificador de __CLASS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b4db6cacb6943619cf6468cf7f03d4a4c08278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091684"
---
# <a name="__class-identifier"></a>\_\_Identificador de classe

A classe de identificador bem conhecida \_ \_ refere-se a uma pseudo propriedade em cada objeto WMI que indica a classe do objeto atual.

Use a \_ \_ classe em uma cláusula [Where](where-clause.md) para filtrar quaisquer objetos de classes derivadas do seu conjunto de resultados. Por exemplo, o conjunto de resultados da consulta a seguir contém não apenas objetos cuja classe é o [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), mas também objetos cuja classe é derivada do **\_ LogicalDisk do Win32**.


```sql
SELECT * FROM Win32_LogicalDisk
```



No exemplo a seguir, o uso da \_ \_ classe na cláusula **Where** filtra todos os objetos das classes derivadas do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) porque sua classe não é o disco **\_ lógico do Win32**.


```sql
SELECT * FROM Win32_LogicalDisk   WHERE __CLASS = "Win32_LogicalDisk"
```



Use \_ \_ a classe em provedores que são solicitados a fornecer instâncias de uma classe específica, independentemente de quaisquer subclasses.

 

 
