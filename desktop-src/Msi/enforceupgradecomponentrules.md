---
description: Essa é uma política de sistema por computador que pode ser usada para aplicar regras de componente de atualização durante pequenas atualizações e atualizações secundárias.
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: EnforceUpgradeComponentRules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 882d7df0e794dfb89ab2211db1fada576bd6e056972810d582385c1404e625a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086066"
---
# <a name="enforceupgradecomponentrules"></a>EnforceUpgradeComponentRules

Essa é uma política de sistema por [computador que](system-policy.md) pode ser usada para aplicar regras de componente de atualização durante pequenas [atualizações](small-updates.md) e [atualizações secundárias.](minor-upgrades.md)

De definir a política EnforceUpgradeComponentRules como 1 para [](minor-upgrades.md) aplicar regras de componente de atualização durante pequenas atualizações e pequenas atualizações de todos os produtos no computador. [](small-updates.md) Para aplicar as regras durante pequenas atualizações e atualizações secundárias de um produto específico, de definir a propriedade [**MSFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) como 1 na linha de comando ou na tabela [Propriedade](property-table.md).

Quando a propriedade ou a política tiver sido definida como 1, pequenas atualizações e atualizações [secundárias](small-updates.md) poderão falhar porque a atualização tenta fazer o seguinte: [](minor-upgrades.md)

-   Adicione um novo recurso à parte superior ou intermediária de uma árvore de recursos existente.

    O novo recurso deve ser adicionado como um novo recurso folha a uma árvore de recursos existente.

    Nesse caso, o [**ProductCode**](productcode.md) do produto pode ser alterado e as atualizações podem ser tratadas como uma [atualização principal.](major-upgrades.md)

-   Remova um componente de um recurso.

    Isso também pode ocorrer se você alterar o GUID de um componente. O componente identificado pelo GUID original parece ser removido e o componente identificado pelo novo GUID aparece como um novo componente.

    **Windows Instalador 4.5 e posterior:** O componente pode ser removido corretamente usando o Windows Installer 4.5 ou posterior definindo o atributo **msidbComponentAttributesUninstallOnSupersedence** na tabela Component ou definindo a propriedade [](component-table.md) [**MSIUNINSTALLSUPERSEDEDCOMPONENTS.**](msiuninstallsupersededcomponents.md)

    Como alternativa, o [**ProductCode**](productcode.md) do produto pode ser alterado e as atualizações podem ser tratadas como uma [atualização principal.](major-upgrades.md)

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ Instalador \_ do** Microsoft machine \\ **software** \\ **policies** \\  \\ **microsoft Windows** \\ 

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



