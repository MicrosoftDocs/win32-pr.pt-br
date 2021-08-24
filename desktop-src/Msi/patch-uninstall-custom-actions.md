---
description: Você pode usar a opção de desinstalação do patch de ação personalizada para especificar que o instalador execute a ação personalizada somente quando um patch for desinstalado.
ms.assetid: c741aa40-ba4c-459e-936a-19c002620c30
title: Corrigir ações personalizadas de desinstalação de patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69077337b80177984ff43f12038edb1daa48215f92c627f4ed22ea2f69c876b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145419"
---
# <a name="patch-uninstall-custom-actions"></a>Corrigir ações personalizadas de desinstalação de patch

Você pode usar a [opção de desinstalação do patch de ação personalizada](custom-action-patch-uninstall-option.md) para especificar que o instalador execute a ação personalizada somente quando um patch for desinstalado.

**Windows Installer 4,5 e posterior:** Você pode usar a [opção de desinstalação de patch de ação personalizada](custom-action-patch-uninstall-option.md) para especificar que o instalador só executa a ação personalizada quando um patch é desinstalado.

**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md): * *

A [opção de desinstalação de patch de ação personalizada](custom-action-patch-uninstall-option.md) não está disponível. Não há nenhum método para marcar uma [ação personalizada](custom-actions.md) em um pacote de patch a ser executado quando o patch é desinstalado porque o instalador não aplica os pacotes de patch que estão sendo desinstalados.

Para que uma [ação personalizada](custom-actions.md) seja executada quando um patch específico é desinstalado, a ação personalizada deve estar presente no aplicativo original ou estar em um patch para o produto que sempre é aplicado.

os desenvolvedores podem usar a propriedade [**MsiPatchRemovalList**](msipatchremovallist.md) para criar um pacote Windows Installer ou patch que executa [ações personalizadas](custom-actions.md) sobre a remoção de um patch. A ação personalizada pode ser criada no pacote de instalação original, um patch que já foi aplicado ao pacote ou um patch que não é um [patch desinstalável](uninstallable-patches.md). A ação personalizada pode ser condicional na propriedade **MsiPatchRemovalList** nas tabelas de sequência. Consulte [usando propriedades em instruções condicionais](using-properties-in-conditional-statements.md) para obter mais informações sobre a condicionalização de ações.

A ação personalizada pode obter os GUIDs dos patches que estão sendo removidos do valor da propriedade [**MsiPatchRemovalList**](msipatchremovallist.md) . A ação personalizada pode determinar se o estado de instalação do patch é aplicado, obsoleto ou substituído chamando o [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) ou a propriedade [**patchproperty**](patch-patchproperty.md) do [objeto patch](patch-object.md).

Se a ação personalizada exigir metadados especiais do patch, o patch deverá conter uma ação personalizada que grava os metadados em um registro ou local de arquivo quando o patch é aplicado. A ação personalizada no aplicativo original ou um patch sempre aplicado pode obter as informações necessárias para remover as alterações do patch.

Patches que fazem dificuldade de desfazer corretamente não devem ser marcados como [patches desinstaláveis](uninstallable-patches.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sequenciamento de patch](sequencing-patches.md)
</dt> <dt>

[Removendo patches](removing-patches.md)
</dt> <dt>

[Patches desinstaláveis](uninstallable-patches.md)
</dt> <dt>

[Desinstalando patches](uninstalling-patches.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



