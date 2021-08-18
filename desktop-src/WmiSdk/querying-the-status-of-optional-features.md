---
description: No Windows 7, o WMI implementou a classe \_ OptionalFeature do Win32. Essa classe recupera o status dos recursos opcionais que estão presentes em um computador.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Consultando o status de recursos opcionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec27457336adcc5c358aad0a5e139c1c7c07f6bcb72335ec549f9ca98cc1e5a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996026"
---
# <a name="querying-the-status-of-optional-features"></a>Consultando o status de recursos opcionais

No Windows 7, o WMI implementou a [**classe \_ OptionalFeature do Win32.**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) Essa classe recupera o status dos recursos opcionais que estão presentes em um computador.

Você pode usar Windows PowerShell cmdlets para consultar o status dos recursos opcionais. Todos os exemplos neste tópico usam o cmdlet Get-WmiObject. Para obter mais informações, [consulte Get-WmiObject](/previous-versions//dd315295(v=technet.10)).

**Para recuperar todas as instâncias de recursos opcionais presentes em um computador**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject Win32_OptionalFeature</code></pre></td>
    </tr>
    </tbody>
    </table>

    

**Para consultar um recurso opcional especificando o nome do recurso**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from Win32_OptionalFeature where name = &#39;TelnetClient&#39;&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    > [!Note]  
    > A **propriedade name** é sensível a minúsculas.

     

**Para consultar recursos opcionais especificando o estado de instalação**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from win32_optionalfeature where installstate= 1&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    Para obter mais informações sobre os valores possíveis para a **propriedade InstallState,** consulte [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
