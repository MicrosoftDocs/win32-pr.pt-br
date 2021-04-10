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
# <a name="__class-identifier"></a><span data-ttu-id="40257-103">\_\_Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="40257-103">\_\_CLASS Identifier</span></span>

<span data-ttu-id="40257-104">A classe de identificador bem conhecida \_ \_ refere-se a uma pseudo propriedade em cada objeto WMI que indica a classe do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="40257-104">The well-known identifier \_\_CLASS refers to a pseudo-property on every WMI object that indicates the class of the current object.</span></span>

<span data-ttu-id="40257-105">Use a \_ \_ classe em uma cláusula [Where](where-clause.md) para filtrar quaisquer objetos de classes derivadas do seu conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="40257-105">Use \_\_CLASS in a [WHERE](where-clause.md) clause to filter out any objects of derived classes from your result set.</span></span> <span data-ttu-id="40257-106">Por exemplo, o conjunto de resultados da consulta a seguir contém não apenas objetos cuja classe é o [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), mas também objetos cuja classe é derivada do **\_ LogicalDisk do Win32**.</span><span class="sxs-lookup"><span data-stu-id="40257-106">For example, the result set of the following query contains not only objects whose class is [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), but also objects whose class is derived from **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM Win32_LogicalDisk
```



<span data-ttu-id="40257-107">No exemplo a seguir, o uso da \_ \_ classe na cláusula **Where** filtra todos os objetos das classes derivadas do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) porque sua classe não é o disco **\_ lógico do Win32**.</span><span class="sxs-lookup"><span data-stu-id="40257-107">In the following example, the use of \_\_CLASS in the **WHERE** clause filters out all objects of classes derived from [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) because their class is not **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM Win32_LogicalDisk   WHERE __CLASS = "Win32_LogicalDisk"
```



<span data-ttu-id="40257-108">Use \_ \_ a classe em provedores que são solicitados a fornecer instâncias de uma classe específica, independentemente de quaisquer subclasses.</span><span class="sxs-lookup"><span data-stu-id="40257-108">Use \_\_CLASS in providers that are asked to provide instances of a specific class, irrespective of any subclasses.</span></span>

 

 
