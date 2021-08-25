---
description: Os módulos de mesclagem raramente exigem uma interface do usuário.
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: Criando interfaces de usuário em módulos de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 931e539d8880c490853b20a6e53b3000f390c0b29f81bf8bb9d3e3703e3f7905
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829186"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a>Criando interfaces de usuário em módulos de mesclagem

Os módulos de mesclagem raramente exigem uma interface do usuário. A liberação de um módulo de mesclagem que contém ambos os componentes instaláveis e uma interface do usuário restringe, por fim, a flexibilidade do usuário do módulo. A combinação dos componentes e da interface do usuário em um módulo pode impedir que os desenvolvedores usem sua própria interface do usuário ou forneçam instalações silenciosas. Uma alternativa melhor é lançar dois módulos de mesclagem, um que instala silenciosamente os componentes e um segundo módulo opcional que contém a interface do usuário. O módulo com a interface do usuário deve listar o módulo de componente em sua [tabela ModuleDependency](moduledependency-table.md). Esse método permite que os autores de módulo forneçam uma interface do usuário sem forçá-lo a desenvolvedores.

Quando as tabelas de interface do usuário são usadas em módulos de mesclagem, elas podem ser mescladas da mesma maneira que qualquer outra tabela.

 

 



