---
description: Use o sinalizador de opção a seguir para especificar que o instalador execute a ação personalizada somente quando um patch estiver sendo desinstalado. Para definir a opção, adicione o valor nessa tabela ao valor no campo Extended da tabela CustomAction.
ms.assetid: aa4d9e21-5316-42b5-a22e-c7a5becd3cae
title: Opção de desinstalação de patch de ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108365876393733f7cc520ae565bb2c5ea7ff3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752660"
---
# <a name="custom-action-patch-uninstall-option"></a>Opção de desinstalação de patch de ação personalizada

Use o sinalizador de opção a seguir para especificar que o instalador execute a ação personalizada somente quando um patch estiver sendo desinstalado. Para definir a opção, adicione o valor nessa tabela ao valor no campo Extended da [tabela CustomAction](customaction-table.md).

**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte. Essa opção está disponível a partir do Windows Installer 4,5.



| Constante                                | Hexadecimal | Decimal | Descrição                                                    |
|-----------------------------------------|-------------|---------|----------------------------------------------------------------|
| **msidbCustomActionTypePatchUninstall** | 0x8000      | 32768   | A ação personalizada é executada somente quando um patch está sendo desinstalado. |



 

## <a name="remarks"></a>Comentários

Esse atributo pode ser adicionado a uma ação personalizada por meio de sua criação no pacote de Windows Installer (arquivo. msi). Uma nova ação personalizada com esse atributo pode ser adicionada por um patch. Uma ação personalizada que tenha esse atributo pode ser atualizada por um patch. Este atributo não pode ser adicionado ou removido por um patch para uma ação personalizada existente.

Se um patch adicionar ou atualizar uma ação personalizada com esse atributo, Windows Installer executará a ação personalizada nova ou atualizada quando o patch for desinstalado. Windows Installer faz com que as atualizações no patch sejam desinstaladas disponíveis para a ação personalizada de desinstalação do patch. O patch deve incluir uma [tabela *<PatchGUID>* MsiTransformView](msitransformview.md) para fornecer essas informações para Windows Installer.

Quando um pacote que contém uma ação personalizada com o atributo **msidbCustomActionTypePatchUninstall** é instalado usando uma versão do instalador anterior à Windows Installer 4,0, o instalador não chama a ação personalizada quando o patch é desinstalado. A instalação pode executar a ação personalizada durante a instalação, o reparo ou a atualização do pacote.

Ações personalizadas com o atributo **msidbCustomActionTypePatchUninstall** devem ser condicionadas usando a propriedade [**MSIPATCHREMOVE**](msipatchremove.md) para impedir que a ação personalizada seja executada durante a instalação, reparo ou atualização usando um sistema com Windows Installer 4,0 ou anterior. Quando o Windows Installer 4,5 e posterior está instalado, todos os patches no sistema que têm ações personalizadas marcadas com o atributo **msidbCustomActionTypePatchUninstall** executam a ação personalizada durante a desinstalação do patch. Se Windows Installer 4,5 ou posterior for removido do sistema, os patches perderão a funcionalidade de desinstalação do patch de ação personalizada.

Para obter informações sobre como executar uma ação personalizada durante a desinstalação de um patch usando uma versão anterior à Windows Installer 4,5, consulte [patches personalizados para desinstalar as ações](patch-uninstall-custom-actions.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md)
</dt> <dt>

[Referência de ação personalizada](custom-action-reference.md)
</dt> <dt>

[Sobre ações personalizadas](about-custom-actions.md)
</dt> <dt>

[Usando ações personalizadas](using-custom-actions.md)
</dt> <dt>

[MsiTransformView *<PatchGUID>*](msitransformview.md)
</dt> </dl>

 

 



