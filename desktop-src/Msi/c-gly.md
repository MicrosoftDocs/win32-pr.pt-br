---
description: saiba mais sobre os conceitos de Windows Installer que começam com a letra C, como arquivo de gabinete e soma de verificação.
ms.assetid: f98d19c5-5187-4718-b241-3ec69454c2d6
title: C (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb0e9a1f14a3b2a7f47722d8db3e3d9cb8356df500e54dbf581bd919afb5765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581776"
---
# <a name="c-windows-installer"></a>C (Windows Installer)

[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**arquivo de gabinete**
</dt> <dd>

Arquivo único, geralmente com uma extensão .cab, que armazena arquivos compactados em uma biblioteca de arquivos. O formato de gabinete é uma maneira eficiente de empacotar vários arquivos, pois a compactação é executada em limites de arquivos, melhorando significativamente a taxa de compactação. Para obter informações sobre como criar gabinetes, consulte [arquivos de gabinete](cabinet-files.md).

</dd> <dt>

<span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**soma**
</dt> <dd>

Valor calculado que depende do conteúdo de um arquivo. Ele é armazenado com dados para detectar a corrupção do arquivo. O sistema verifica esse valor para garantir que os dados não sejam corrompidos.

</dd> <dt>

<span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**componente**
</dt> <dd>

Menor parte de uma instalação tratada pelo instalador, também um bloco de construção de um aplicativo ou recurso da perspectiva do programador. Exemplos de componentes são um grupo de arquivos relacionados, um objeto COM ou uma biblioteca. Para obter mais informações, consulte [componentes e recursos](components-and-features.md).

</dd> <dt>

<span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**confirmando bancos de dados**
</dt> <dd>

Alterações acumuladas feitas em um banco de dados. As alterações não são refletidas no banco de dados real até que o banco de dados seja confirmado. Para obter mais informações, consulte [confirmando bancos de dados](committing-databases.md).

</dd> <dt>

<span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent,**
</dt> <dd>

Aspecto da funcionalidade da interface do usuário do instalador. Um ControlEvent, típico aciona alguma ação pelo instalador após a ativação de um controle de caixa de diálogo ou outro evento. Para obter mais informações, consulte [visão geral do ControlEvent,](controlevent-overview.md).

</dd> <dt>

<span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**custos**
</dt> <dd>

Método usado pelo instalador para determinar os requisitos de espaço em disco para a instalação. O custo leva em consideração os fatores, como se os arquivos existentes precisam ser substituídos. Para obter mais informações, consulte [custos de arquivo](file-costing.md).

</dd> <dt>

<span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**arquivo. Cub**
</dt> <dd>

Módulo de validação que armazena e fornece acesso a ações personalizadas do ICE. Para obter mais informações, consulte [arquivo. Cub de exemplo](sample--cub-file.md). para obter mais informações, consulte também [Windows Installer extensões de arquivo](windows-installer-file-extensions.md).

</dd> <dt>

<span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**ação personalizada**
</dt> <dd>

Escrito pelo autor do [*pacote*](p-gly.md) , mas não embutido no instalador como uma ação padrão. Para obter mais informações, consulte [Custom Actions](custom-actions.md).

</dd> </dl>

 

 



