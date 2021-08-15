---
description: Saiba mais Windows conceitos do Instalador que começam com a letra P, como código do pacote e a adoção de patch.
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (Windows Instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74af2780852bcb59124390042bfdbbc7bf2e7618cdb4167f58b15fc04ab1b15b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942756"
---
# <a name="p-windows-installer"></a>P (Windows Instalador)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](f-gly.md) [](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**Pacote**
</dt> <dd>

[*.msi arquivo e*](m-gly.md) quaisquer [*arquivos de origem externos*](e-gly.md) que possam ser apontados por esse arquivo. Portanto, um pacote contém todas as informações que o Windows Instalador precisa para executar a interface do usuário e instalar ou desinstalar o aplicativo. Para obter mais informações, consulte também banco [*de dados do instalador*](i-gly.md).

</dd> <dt>

<span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**código do pacote**
</dt> <dd>

GUID que identifica um pacote específico. Um código de pacote exclusivo é necessário porque algumas transformações ou pacotes de patch podem ser aplicados a mais de um aplicativo ou podem atualizar um aplicativo para outro aplicativo ou versão. Para obter mais informações, consulte [Códigos de pacote](package-codes.md).

</dd> <dt>

<span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**Remendar**
</dt> <dd>

Método de atualização de um arquivo que substitui apenas os bits que estão sendo alterados, em vez de todo o arquivo. Isso significa que os usuários podem baixar um patch de atualização para um produto muito menor do que o produto inteiro. Para obter mais informações, consulte [Pacotes de patch](patch-packages.md).

</dd> <dt>

<span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**arquivo patch**
</dt> <dd>

Pacote [de trava P](patch-packages.md) usado para a adoção de patch. Para obter mais informações, consulte [Patching and Upgrades](patching-and-upgrades.md).

</dd> <dt>

<span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**modo de visualização**
</dt> <dd>

Modo para exibir o design da interface do usuário. Para obter mais informações, consulte [Visualizando o Interface do Usuário](previewing-the-user-interface.md).

</dd> <dt>

<span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**barra de progresso**
</dt> <dd>

Controlar o instalador pode ser exibido durante o tempo de execução do script que representa o progresso da instalação. Para obter mais informações, [consulte Authoring a ProgressBar Control](authoring-a-progressbar-control.md).

</dd> <dt>

<span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**Propriedade**
</dt> <dd>

Variáveis globais usadas durante uma instalação. (Consulte [Sobre propriedades](about-properties.md).)

O termo "propriedade" também se refere a um atributo de um objeto de automação. (Consulte [Interface de Automação](automation-interface.md).)

</dd> <dt>

<span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**Publicação**
</dt> <dd>

Método de [*anunciar um*](a-gly.md) recurso ou aplicativo. A publicação não preenche a interface do usuário. No entanto, se outro aplicativo tentar abrir um aplicativo publicado, haverá informações suficientes presentes para o instalador atribuir o aplicativo publicado. Para obter mais informações, consulte [*Atribuindo componentes*](a-gly.md) [e recursos](components-and-features.md).

</dd> </dl>

 

 



