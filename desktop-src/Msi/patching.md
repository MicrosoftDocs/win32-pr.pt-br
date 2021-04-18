---
description: Estas seções descrevem a aplicação de patch em uma instalação Windows Installer.
ms.assetid: e3c233bc-4344-449e-9e79-1a3b96ad2d08
title: Aplicação de patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3117723bda1699eeae341fc75db201421f6ae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780947"
---
# <a name="patching"></a>Aplicação de patch

Um aplicativo que foi instalado usando o Microsoft Windows Installer pode ser atualizado reinstalando um pacote de instalação atualizado (arquivo. msi) ou aplicando um patch de Windows Installer (um arquivo. msp) ao aplicativo.

Um patch Windows Installer (arquivo. msp) é um pacote independente que contém as atualizações para o aplicativo e descreve quais versões do aplicativo podem receber o patch. Os patches contêm, no mínimo, duas transformações de banco de dados e podem conter arquivos de patch que são armazenados no fluxo do arquivo de gabinete do pacote de patch. Para obter mais informações sobre as partes de um pacote de patches Windows Installer, consulte [pacotes de patches](patch-packages.md).

A manutenção de aplicativos ao fornecer um patch Windows Installer, em vez de um pacote de instalação completo para o produto atualizado, pode ter vantagens. Um patch pode conter um arquivo inteiro ou apenas os bits de arquivo necessários para atualizar parte do arquivo. Isso pode permitir que o usuário Baixe um patch de atualização que seja muito menor do que o pacote de instalação para todo o produto. Uma atualização usando um patch pode preservar uma personalização de usuário do aplicativo por meio da atualização.

* * Windows Installer 4,5 e posterior: * *

A partir do Windows Installer 4,5, os desenvolvedores podem marcar componentes em um patch com o valor **msidbComponentAttributesUninstallOnSupersedence** na [tabela de componentes](component-table.md). Se um patch subsequente estiver instalado, marcado com o valor **msidbPatchSequenceSupersedeEarlier** em sua [tabela MsiPatchSequence](msipatchsequence-table.md) para substituir o primeiro patch, Windows Installer 4,5 e posterior poderá cancelar o registro e desinstalar os componentes marcados como **msidbComponentAttributesUninstallOnSupersedence** para evitar a saída dos componentes não utilizados no computador. Se o componente não estiver marcado com esse bit, a instalação do patch substituto poderá deixar um componente não utilizado no computador. Definir a propriedade **MSIUNINSTALLSUPERSEDEDCOMPONENTS** tem o mesmo efeito que definir esse bit para todos os componentes.

* * Windows Installer 3,0 e posterior: * *

Os desenvolvedores que usam o Windows Installer 3,0 e criam pacotes de patches que têm a [tabela MsiPatchSequence](msipatchsequence-table.md) podem criar pacotes de patches que fazem o seguinte:

-   Use a linha de base do produto armazenada em cache pelo instalador para fazer a manutenção de aplicativos mais facilmente com patches Delta menores. Para obter mais informações sobre como usar a linha de base do produto, consulte [reduzindo o tamanho do patch](reducing-patch-size.md).
-   Ignorar ações associadas a tabelas específicas que não são modificadas pelo patch. Isso pode reduzir significativamente o tempo necessário para instalar o patch. Para obter mais informações sobre quais tabelas podem ser ignoradas, consulte [otimização de patch](patch-optimization.md).
-   Crie e instale patches que podem ser desinstalados individualmente, e em qualquer ordem, sem precisar desinstalar e reinstalar todo o aplicativo e outros patches. Para obter mais informações sobre a desinstalação de patches, consulte [removendo patches](removing-patches.md).
-   Aplique patches em uma ordem constante, independentemente da ordem em que os patches são fornecidos ao sistema. Para obter mais informações sobre como o Windows Installer determina a sequência usada para aplicar patches, consulte [sequenciando patches](sequencing-patches.md).
-   Aplique patches a um aplicativo que foi instalado em um contexto gerenciado por usuário. Para obter mais informações, consulte [aplicação de patches Per-User aplicativos gerenciados](patching-per-user-managed-applications.md).

* * Windows Installer 2,0: * *

Não há suporte para a [tabela MsiPatchSequence](msipatchsequence-table.md) . A partir do Windows Installer 3,0, os pacotes de patch podem conter informações que descrevem a sequência de patches para o patch em relação a outras atualizações e informações descritivas adicionais.

O método recomendado para criar um pacote de patch é usar ferramentas de criação de patch, como [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md). Os desenvolvedores podem gerar um arquivo de criação de patch conforme descrito na seção: [criando um pacote de patch](creating-a-patch-package.md). A criação de um patch de atualização pequeno é descrita na seção: [um exemplo de aplicação de patch de atualização pequena](a-small-update-patching-example.md).

Microsoft Windows Installer aceita um URL (Uniform Resource Locator) como uma fonte válida para um patch. Para obter mais informações sobre como instalar um patch localizado em um servidor Web, consulte [baixando e instalando um patch da Internet](downloading-and-installing-a-patch-from-the-internet.md).

Um único Windows Installer patch (arquivo. msp) pode ser aplicado ao pacote de instalação ao instalar um aplicativo pela primeira vez. Para obter mais informações, consulte [aplicação de patch nas instalações iniciais](patching-initial-installations.md).

Não é possível eliminar todas as circunstâncias quando a aplicação de um patch pode exigir acesso à fonte de instalação original. No entanto, para minimizar a possibilidade de que seu patch exija acesso à fonte original, siga os pontos listados na seção a seguir: [impedir que um patch exija acesso à fonte de instalação original](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md).

Para minimizar a possibilidade de o patch não ser interrompido por uma transformação de personalização subsequente, normalmente o patch é instalado primeiro, seguido pela personalização. Instalar as transformações de personalização primeiro e, em seguida, o patch, pode interromper a personalização. Para obter mais informações sobre aplicação de patch em aplicativos personalizados, consulte [aplicação de patch em aplicativos personalizados](patching-customized-applications.md).

 

 



