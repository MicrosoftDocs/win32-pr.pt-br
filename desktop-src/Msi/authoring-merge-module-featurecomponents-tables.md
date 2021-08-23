---
description: Uma tabela FeatureComponents em branco é necessária em cada módulo de mesclagem. Essa tabela vazia fornecerá um esquema para a ferramenta de mesclagem se o arquivo de .msi de destino não tiver sua própria tabela FeatureComponents.
ms.assetid: 19463fc7-8362-4943-8907-22c38f66fe25
title: Criando tabelas FeatureComponents do módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b2da3e25d84f4f10edad6566edeba5a10d43c5617340d40c733aa23d31f4b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650295"
---
# <a name="authoring-merge-module-featurecomponents-tables"></a>Criando tabelas FeatureComponents do módulo de mesclagem

Uma [tabela FeatureComponents](featurecomponents-table.md) em branco é necessária em cada módulo de mesclagem. Essa tabela vazia fornecerá um esquema para a ferramenta de mesclagem se o arquivo de .msi de destino não tiver sua própria tabela FeatureComponents.

Se, e somente se, não houver nenhuma tabela FeatureComponents no arquivo de .msi de destino, a ferramenta de mesclagem usará a tabela em branco fornecida no módulo. Nesse caso, a ferramenta de mesclagem cria uma tabela duplicada no arquivo de .msi de destino e adiciona linhas que associam os novos componentes no módulo de mesclagem aos recursos no pacote de instalação do aplicativo.

 

 



