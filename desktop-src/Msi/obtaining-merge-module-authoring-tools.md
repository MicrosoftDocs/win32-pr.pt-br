---
description: Para gerar um módulo de mesclagem, você precisa obter uma ferramenta de software com a qual editar um arquivo .msm.
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: Obtendo ferramentas de autor de módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a85fb75c0317a6737393e67f12a7a03cd8b76c68a8261c9d26d10d06cbe484c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327876"
---
# <a name="obtaining-merge-module-authoring-tools"></a>Obtendo ferramentas de autor de módulo de mesclagem

Para gerar um módulo de mesclagem, você precisa obter uma ferramenta de software com a qual editar um arquivo .msm. Como um arquivo .msm é basicamente um arquivo .msi simplificado, você pode usar as mesmas ferramentas usadas para criar um banco de dados de instalação. Por exemplo, o aplicativo Orca.exe fornecido com o SDK Windows Installer.

Uma alternativa é comprar uma das ferramentas de empacotamento do instalador para estar disponível de fornecedores de software independentes. Há várias ferramentas de terceiros em desenvolvimento que podem ser usadas para produzir módulos de mesclagem. Se você optar por usar uma ferramenta de terceiros, verifique se ela gera módulos de mesclagem consistentes com o padrão descrito neste documento. Em particular, você deve determinar que as ferramentas de edição não fizeram nada do seguinte para o módulo de mesclagem.

-   Foram adicionadas tabelas diferentes ao módulo de mesclagem que não são referenciadas na [tabela ModuleIgnoreTable](moduleignoretable-table.md).

    Exclua essas tabelas ou adicione-as à tabela ModuleIgnoreTable.

-   Adicionada uma tabela [TextStyle desnecessária](textstyle-table.md) ao módulo de mesclagem.

    Se o módulo de mesclagem não tiver interface do usuário (e geralmente não deve), você poderá excluir essa tabela com segurança.

-   Adicionadas entradas desnecessárias à [tabela Directory](directory-table.md).

    Remova entradas desnecessárias da tabela Diretório.

-   Informações deixadas fora da tabela Validação do módulo \_ de mesclagem.

    Isso impede a validação do módulo de mesclagem. Adicione uma tabela \_ validação completa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como fazer interfaces do usuário em módulos de mesclagem](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[Como autorar tabelas de diretório do módulo de mesclagem](authoring-merge-module-directory-tables.md)
</dt> <dt>

[Validando módulos de mesclagem](validating-merge-modules.md)
</dt> </dl>

 

 



