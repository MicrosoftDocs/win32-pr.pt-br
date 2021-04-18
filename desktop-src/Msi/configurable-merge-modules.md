---
description: Os módulos de mesclagem (arquivos. msm) podem ser criados para conter atributos que são configuráveis pelo consumidor do módulo de mesclagem.
ms.assetid: 461436f0-3a91-4a49-934a-f975bf13df40
title: Módulos de mesclagem configuráveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716688d947ae84279dc3409bf97abe4eb58a69d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766877"
---
# <a name="configurable-merge-modules"></a>Módulos de mesclagem configuráveis

Os módulos de mesclagem (arquivos. msm) podem ser criados para conter atributos que são configuráveis pelo consumidor do módulo de mesclagem. Isso permite que o módulo de mesclagem seja configurado no momento em que o pacote de instalação e o módulo são mesclados e instalados pelo usuário final. Os módulos de mesclagem configuráveis exigem Mergemod.dll versão 2,0, mas podem ser executados em qualquer versão do Windows Installer.

A implementação de módulos de mesclagem configuráveis consiste em duas partes. Primeiro, ao criar o módulo de mesclagem (arquivo. msm), o autor do módulo de mesclagem adiciona informações ao banco de dados do módulo que especifica quais itens podem ser modificados e como esses itens podem ser configurados pelo usuário do módulo. O autor adiciona entradas às [tabelas de banco de dados do módulo de mesclagem](merge-module-database-tables.md) que são reservadas para informações configuráveis ([Tabela ModuleConfiguration](moduleconfiguration-table.md) e [tabela ModuleSubstitution](modulesubstitution-table.md)), atualiza a [ \_ tabela de validação](-validation-table.md)e adiciona entradas para as tabelas de módulo de mesclagem configuráveis à [tabela ModuleIgnoreTable](moduleignoretable-table.md). As adições à tabela ModuleIgnore são necessárias para tornar o módulo compatível com as versões de Mergemod.dll anteriores a 2,0.

Em segundo lugar, ao mesclar o módulo em um pacote de instalação (arquivo. msi), o usuário final do módulo usa uma ferramenta de mesclagem. A ferramenta de mesclagem chama Mergemod.dll para expor as informações de configuração no módulo para uma ferramenta de configuração do cliente. A ferramenta de configuração pode interagir com o usuário final, mas não é necessário para expor todas as opções de configuração possíveis. Se o usuário recusar a fornecer uma seleção para um item configurável, o módulo poderá fornecer um valor padrão. Depois que o usuário dá à ferramenta de configuração suas seleções, a ferramenta de mesclagem chama Mergemod.dll para executar a mesclagem.

Os módulos de mesclagem configuráveis são totalmente compatíveis com as ferramentas anteriores à Mergemod.dll versão 2,0. Nesses casos, a ferramenta usa os valores padrão no módulo.

Para obter mais informações, consulte [usando módulos de mesclagem configuráveis](using-configurable-merge-modules.md).

 

 



