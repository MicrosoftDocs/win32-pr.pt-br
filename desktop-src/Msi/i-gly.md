---
description: Saiba mais Windows Installer conceitos que começam com a letra I, como a tabela Importar Endereço e o nível de instalação.
ms.assetid: b8e0a14f-ebdc-4b8f-a884-f6276dccda49
title: I (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33b5cfb9c4545a5482b214e0413ab3e3d981109
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010649"
---
# <a name="i-windows-installer"></a>I (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](f-gly.md) [](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**Arquivo .idt**
</dt> <dd>

Tabela de banco de dados do instalador exportado. Para obter mais informações, [consulte Importando e exportando e](importing-and-exporting.md) Windows Installer [extensões de arquivo](windows-installer-file-extensions.md).

</dd> <dt>

<span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Tabela Importar Endereço (IAT)**
</dt> <dd>

Onde o endereço virtual computado é salvo de cada função importada de todas as DLLs.

</dd> <dt>

<span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**interface do usuário interna**
</dt> <dd>

Recursos integrados do instalador que podem ser usados para a autor de uma interface do usuário gráfica para instalação. Um autor pode escolher uma [*interface do usuário externa*](e-gly.md). Para obter mais informações, [consulte Sobre o Interface do Usuário](about-the-user-interface.md).

</dd> <dt>

<span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**nível de instalação**
</dt> <dd>

Valor de instalação especificado. Um aplicativo será instalado somente se seu próprio nível for menor ou igual ao nível de instalação. Portanto, o conjunto de aplicativos escolhido para instalação pode ser alterado alterando o nível de instalação. Para obter mais informações, consulte [Tabela de recursos](feature-table.md).

</dd> <dt>

<span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**instalação sob demanda**
</dt> <dd>

Serviço que instala aplicativos ou recursos conforme solicitado pelo usuário ou outro aplicativo. [*A publicidade*](a-gly.md) disponibiliza um recurso ou aplicativo para instalação sob demanda. Para obter mais informações, consulte: [Instalação sob demanda.](installation-on-demand.md)

</dd> <dt>

<span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**contexto de instalação**
</dt> <dd>

A combinação de direitos de instalação e tipos de instalação produz três contextos de instalação diferentes: por usuário não gerenciado, gerenciado por usuário e gerenciado por computador. Não há essa coisa de não gerenciado por computador.

</dd> <dt>

<span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**Instalador**
</dt> <dd>

O [*Windows Installer*](m-gly.md).

</dd> <dt>

<span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**banco de dados do instalador**
</dt> <dd>

Banco de dados relacional que contém instruções de instalação para uma instalação. O banco de dados do instalador é armazenado [*no arquivo.msi .*](m-gly.md) Para obter mais informações, consulte [Installer Database](installer-database.md).

</dd> <dt>

<span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**função do instalador**
</dt> <dd>

Chamado por um usuário ou aplicativo para obter serviços e funcionalidades do instalador. Essa é a interface de programação de aplicativo do instalador. Para obter informações, consulte [Referência de função do instalador](installer-function-reference.md).

</dd> <dt>

<span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**ferramenta de autor de pacote do instalador**
</dt> <dd>

Software que permite que um desenvolvedor crie e edite um [*arquivo.msi .*](m-gly.md) Isso junto com os [*arquivos de origem externos*](e-gly.md) compõem [*um*](p-gly.md) pacote que contém todas as informações necessárias para uma instalação.

</dd> <dt>

<span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**arquivos de origem internos**
</dt> <dd>

Armazenado no arquivo [*.msi .*](m-gly.md) Vários arquivos de origem internos podem ser compactados e armazenados juntos em um arquivo [*de gabinete*](c-gly.md) armazenado em um .msi arquivo.

</dd> </dl>

 

 



