---
description: Uma ação encapsula uma função típica executada durante a instalação ou manutenção de um aplicativo. Windows O instalador tem muitas ações padrão internas. Os desenvolvedores de pacotes de instalação também podem criar suas próprias ações personalizadas.
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: Ações padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e95c3ab95a7bddc1f23dd38108b2cb10978ad5316da60397e6f3ba019a415ac4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627616"
---
# <a name="standard-actions"></a>Ações padrão

Uma ação encapsula uma função típica executada durante a instalação ou manutenção de um aplicativo. Windows O instalador tem muitas ações padrão internas. Os desenvolvedores de pacotes de instalação também podem criar suas próprias [ações personalizadas](custom-actions.md).

Exemplos de ações padrão do instalador incluem:

-   [Ação Createatalhos](createshortcuts-action.md): gerencia a criação de atalhos para arquivos instalados com o aplicativo atual. Essa ação usa a [tabela de atalho](shortcut-table.md) para seus dados.
-   [Ação InstallFiles](installfiles-action.md): copia os arquivos selecionados do diretório de origem para o diretório de destino. Essa ação usa a [tabela de arquivos](file-table.md) para seus dados.
-   [Ação WriteRegistryValues](writeregistryvalues-action.md): configura as informações do registro que o aplicativo requer no registro. Essa ação usa a [tabela de registro](registry-table.md) para seus dados.

As seções a seguir discutem ações padrão.

-   [Sobre as ações padrão](about-standard-actions.md)
-   [Usando ações padrão](using-standard-actions.md)
-   [Referência de ações padrão](standard-actions-reference.md)

 

 



