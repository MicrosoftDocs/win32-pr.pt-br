---
description: Defina a propriedade MSIENFORCEUPGRADECOMPONENTRULES como 1 na linha de comando ou na tabela de propriedades para aplicar as regras de atualização de componente durante pequenas atualizações e pequenas atualizações de um produto específico.
ms.assetid: 0c8424c7-ab9b-4a09-aaa8-6a3f44c2789f
title: Propriedade MSIENFORCEUPGRADECOMPONENTRULES
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d5946ba3a0001c988ddfe76eeaf95c008205b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811838"
---
# <a name="msienforceupgradecomponentrules-property"></a>Propriedade MSIENFORCEUPGRADECOMPONENTRULES

Defina a propriedade **MSIENFORCEUPGRADECOMPONENTRULES** como 1 na linha de comando ou na [tabela de propriedades](property-table.md) para aplicar as regras de atualização de componente durante [pequenas atualizações](small-updates.md) e pequenas [atualizações](minor-upgrades.md) de um produto específico. Para aplicar as regras durante pequenas atualizações e pequenas atualizações de todos os produtos no computador, defina a política [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) como 1.

Quando a propriedade ou a política é definida como 1, [as pequenas atualizações](small-updates.md) e atualizações [secundárias](minor-upgrades.md) podem falhar porque a atualização tenta fazer o seguinte que viola as regras de componente de atualização:

-   Adicione um novo recurso à parte superior ou central de uma árvore de recursos existente.

    O novo recurso deve ser adicionado como um novo recurso folha a uma árvore de recursos existente.

    Nesse caso, o [**ProductCode**](productcode.md) do produto pode ser alterado e a atualização pode ser tratada como uma [atualização principal](major-upgrades.md).

-   Remover um componente de um recurso.

    Isso também pode ocorrer se você alterar o GUID de um componente. O componente identificado pelo GUID original parece ser removido e o componente, conforme identificado pelo novo GUID, aparece como um novo componente.

    **Windows Installer 4,5 e posterior:** O componente pode ser removido corretamente usando Windows Installer 4,5 e posterior definindo o atributo **msidbComponentAttributesUninstallOnSupersedence** na tabela de [componentes](component-table.md) ou definindo a propriedade [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) .

    Como alternativa, o [**ProductCode**](productcode.md) do produto pode ser alterado e a atualização pode ser tratada como uma [atualização principal](major-upgrades.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




