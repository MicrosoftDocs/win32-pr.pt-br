---
description: O provedor SNMP usa os seguintes qualificadores de classe CIM ao mapear definições de objeto MIB para definições de classe CIM.
ms.assetid: 458167dc-562e-47b8-8760-797ae13f9459
ms.tgt_platform: multiple
title: Qualificadores de classe CIM para objetos MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60fe97debc7fd81b48a6daf0f5a955374546458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171235"
---
# <a name="cim-class-qualifiers-for-mib-objects"></a>Qualificadores de classe CIM para objetos MIB

O provedor SNMP usa os seguintes qualificadores de classe CIM ao mapear definições de objeto MIB para definições de classe CIM. Um qualificador obrigatório deve estar presente para que o provedor SNMP resolva completamente um objeto de grupo. Falha ao definir um qualificador obrigatório retorna um erro. A especificação de um valor de qualificador inválido também retorna um erro.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 



| Qualificador           | Descrição                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Descrição**     | **cadeia de caracteres** Adicional<br/> Descrição da classe.<br/>                                                                      |
| **ObjectID do grupo \_** | **cadeia de caracteres** Obrigatório, se a classe for para o provedor de classe SNMP.<br/> Identificador de objeto da coleção criei.<br/> |
| **Importações de módulo \_** | **cadeia de caracteres** Adicional<br/> Lista separada por vírgulas de nomes de módulo MIB usados para resolver importações.<br/>                              |
| **Nome do módulo \_**    | **cadeia de caracteres** Adicional<br/> Nome da identidade de um módulo MIB.<br/>                                                                 |
| **Referência**       | **cadeia de caracteres** Adicional<br/> Refere-se a outro documento que contém mais informações sobre a classe.<br/>                     |
| **Único**       | **Bool** Obrigatório para classes mapeadas de coleções escalares.<br/> Indica uma classe que só pode ter uma instância.<br/>  |



 

 

 




