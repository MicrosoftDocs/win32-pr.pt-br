---
description: no Windows 7, o WMI implementou a \_ classe Win32 OptionalFeature. Essa classe recupera o status dos recursos opcionais que estão presentes em um computador.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Consultando o status de recursos opcionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecffe6ddbe9b860c6f49fe12d3fed500c169bef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476702"
---
# <a name="querying-the-status-of-optional-features"></a>Consultando o status de recursos opcionais

no Windows 7, o WMI implementou a classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Essa classe recupera o status dos recursos opcionais que estão presentes em um computador.

você pode usar Windows PowerShell cmdlets para consultar o status dos recursos opcionais. Todos os exemplos neste tópico usam o cmdlet Get-WmiObject. Para obter mais informações, consulte [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).

**Para recuperar todas as instâncias de recursos opcionais presentes em um computador**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject Win32_OptionalFeature</code></pre> | 


    

**Para consultar um recurso opcional especificando o nome do recurso**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject -query "select * from Win32_OptionalFeature where name = 'TelnetClient'"</code></pre> | 


    

    > [!Note]  
    > The **name** property is case-sensitive.

     

**Para consultar recursos opcionais especificando o estado de instalação**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject -query "select * from win32_optionalfeature where installstate= 1"</code></pre> | 


    

    For more information about the possible values for the **InstallState** property, see [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_OptionalFeature Win32**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
