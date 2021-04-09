---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4e6b8f1343fdd68f4a6ce042852cff1e28e05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091534"
---
# <a name="p-windows-installer"></a>P (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**agrupa**
</dt> <dd>

[*arquivo. msi*](m-gly.md) e quaisquer [*arquivos de origem externos*](e-gly.md) que possam ser apontados por esse arquivo. Portanto, um pacote contém todas as informações que o Windows Installer precisa para executar a interface do usuário e instalar ou desinstalar o aplicativo. Para obter mais informações, consulte também [*banco de dados do instalador*](i-gly.md).

</dd> <dt>

<span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**código do pacote**
</dt> <dd>

GUID que identifica um pacote específico. Um código de pacote exclusivo é necessário porque algumas transformações ou pacotes de patch podem ser aplicados a mais de um aplicativo ou podem atualizar um aplicativo para outro aplicativo ou versão. Para obter mais informações, consulte [Package codes](package-codes.md).

</dd> <dt>

<span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**patch**
</dt> <dd>

Método de atualização de um arquivo que substitui somente os bits que estão sendo alterados, em vez de todo o arquivo. Isso significa que os usuários podem baixar um patch de atualização para um produto que seja muito menor do que o produto inteiro. Para obter mais informações, consulte [pacotes de patch](patch-packages.md).

</dd> <dt>

<span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**arquivo de patch**
</dt> <dd>

[Pacote P corresponder](patch-packages.md) usado para aplicação de patch. Para obter mais informações, consulte [patches e atualizações](patching-and-upgrades.md).

</dd> <dt>

<span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**modo de visualização**
</dt> <dd>

Modo para exibir o design da interface do usuário. Para obter mais informações, consulte [visualizando a interface do usuário](previewing-the-user-interface.md).

</dd> <dt>

<span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**barra de progresso**
</dt> <dd>

O controle do instalador pode ser exibido durante o tempo de execução do script que representa o progresso da instalação. Para obter mais informações, consulte [criando um controle ProgressBar](authoring-a-progressbar-control.md).

</dd> <dt>

<span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**Propriedade**
</dt> <dd>

Variáveis globais usadas durante uma instalação. (Consulte [sobre propriedades](about-properties.md).)

O termo "Propriedade" também se refere a um atributo de um objeto de automação. (Consulte [interface de automação](automation-interface.md).)

</dd> <dt>

<span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**editor**
</dt> <dd>

Método de [*anunciar*](a-gly.md) um recurso ou aplicativo. A publicação não preenche a interface do usuário. No entanto, se outro aplicativo tentar abrir um aplicativo publicado, há informações suficientes presentes para o instalador atribuir o aplicativo publicado. Para obter mais informações, consulte [*atribuindo*](a-gly.md) e [componentes e recursos](components-and-features.md).

</dd> </dl>

 

 



