---
description: Os módulos de mesclagem raramente exigem uma interface do usuário.
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: Criando interfaces de usuário em módulos de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2df8781efea35ddd854ef76c2155d4a2ded7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764665"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a>Criando interfaces de usuário em módulos de mesclagem

Os módulos de mesclagem raramente exigem uma interface do usuário. A liberação de um módulo de mesclagem que contém ambos os componentes instaláveis e uma interface do usuário restringe, por fim, a flexibilidade do usuário do módulo. A combinação dos componentes e da interface do usuário em um módulo pode impedir que os desenvolvedores usem sua própria interface do usuário ou forneçam instalações silenciosas. Uma alternativa melhor é lançar dois módulos de mesclagem, um que instala silenciosamente os componentes e um segundo módulo opcional que contém a interface do usuário. O módulo com a interface do usuário deve listar o módulo de componente em sua [tabela ModuleDependency](moduledependency-table.md). Esse método permite que os autores de módulo forneçam uma interface do usuário sem forçá-lo a desenvolvedores.

Quando as tabelas de interface do usuário são usadas em módulos de mesclagem, elas podem ser mescladas da mesma maneira que qualquer outra tabela.

 

 



