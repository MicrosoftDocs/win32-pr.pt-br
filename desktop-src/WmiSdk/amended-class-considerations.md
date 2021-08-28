---
description: Não é possível criar instâncias das classes corrigidas no namespace localizado. Classes corrigidas no namespace localizado são tratadas como se elas são abstratas, embora não contenham o qualificador Abstract.
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: Considerações de classe corrigidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cd38bc6134c4fd3596cc36e8a7638eaa1fd6ed264c90302d921a391982e5d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320233"
---
# <a name="amended-class-considerations"></a>Considerações de classe corrigidas

Não é possível criar instâncias das classes corrigidas no namespace localizado. Classes corrigidas no namespace localizado são tratadas como se elas são abstratas, embora não contenham o [**qualificador**](standard-qualifiers.md) Abstract.

Se você recuperar uma classe corrigida de um namespace localizado usando o sinalizador WBEM \_ \_ USE \_ AMENDED QUALIFIERS e gerar uma instância dele, a instância conterá todos os qualificadores corrigidos da classe \_ corrigida. Você não pode armazenar essa nova classe no namespace que contém a definição de classe básica, a menos que você execute a operação **put** com o sinalizador WBEM \_ USE \_ \_ \_ QUALIFICADORES CORRIGIDOs. Esse sinalizador instrui o WMI a retirar todos os qualificadores corrigidos antes de salvar o objeto. Se você não especificar WBEM FLAG USE QUALIFICADORES CORRIGIDOs, a operação put falhará com um \_ \_ erro \_ \_ WBEM  \_ \_ EMENDED \_ OBJECT.

 

 



