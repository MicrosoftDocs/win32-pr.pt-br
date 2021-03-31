---
description: Você não pode criar instâncias das classes corrigidas no namespace localizado. As classes corrigidas no namespace localizado são tratadas como se fossem abstratas, embora não contenham o qualificador abstract.
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: Considerações sobre a classe corrigida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77a2caa315ab4878fe619c13c69bd5d2e1a2610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172304"
---
# <a name="amended-class-considerations"></a>Considerações sobre a classe corrigida

Você não pode criar instâncias das classes corrigidas no namespace localizado. As classes corrigidas no namespace localizado são tratadas como se fossem abstratas, embora não contenham o qualificador [**abstract**](standard-qualifiers.md) .

Se você recuperar uma classe corrigida de um namespace localizado usando o \_ sinalizador WBEM \_ usar \_ sinalizador de \_ qualificadores corrigidos e gerar uma instância a partir dele, a instância conterá todos os qualificadores corrigidos da classe corrigida. Não é possível armazenar essa nova classe no namespace que contém a definição de classe básica, a menos que você execute a operação **Put** com o sinalizador WBEM \_ \_ usar \_ sinalizador de \_ qualificadores corrigidos. Esse sinalizador instrui o WMI a remover quaisquer qualificadores reparados antes de salvar o objeto. Se você não especificar \_ o sinalizador WBEM \_ usar \_ \_ qualificadores corrigidos, a operação **Put** falhará com um erro de objeto do WBEM \_ E \_ alterado \_ .

 

 



