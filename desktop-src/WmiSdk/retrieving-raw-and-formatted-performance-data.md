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
# <a name="retrieving-documentation-for-raw-and-formatted-performance-data-objects"></a><span data-ttu-id="fa5f5-103">Recuperando a documentação para objetos de dados de desempenho brutos e formatados</span><span class="sxs-lookup"><span data-stu-id="fa5f5-103">Retrieving Documentation for Raw and Formatted Performance Data Objects</span></span>

<span data-ttu-id="fa5f5-104">O tópico a seguir descreve como recuperar a documentação de programação online para um objeto de dados brutos ou formatados criado dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="fa5f5-104">The following topic describes how to retrieve the on-line programming documentation for a dynamically-created raw or formatted data object.</span></span>

<span data-ttu-id="fa5f5-105">O WMI contém vários objetos que acompanham o desempenho.</span><span class="sxs-lookup"><span data-stu-id="fa5f5-105">WMI contains a number of objects that track performance.</span></span> <span data-ttu-id="fa5f5-106">As classes derivadas do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) contêm dados de desempenho brutos ou "não-cookied" e têm suporte do [provedor de contador de desempenho](performance-counter-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fa5f5-106">Classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) contain raw, or "uncooked" performance data, and are supported by the [Performance Counter provider](performance-counter-provider.md).</span></span> <span data-ttu-id="fa5f5-107">Por outro lado, as classes derivadas do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contêm "cooked", ou dados formatados, e têm suporte pelo [provedor de dados de desempenho formatado](formatted-performance-data-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fa5f5-107">In contrast, classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contain "cooked", or formatted data, and are supported by the [Formatted Performance Data Provider](formatted-performance-data-provider.md).</span></span>

<span data-ttu-id="fa5f5-108">No entanto, ambos os provedores dão suporte a um número de classes filho criadas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="fa5f5-108">However, both providers support a number of dynamically-created child classes.</span></span> <span data-ttu-id="fa5f5-109">Como as propriedades são adicionadas em tempo de execução, essas classes podem conter Propriedades não documentadas.</span><span class="sxs-lookup"><span data-stu-id="fa5f5-109">Because the properties are added at run-time, these classes may contain undocumented properties.</span></span> <span data-ttu-id="fa5f5-110">Você pode usar o código a seguir para identificar quais propriedades uma determinada classe criada dinamicamente tem.</span><span class="sxs-lookup"><span data-stu-id="fa5f5-110">You can use the following code to identify what properties a given dynamically-created class has.</span></span>

<span data-ttu-id="fa5f5-111">**Para recuperar uma descrição de uma classe criada dinamicamente**</span><span class="sxs-lookup"><span data-stu-id="fa5f5-111">**To retrieve a description of a dynamically-created class**</span></span>

1.  <span data-ttu-id="fa5f5-112">Crie uma instância do item e defina o qualificador corrigido como true.</span><span class="sxs-lookup"><span data-stu-id="fa5f5-112">Create an instance of the item, and set the amended qualifier to true.</span></span>

    ```PowerShell
    $osClass = New-Object System.Management.ManagementClass Win32_ClassNameHere  
    $osClass.Options.UseAmendedQualifiers = $true
    ```

    

2.  <span data-ttu-id="fa5f5-113">Recupere as propriedades da classe.</span><span class="sxs-lookup"><span data-stu-id="fa5f5-113">Retrieve the properties of the class.</span></span>

    ```PowerShell
    $properties = $osClass.Properties  
    "This class has {0} properties as follows:" -f $properties.count
    ```

    

3.  <span data-ttu-id="fa5f5-114">Exiba as propriedades.</span><span class="sxs-lookup"><span data-stu-id="fa5f5-114">Display the properties.</span></span>

    ```PowerShell
    foreach ($property in $properties) {  
    "Property Name: {0}" -f $property.Name  
    "Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
    "Type:          {0}" -f $property.Type  
    "-------"
    }
    ```

    

<span data-ttu-id="fa5f5-115">O código a seguir recupera as descrições de propriedade para o objeto [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) especificado.</span><span class="sxs-lookup"><span data-stu-id="fa5f5-115">The following code retrieves the property descriptions for the specified [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) object.</span></span>


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



 

 
