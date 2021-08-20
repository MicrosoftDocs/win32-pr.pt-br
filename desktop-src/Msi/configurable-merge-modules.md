---
description: Módulos de mesclagem (arquivos .msm) podem ser autores para conter atributos configuráveis pelo consumidor do módulo de mesclagem.
ms.assetid: 461436f0-3a91-4a49-934a-f975bf13df40
title: Módulos de mesclagem configuráveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ca110b45e1ec9bd28662c24440124bb75d0dde73d6e425146e8be640ae2de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144265"
---
# <a name="configurable-merge-modules"></a>Módulos de mesclagem configuráveis

Módulos de mesclagem (arquivos .msm) podem ser autores para conter atributos configuráveis pelo consumidor do módulo de mesclagem. Isso permite que o módulo de mesclagem seja configurado no momento em que o pacote de instalação e o módulo são mesclados e instalados pelo usuário final. Módulos de mesclagem configuráveis Mergemod.dll versão 2.0, mas podem ser executados em qualquer versão do Windows Instalador.

A implementação de módulos de mesclagem configuráveis consiste em duas partes. Primeiro, ao criar o módulo de mesclagem (arquivo .msm), o autor do módulo de mesclagem adiciona informações ao banco de dados do módulo que especifica quais itens podem ser modificados e como esses itens podem ser configurados pelo usuário do módulo. O autor adiciona entradas [](merge-module-database-tables.md) às Tabelas de Banco de Dados do Módulo de Mesclagem reservadas para informações configuráveis ([Tabela ModuleConfiguration](moduleconfiguration-table.md) e [Tabela ModuleSubstitution](modulesubstitution-table.md)), atualiza a tabela [ \_ Validação](-validation-table.md)e adiciona entradas para as tabelas de módulo de mesclagem configuráveis à tabela [ModuleIgnoreTable](moduleignoretable-table.md). As adições à tabela ModuleIgnore são necessárias para tornar o módulo compatível com Mergemod.dll versões anteriores à 2.0.

Em segundo lugar, ao mesclar o módulo em um pacote de instalação (arquivo .msi), o usuário final do módulo usa uma ferramenta de mesclagem. A ferramenta de mesclagem chama Mergemod.dll para expor as informações de configuração no módulo a uma ferramenta de configuração do cliente. A ferramenta de configuração pode interagir com o usuário final, mas não é necessária para expor todas as opções de configuração possíveis. Se o usuário se recusar a fornecer uma seleção para um item configurável, o módulo poderá fornecer um valor padrão. Depois que o usuário fornece à ferramenta de configuração suas seleções, a ferramenta de mesclagem chama Mergemod.dll para executar a mesclagem.

Módulos de mesclagem configuráveis são totalmente compatíveis com ferramentas anteriores Mergemod.dll versão 2.0. Nesses casos, a ferramenta usa os valores padrão no módulo.

Para obter mais informações, consulte [Usando módulos de mesclagem configuráveis](using-configurable-merge-modules.md).

 

 



