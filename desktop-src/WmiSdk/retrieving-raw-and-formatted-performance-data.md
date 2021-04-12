---
description: O tópico a seguir descreve como recuperar a documentação de programação online para um objeto de dados brutos ou formatados criado dinamicamente.
ms.assetid: B3CD7E2C-9FCF-42FB-8713-01A696E905B0
ms.tgt_platform: multiple
title: Recuperando a documentação para objetos de dados de desempenho brutos e formatados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ab9cf66aa4536da25102511fdcbcab6bdd5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297497"
---
# <a name="retrieving-documentation-for-raw-and-formatted-performance-data-objects"></a>Recuperando a documentação para objetos de dados de desempenho brutos e formatados

O tópico a seguir descreve como recuperar a documentação de programação online para um objeto de dados brutos ou formatados criado dinamicamente.

O WMI contém vários objetos que acompanham o desempenho. As classes derivadas do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) contêm dados de desempenho brutos ou "não-cookied" e têm suporte do [provedor de contador de desempenho](performance-counter-provider.md). Por outro lado, as classes derivadas do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contêm "cooked", ou dados formatados, e têm suporte pelo [provedor de dados de desempenho formatado](formatted-performance-data-provider.md).

No entanto, ambos os provedores dão suporte a um número de classes filho criadas dinamicamente. Como as propriedades são adicionadas em tempo de execução, essas classes podem conter Propriedades não documentadas. Você pode usar o código a seguir para identificar quais propriedades uma determinada classe criada dinamicamente tem.

**Para recuperar uma descrição de uma classe criada dinamicamente**

1.  Crie uma instância do item e defina o qualificador corrigido como true.

    ```PowerShell
    $osClass = New-Object System.Management.ManagementClass Win32_ClassNameHere  
    $osClass.Options.UseAmendedQualifiers = $true
    ```

    

2.  Recupere as propriedades da classe.

    ```PowerShell
    $properties = $osClass.Properties  
    "This class has {0} properties as follows:" -f $properties.count
    ```

    

3.  Exiba as propriedades.

    ```PowerShell
    foreach ($property in $properties) {  
    "Property Name: {0}" -f $property.Name  
    "Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
    "Type:          {0}" -f $property.Type  
    "-------"
    }
    ```

    

O código a seguir recupera as descrições de propriedade para o objeto [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) especificado.


```PowerShell
$osClass = New-Object System.Management.ManagementClass Win32_PerfFormattedData_APPPOOLCountersProvider_APPPOOLWAS  
$osClass.Options.UseAmendedQualifiers = $true  
  
# Get the Properties in the class  
$properties = $osClass.Properties  
"This class has {0} properties as follows:" -f $properties.count  
  
  
# display the Property name, description, type, qualifiers and instance values  
  
foreach ($property in $properties) {  
"Property Name: {0}" -f $property.Name  
"Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
"Type:          {0}" -f $property.Type  
"-------"  
}
```



 

 
