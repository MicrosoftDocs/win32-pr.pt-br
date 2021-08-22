---
description: Siga as diretrizes gerais para aplicar os módulos de mesclagem descritos em aplicando módulos de mesclagem.
ms.assetid: 6035b1a9-d452-4020-9fe3-c20ba874a2ed
title: Aplicando um módulo de mesclagem configurável com personalizações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e9c771493a7a8e854472d840ffc21358c9741d8b3a8ea9876251456b6badf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829196"
---
# <a name="applying-a-configurable-merge-module-with-customizations"></a>Aplicando um módulo de mesclagem configurável com personalizações

Siga as diretrizes gerais para aplicar os módulos de mesclagem descritos em [aplicando módulos de mesclagem](applying-merge-modules.md). Além disso, os consumidores de módulo de mesclagem devem fazer o seguinte para configurar um módulo de mesclagem no momento da instalação:

-   Use um módulo de mesclagem que seja criado para ter configurações configuráveis. Para obter mais informações, consulte [criando um módulo de mesclagem que pode ser configurado pelo usuário final](creating-a-merge-module-that-can-be-configured-by-the-end-user.md)
-   Use uma ferramenta de mesclagem e configuração que chama Mergemod.dll versão 2,0 ou posterior. As versões anteriores do Mergmod.dll não podem definir as configurações do módulo de mesclagem. Os autores devem criar módulos de mesclagem que forneçam valores padrão e sejam compatíveis com versões anteriores do Mergmod.dll.
-   Forneça informações de personalização quando solicitado pela ferramenta de cliente de configuração. Os autores devem criar módulos de mesclagem que usam valores padrão quando um usuário recusa a fornecer informações.

 

 



