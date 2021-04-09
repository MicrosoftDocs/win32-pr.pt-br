---
description: O provedor SNMP usa os seguintes qualificadores de propriedade CIM ao mapear definições de objeto MIB para definições de classe CIM.
ms.assetid: 6e858e7e-5c46-4350-9696-c5efa1252c00
ms.tgt_platform: multiple
title: Qualificadores de propriedade CIM para objetos MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f2a25edf9c15930202d3c8cf79d3d62b0d1dd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171231"
---
# <a name="cim-property-qualifiers-for-mib-objects"></a>Qualificadores de propriedade CIM para objetos MIB

O provedor SNMP usa os seguintes qualificadores de propriedade CIM ao mapear definições de objeto MIB para definições de classe CIM. Um qualificador obrigatório deve estar presente para que o provedor SNMP resolva completamente um objeto MIB. Falha ao definir um qualificador obrigatório retorna um erro. A especificação de um valor de qualificador inválido também retorna um erro.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 



| Qualificador                          | Descrição                                                                                                                                                                                            |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bits**                           | **cadeia de caracteres** Obrigatório, se o qualificador de **\_ Convenção textual** não for igual a bits.<br/> Valores enumerados para a definição de subtipo de um bit.<br/>                                        |
| **CimType**                        | **cadeia de caracteres** Obrigatório<br/> Representação textual de CIM que formata um valor de protocolo CIM subjacente.<br/>                                                                                    |
| **Defval**                         | **cadeia de caracteres** Adicional<br/> Valor padrão do objeto.<br/>                                                                                                                                       |
| **Descrição**                    | **cadeia de caracteres** Adicional<br/> Descrição do objeto.<br/>                                                                                                                                    |
| **Exibir \_ dica**                  | **cadeia de caracteres** Adicional<br/> Maneira na qual os dados do objeto devem aparecer para um usuário.<br/>                                                                                                    |
| **Codificação**                       | **cadeia de caracteres** Adicional<br/> Tipo de SNMP usado ao codificar quadros de protocolo SNMPv1 e SNMPv2C.<br/>                                                                                              |
| **Enumeração**                    | **cadeia de caracteres** Obrigatório, se o qualificador de **\_ Convenção textual** não for igual a ENUMERATEDINTEGER.<br/> Valores enumerados para uma definição de subtipo de inteiro enumerado.<br/>                  |
| **\_Comprimento fixo**                  | **UInt32** Adicional<br/> Valor de comprimento fixo.<br/>                                                                                                                                           |
| [**Chave**](standard-qualifiers.md) | **Bool** Adicional<br/> Propriedade de chave de uma definição de classe.<br/>                                                                                                                             |
| **Ordem de chave \_**                     | **UInt32** Opcional, a menos que a [**chave**](standard-qualifiers.md) seja especificada.<br/> Ordem da propriedade de chave na definição de classe.<br/>                                                   |
| **Nome**                           | **cadeia de caracteres** Obrigatório<br/> Nome implícito da propriedade. Observe que esse qualificador não está definido explicitamente.<br/>                                                                           |
| **Identificador de objeto \_**             | **cadeia de caracteres** Obrigatório<br/> Identificador de objeto MIB do objeto.<br/>                                                                                                                              |
| **Sintaxe de objeto \_**                 | **cadeia de caracteres** Adicional<br/> Definição de tipo nomeado do objeto.<br/>                                                                                                                               |
| **Ler**                           | **Bool** Opcional (pelo menos um de **leitura** ou **gravação** deve ser especificado)<br/> Concede acesso de leitura ao objeto.<br/>                                                                     |
| **Referência**                      | **cadeia de caracteres** Adicional<br/> Refere-se a outro documento que contém mais informações sobre o objeto.<br/>                                                                                   |
| **Status**                         | **cadeia de caracteres** Adicional<br/> Indica se o objeto deve ter suporte.<br/>                                                                                                               |
| **\_Convenção textual**            | **cadeia de caracteres** Obrigatório<br/> Representação textual da cláusula de sintaxe da macro do [tipo de objeto](object-type-macro.md) MIB.<br/>                                                           |
| **Unidades**                          | **cadeia de caracteres** Adicional<br/> Definição precisa do que o objeto representa.<br/>                                                                                                             |
| **\_Comprimento variável**               | **cadeia de caracteres** Adicional<br/> Valores mínimo, máximo e de comprimento fixo associados à definição de tipo do objeto.<br/>                                                                       |
| **Valor da variável \_**                | **cadeia de caracteres** Adicional<br/> Valores de intervalo e fixos associados à definição de tipo do objeto.<br/>                                                                                         |
| **\_Chave virtual**                   | **Bool** Adicional<br/> Indica que o valor da propriedade deve ser baseado no superconjunto de informações de instância associado a todos os objetos MIB acessíveis na definição de classe.<br/> |
| **Gravar**                          | **Bool** Opcional (pelo menos um de **leitura** ou **gravação** deve ser especificado)<br/> Concede acesso de gravação ao objeto.<br/>                                                                    |



 

 

 




