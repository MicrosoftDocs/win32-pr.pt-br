---
description: O provedor SNMP usa os qualificadores de propriedade CIM a seguir ao mapear definições de objeto MIB para definições de classe CIM.
ms.assetid: 6e858e7e-5c46-4350-9696-c5efa1252c00
ms.tgt_platform: multiple
title: Qualificadores de propriedade CIM para objetos MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2fd45f250b603fcea97040a35faf43f6343311094e97a52ca06823e99bfcac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131708"
---
# <a name="cim-property-qualifiers-for-mib-objects"></a>Qualificadores de propriedade CIM para objetos MIB

O provedor SNMP usa os qualificadores de propriedade CIM a seguir ao mapear definições de objeto MIB para definições de classe CIM. Um qualificador obrigatório deve estar presente para que o Provedor SNMP resolva totalmente um objeto MIB. Falha ao definir um qualificador obrigatório retorna um erro. Especificar um valor de qualificador ilegal também retorna um erro.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 



| Qualificador                          | Descrição                                                                                                                                                                                            |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bits**                           | **cadeia de caracteres** Obrigatório, se o **qualificador de \_ Convenção Textual** não for igual a BITS.<br/> Valores enumerados para a definição de subtipo de um bit.<br/>                                        |
| **Cimtype**                        | **cadeia de caracteres** Obrigatório<br/> Representação textual CIM que formatar um valor de protocolo CIM subjacente.<br/>                                                                                    |
| **Defval**                         | **cadeia de caracteres** Opcional<br/> O valor padrão do objeto.<br/>                                                                                                                                       |
| **Descrição**                    | **cadeia de caracteres** Opcional<br/> Descrição do objeto.<br/>                                                                                                                                    |
| **Dica de \_ exibição**                  | **cadeia de caracteres** Opcional<br/> Maneira na qual os dados do objeto devem aparecer para um usuário.<br/>                                                                                                    |
| **Codificação**                       | **cadeia de caracteres** Opcional<br/> Tipo SNMP usado ao codificar quadros de protocolo SNMPv1 e SNMPv2C.<br/>                                                                                              |
| **Enumeração**                    | **cadeia de caracteres** Obrigatório, se o **qualificador de \_ Convenção Textual** não for igual a ENUMERATEDINTEGER.<br/> Valores enumerados para uma definição de subtipo inteiro enumerado.<br/>                  |
| **Comprimento \_ Fixo**                  | **uint32** Opcional<br/> Valor de comprimento fixo.<br/>                                                                                                                                           |
| [**Chave**](standard-qualifiers.md) | **Bool** Opcional<br/> Propriedade de chave de uma definição de classe.<br/>                                                                                                                             |
| **Ordem de \_ chave**                     | **uint32** Opcional, a [**menos que Key**](standard-qualifiers.md) seja especificado.<br/> Ordem da propriedade de chave na definição de classe.<br/>                                                   |
| **Nome**                           | **cadeia de caracteres** Obrigatório<br/> Nome implícito da propriedade. Observe que esse qualificador não está definido explicitamente.<br/>                                                                           |
| **Identificador \_ de Objeto**             | **cadeia de caracteres** Obrigatório<br/> Identificador de objeto MIB do objeto.<br/>                                                                                                                              |
| **Sintaxe do \_ objeto**                 | **cadeia de caracteres** Opcional<br/> Definição de tipo nomeado do objeto.<br/>                                                                                                                               |
| **Ler**                           | **Bool** Opcional (pelo menos um de **Leitura** **ou Gravação** deve ser especificado)<br/> Concede acesso de leitura ao objeto .<br/>                                                                     |
| **Referência**                      | **cadeia de caracteres** Opcional<br/> Refere-se a outro documento que contém mais informações sobre o objeto .<br/>                                                                                   |
| **Status**                         | **cadeia de caracteres** Opcional<br/> Indica se o objeto deve ter suporte.<br/>                                                                                                               |
| **Convenção \_ textual**            | **cadeia de caracteres** Obrigatório<br/> Representação textual da cláusula SYNTAX da macro MIB [OBJECT-TYPE.](object-type-macro.md)<br/>                                                           |
| **Unidades**                          | **cadeia de caracteres** Opcional<br/> Definição precisa do que o objeto representa.<br/>                                                                                                             |
| **Comprimento \_ variável**               | **cadeia de caracteres** Opcional<br/> Valores mínimo, máximo e de comprimento fixo associados à definição de tipo do objeto.<br/>                                                                       |
| **Valor da \_ variável**                | **cadeia de caracteres** Opcional<br/> Valores fixos e ranged associados à definição de tipo do objeto.<br/>                                                                                         |
| **Chave \_ virtual**                   | **Bool** Opcional<br/> Indica que o valor da propriedade deve ser baseado no superconjunto de informações de instância associadas a todos os objetos MIB acessíveis na definição de classe.<br/> |
| **Gravar**                          | **Bool** Opcional (pelo menos um de **Leitura** **ou Gravação** deve ser especificado)<br/> Concede acesso de gravação ao objeto .<br/>                                                                    |



 

 

 




