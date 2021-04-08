---
description: Essa é uma política de sistema por máquina que pode ser usada para aplicar as regras de componente de atualização durante pequenas atualizações e atualizações secundárias.
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: EnforceUpgradeComponentRules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a2fc093c2f0beb4167374f93447d978bbca8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921912"
---
# <a name="enforceupgradecomponentrules"></a>EnforceUpgradeComponentRules

Essa é uma [política de sistema](system-policy.md) por máquina que pode ser usada para aplicar as regras de componente de atualização durante [pequenas atualizações](small-updates.md) e atualizações [secundárias](minor-upgrades.md).

Defina a política EnforceUpgradeComponentRules como 1 para aplicar as regras de componente de atualização durante [pequenas atualizações](small-updates.md) [e pequenas atualizações de](minor-upgrades.md) todos os produtos no computador. Para aplicar as regras durante pequenas atualizações e pequenas atualizações de um produto específico, defina a propriedade [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) como 1 na linha de comando ou na [tabela de propriedades](property-table.md).

Quando a propriedade ou a política foi definida como 1, [as pequenas atualizações](small-updates.md) e atualizações [secundárias](minor-upgrades.md) podem falhar porque a atualização tenta fazer o seguinte:

-   Adicione um novo recurso à parte superior ou central de uma árvore de recursos existente.

    O novo recurso deve ser adicionado como um novo recurso folha a uma árvore de recursos existente.

    Nesse caso, o [**ProductCode**](productcode.md) do produto pode ser alterado e as atualizações podem ser tratadas como uma [atualização principal](major-upgrades.md).

-   Remover um componente de um recurso.

    Isso também pode ocorrer se você alterar o GUID de um componente. O componente identificado pelo GUID original parece ser removido e o componente, conforme identificado pelo novo GUID, aparece como um novo componente.

    **Windows Installer 4,5 e posterior:** O componente pode ser removido corretamente usando Windows Installer 4,5 ou posterior definindo o atributo **msidbComponentAttributesUninstallOnSupersedence** na tabela de [componentes](component-table.md) ou definindo a propriedade [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) .

    Como alternativa, o [**ProductCode**](productcode.md) do produto pode ser alterado e as atualizações podem ser tratadas como uma [atualização principal](major-upgrades.md).

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



