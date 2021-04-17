---
description: O WMI define um conjunto de propriedades do sistema que estão associadas a todas as classes e instâncias de classes, além de propriedades específicas de classe.
ms.assetid: ea8ca4e4-9969-48fc-9b9f-5a5c8442006d
ms.tgt_platform: multiple
title: Propriedades do sistema CIM para objetos MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0425afecc399c3cd1399e8bf565908b1c7c5d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780305"
---
# <a name="cim-system-properties-for-mib-objects"></a>Propriedades do sistema CIM para objetos MIB

O WMI define um conjunto de propriedades do sistema que estão associadas a todas as classes e instâncias de classes, além de propriedades específicas de classe.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

O provedor SNMP usa as seguintes propriedades do sistema CIM ao mapear definições de objeto MIB para definições de classe CIM. As propriedades obrigatórias devem estar presentes para que o provedor SNMP resolva completamente um objeto de grupo. Falha ao definir uma propriedade obrigatória retorna um erro.



<table>
<thead>
<tr class="header">
<th>Propriedade</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>__CLASS</strong></td>
<td><strong>cadeia de caracteres</strong> Obrigatório<br/> Para instâncias, a classe à qual o objeto pertence. Para classes, esse é o nome da classe.<br/></td>
</tr>
<tr class="even">
<td><strong>__DYNASTY</strong></td>
<td><strong>cadeia de caracteres</strong> Adicional<br/> Nome da classe que é a classe base definitiva para o objeto atual (não sua classe pai imediata).<br/></td>
</tr>
<tr class="odd">
<td><strong>__GENUS</strong></td>
<td><strong>UInt32</strong> Obrigatório<br/> Tipo de objeto. Os valores são:<br/> <dl> 1 = classe<br />
2 = instância<br />
</dl></td>
</tr>
<tr class="even">
<td><strong>__NAMESPACE</strong></td>
<td><strong>cadeia de caracteres</strong> Obrigatório<br/> Namespace onde o objeto está localizado.<br/></td>
</tr>
<tr class="odd">
<td><strong>__PATH</strong></td>
<td><strong>cadeia de caracteres</strong> Obrigatório<br/> Caminho absoluto para o objeto.<br/></td>
</tr>
<tr class="even">
<td><strong>__PROPERTYCOUNT</strong></td>
<td><strong>UInt32</strong> Obrigatório<br/> Número de propriedades que não são do sistema definidas para o objeto.<br/></td>
</tr>
<tr class="odd">
<td><strong>__RELPATH</strong></td>
<td><strong>cadeia de caracteres</strong> Obrigatório<br/> Caminho relativo para o objeto.<br/></td>
</tr>
<tr class="even">
<td><strong>__SERVER</strong></td>
<td><strong>cadeia de caracteres</strong> Obrigatório<br/> Servidor fornecendo o objeto.<br/></td>
</tr>
<tr class="odd">
<td><strong>__SUPERCLASS</strong></td>
<td><strong>cadeia de caracteres</strong> Adicional<br/> Classe pai imediata do objeto.<br/></td>
</tr>
</tbody>
</table>



 

 

 




