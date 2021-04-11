---
description: O WMI tem vários tipos de qualificadores de classe e de propriedade. Os qualificadores também podem ter tipos de modificação.
ms.assetid: b889df69-327b-40d0-bbd7-a33d7924f3e1
ms.tgt_platform: multiple
title: Qualificadores WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b14dc8f1f73571fc2c449e55c30034f86c2453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165182"
---
# <a name="wmi-qualifiers"></a>Qualificadores WMI

O WMI tem vários tipos de [*qualificadores*](gloss-q.md)de classe e de propriedade. Os qualificadores também podem ter [*tipos*](gloss-f.md)de modificação. Os seguintes tipos de qualificadores e versões são usados no WMI.

O nome de cada qualificador é exibido com seu tipo de dados e um indicador de se o qualificador pode ser aplicado a uma classe, instância, propriedade ou método. Para qualificadores como a **Associação** (discutida em [meta Qualifiers](meta-qualifiers.md)), há uma regra de uso implícita que o meta Qualifier também deve estar presente. Por exemplo, a regra de uso implícito para os qualificadores de **agregação** é que o qualificador de **Associação** também deve estar presente.



| Tipo de qualificador                              | Descrição                                                                                                                           |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Volume](meta-qualifiers.md)                 | Restringe a definição de metaconstruções esclarecendo o uso real de uma classe ou declaração de propriedade.                          |
| [Opcional](optional-qualifiers.md)         | As situações de endereços não são comuns a todas as implementações em conformidade com o CIM.                                                                 |
| [Tipos de qualificadores](qualifier-flavors.md)  | Fornece mais informações sobre um qualificador, como se uma classe ou instância derivada pode substituir o valor original do qualificador. |
| [Standard](standard-qualifiers.md)         | Dá suporte às descrições que todas as implementações compatíveis com CIM devem manipular.                                                         |
| [Específico do WMI](wmi-specific-qualifiers.md) | Descreve os qualificadores específicos ao WMI, como qualificadores de classe de contador de desempenho.                                                   |



 

Para obter mais informações sobre como aplicar qualificadores a suas classes WMI, consulte [adicionando um qualificador](adding-a-qualifier.md). Para ver como examinar qualificadores em classes WMI existentes, consulte o código de exemplo abaixo.

## <a name="example"></a>Exemplo

O código do PowerShell a seguir, extraído da [Galeria do TechNet](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7), descreve como recuperar qualificadores de uma classe WMI.


```PowerShell
Function Get-WMIClassesWithQualifiers 
{ 
 Param([string]$qualifier = "dynamic", 
  [string]$namespace = "root\cimv2") 
 $classes = Gwmi -list -namespace $namespace 
 foreach($class in $classes) 
 { 
  $query = "select * from meta_class where __this isa ""$($class.name)"" " 
  $a = gwmi -Query $query -Namespace $namespace |  
  select -Property __class, qualifiers 
   if($a.qualifiers | % { $_ | ? { $_.name -match "$qualifier" }}) 
    { $a.__class } 
  } #end foreach $class 
} 
```



 

 



