---
description: Saiba mais Windows Installer conceitos que começam com a letra C, como arquivo de gabinete e checksum.
ms.assetid: f98d19c5-5187-4718-b241-3ec69454c2d6
title: C (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e7af99ad32d8dff7f4e8509976b0004045477b
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010919"
---
# <a name="c-windows-installer"></a>C (Windows Installer)

[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**arquivo de gabinete**
</dt> <dd>

Arquivo único, geralmente com uma .cab, que armazena arquivos compactados em uma biblioteca de arquivos. O formato de gabinete é uma maneira eficiente de empacotar vários arquivos porque a compactação é executada entre limites de arquivo, melhorando significativamente a taxa de compactação. Para obter informações sobre como criar gabinetes, consulte [Arquivos de gabinete](cabinet-files.md).

</dd> <dt>

<span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**Soma**
</dt> <dd>

Valor computado que depende do conteúdo de um arquivo. Ele é armazenado com dados para detectar corrupção de arquivo. O sistema verifica esse valor para garantir que os dados não são interrompidos.

</dd> <dt>

<span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**Componente**
</dt> <dd>

A menor parte de uma instalação manipulada pelo instalador, também um bloco de construção de um aplicativo ou recurso da perspectiva do programador. Exemplos de componentes são um grupo de arquivos relacionados, um objeto COM ou uma biblioteca. Para obter mais informações, consulte [Componentes e recursos](components-and-features.md).

</dd> <dt>

<span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**commitindo bancos de dados**
</dt> <dd>

Alterações acumuladas feitas em um banco de dados. As alterações não são refletidas no banco de dados real até que o banco de dados seja confirmado. Para obter mais informações, consulte [Committing Databases](committing-databases.md).

</dd> <dt>

<span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**
</dt> <dd>

Aspecto da funcionalidade da interface do usuário do instalador. Um ControlEvent típico dispara alguma ação do instalador após a ativação de um controle de caixa de diálogo ou outro evento. Para obter mais informações, consulte [Visão geral do ControlEvent.](controlevent-overview.md)

</dd> <dt>

<span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**Custando**
</dt> <dd>

Método usado pelo instalador para determinar os requisitos de espaço em disco para instalação. O custo leva em conta fatores como se os arquivos existentes precisam ser substituídos. Para obter mais informações, consulte [Custo do arquivo](file-costing.md).

</dd> <dt>

<span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**Arquivo .file**
</dt> <dd>

Módulo de validação que armazena e fornece acesso a ações personalizadas do ICE. Para obter mais informações, consulte [Arquivo .cú de exemplo](sample--cub-file.md). Para obter mais informações, consulte [também Windows Installer extensões de arquivo](windows-installer-file-extensions.md).

</dd> <dt>

<span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**ação personalizada**
</dt> <dd>

Escrito pelo autor do [*pacote, mas*](p-gly.md) não integrado ao instalador como uma ação padrão. Para obter mais informações, consulte [Ações personalizadas.](custom-actions.md)

</dd> </dl>

 

 



