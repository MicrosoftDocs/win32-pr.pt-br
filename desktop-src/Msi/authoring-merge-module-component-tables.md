---
description: Uma tabela de componentes é necessária em cada módulo de mesclagem.
ms.assetid: ef4a0678-bf6b-47c9-89e8-40e12da52d9b
title: Criando tabelas de componentes do módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46557541b3a6b89841fe3e26cef7c00e59dc3911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010915"
---
# <a name="authoring-merge-module-component-tables"></a>Criando tabelas de componentes do módulo de mesclagem

Uma [tabela de componentes](component-table.md) é necessária em cada módulo de mesclagem. Esta tabela contém um registro para cada componente fornecido pelo módulo de mesclagem para o arquivo. msi de destino. Observe que cada um desses componentes também deve ser especificado na [tabela ModuleComponents](modulecomponents-table.md) , descrita em [criando tabelas ModuleComponents](authoring-modulecomponents-tables.md).

Use a Convenção de nomenclatura padrão ao inserir nomes na coluna componente para garantir que o identificador de cada componente seja exclusivo para todos os módulos de mesclagem e bancos de dados de instalação. Para obter mais informações, consulte [nomeando chaves primárias em bancos de dados do módulo de mesclagem](naming-primary-keys-in-merge-module-databases.md).

Preencha os campos restantes em cada registro, conforme descrito em um banco de dados de instalação na [tabela de componentes](component-table.md). Os componentes adicionados a um pacote por um módulo de mesclagem devem aderir às diretrizes para componentes válidos do Windows Installer descritos nas seções a seguir:

-   [Componentes do Windows Installer](windows-installer-components.md)
-   [Organizando aplicativos em componentes](organizing-applications-into-components.md)

 

 



