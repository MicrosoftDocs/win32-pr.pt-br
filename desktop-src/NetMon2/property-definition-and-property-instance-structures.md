---
description: Monitor de Rede fornece uma estrutura PROPERTYINFO para definir as propriedades de um protocolo, e uma estrutura PROPERTYINST e PROPERTYINSTEX para definir uma instância de uma propriedade.
ms.assetid: d1e29bd6-c04a-48f1-9727-96b9450e256f
title: Definição de propriedade e estruturas de instância de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8289c16bf501d36936b1aba6f292787e1b9a41babdb1225d3c0d53885c0ba31a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676806"
---
# <a name="property-definition-and-property-instance-structures"></a>Definição de propriedade e estruturas de instância de propriedade

Monitor de Rede fornece uma estrutura [**PROPERTYINFO**](propertyinfo.md) para definir as propriedades de um protocolo, e uma estrutura [**PROPERTYINST**](propertyinst.md)e [**PROPERTYINSTEX**](propertyinstex.md) para definir uma instância de uma propriedade.

![estruturas do monitor de rede](images/property1.png)

O analisador aloca e preenche a estrutura [**PROPERTYINFO**](propertyinfo.md) para todas as propriedades às quais um protocolo dá suporte. O analisador passa a estrutura para Monitor de Rede onde a estrutura é adicionada ao banco de [*dados de propriedades*](p.md)de protocolo. As informações na estrutura **PROPERTYINFO** são usadas ao analisar uma instância de uma propriedade e ao formatar os dados exibidos na interface do usuário do monitor de rede.

Monitor de Rede aloca as estruturas [**PROPERTYINST**](propertyinst.md) e [**PROPERTYINSTEX**](propertyinstex.md) quando o analisador anexa uma definição de propriedade a uma instância de uma propriedade.

O procedimento a seguir identifica as etapas necessárias para anexar uma definição de propriedade.

**Para anexar uma definição de propriedade**

1.  Identifique cada propriedade que existe em uma instância do protocolo. Ao anexar uma definição, Monitor de Rede passa os dados capturados para o analisador. Os dados são passados em uma base de instância de protocolo.
2.  Determine o local da propriedade na instância de protocolo.
3.  Anexe uma definição de propriedade ao local da propriedade.

Monitor de Rede implementa uma estrutura [**PROPERTYINST**](propertyinst.md) quando o analisador usa os dados de propriedade como eles existem na captura. Monitor de Rede implementa uma estrutura [**PROPERTYINSTEX**](propertyinstex.md) quando o analisador deve modificar os dados de propriedade na captura.

 

 



