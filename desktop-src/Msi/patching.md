---
description: Estas seções descrevem a adoção de patch Windows instalação do Instalador.
ms.assetid: e3c233bc-4344-449e-9e79-1a3b96ad2d08
title: Aplicação de patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb90436c2a33495aaa818d0796c5d749e5d76286db4dbdc247ec4ee58c7ea6ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926227"
---
# <a name="patching"></a>Aplicação de patch

Um aplicativo que foi instalado usando o Instalador do Microsoft Windows pode ser atualizado reinstalando um pacote de instalação atualizado (arquivo .msi) ou aplicando um patch do instalador do Windows (um arquivo .msp) ao aplicativo.

Um Windows patch do instalador do Windows (arquivo .msp) é um pacote autossunte que contém as atualizações do aplicativo e descreve quais versões do aplicativo podem receber o patch. Os patches contêm, no mínimo, duas transformaçãos de banco de dados e podem conter arquivos de patch armazenados no fluxo de arquivos de gabinete do pacote de patch. Para obter mais informações sobre as partes de um pacote de patch do Windows Installer, consulte [Pacotes de patch](patch-packages.md).

A manutenção de aplicativos fornecendo um patch Windows instalador, em vez de um pacote de instalação completo para o produto atualizado pode ter vantagens. Um patch pode conter um arquivo inteiro ou apenas os bits de arquivo necessários para atualizar parte do arquivo. Isso pode permitir que o usuário baixe um patch de atualização muito menor do que o pacote de instalação para todo o produto. Uma atualização usando um patch pode preservar uma personalização do usuário do aplicativo por meio da atualização.

**Windows Instalador 4.5 e posterior: **

A partir do Windows Installer 4.5, os desenvolvedores podem marcar componentes em um patch com o valor **msidbComponentAttributesUninstallOnSupersedence** na tabela [Component](component-table.md). Se um patch subsequente for instalado, marcado com o valor **msidbPatchSequenceSupersedeEarlier** em sua tabela [MsiPatchSequence](msipatchsequence-table.md) para substituir o primeiro patch, o Windows Installer 4.5 e posterior poderá desinstalar e desinstalar componentes **marcados como msidbComponentAttributesUninstallOnSupersedence** para evitar deixar componentes não utilizados no computador. Se o componente não estiver marcado com com esse bit, a instalação do patch de ressalto poderá deixar um componente nãoutilado no computador. Definir a **propriedade MSIUNINSTALLSUPERSEDEDCOMPONENTS** tem o mesmo efeito que definir esse bit para todos os componentes.

**Windows Instalador 3.0 e posterior: **

Os desenvolvedores que usam Windows Installer 3.0 e criam pacotes de patch que têm a tabela [MsiPatchSequence](msipatchsequence-table.md) podem criar pacotes de patch que fazem o seguinte:

-   Use a linha de base do produto armazenada em cache pelo instalador para dar mais facilidade a aplicativos de serviço com patches delta menores. Para obter mais informações sobre como usar a linha de base do produto, consulte [Reduzindo o tamanho do patch.](reducing-patch-size.md)
-   Ignore as ações associadas a tabelas específicas que não são modificadas pelo patch. Isso pode reduzir significativamente o tempo necessário para instalar o patch. Para obter mais informações sobre quais tabelas podem ser ignoradas, consulte [Otimização de patch](patch-optimization.md).
-   Crie e instale patches que podem ser desinstalados de forma completa e em qualquer ordem, sem precisar desinstalar e reinstalar todo o aplicativo e outros patches. Para obter mais informações sobre como desinstalar patches, consulte [Removendo patches](removing-patches.md).
-   Aplique patches em uma ordem constante, independentemente da ordem em que os patches são fornecidos ao sistema. Para obter mais informações sobre como o instalador Windows determina a sequência usada para aplicar patches, consulte [Sequenciando patches](sequencing-patches.md).
-   Aplique patches a um aplicativo que foi instalado em um contexto gerenciado por usuário. Para obter mais informações, consulte [Patching Per-User Managed Applications](patching-per-user-managed-applications.md).

**Windows Instalador 2.0: **

Não há suporte para a tabela [MsiPatchSequence.](msipatchsequence-table.md) A partir do Windows 3.0, os pacotes de patch podem conter informações que descrevem a sequência de a patch do patch em relação a outras atualizações e informações descritivas adicionais.

O método recomendado para criar um pacote de patch é usar ferramentas de criação de patch, [ como ](msimsp-exe.md)Msimsp.exee [Patchwiz.dll](patchwiz-dll.md). Os desenvolvedores podem gerar um arquivo de criação de patch, conforme descrito na seção: [Criando um pacote de patch](creating-a-patch-package.md). A criação de um pequeno patch de atualização é descrita na seção: Um pequeno exemplo de a patch [de atualização](a-small-update-patching-example.md).

O Microsoft Windows Installer aceita uma URL (Uniform Resource Locator) como uma fonte válida para um patch. Para obter mais informações sobre como instalar um patch localizado em um servidor Web, consulte Baixando e instalando [um patch da Internet.](downloading-and-installing-a-patch-from-the-internet.md)

Um único Windows patch do instalador (arquivo .msp) pode ser aplicado ao pacote de instalação ao instalar um aplicativo pela primeira vez. Para obter mais informações, consulte [Patching Initial Installations](patching-initial-installations.md).

Não é possível eliminar todas as circunstâncias em que a aplicação de um patch pode exigir acesso à fonte de instalação original. No entanto, para minimizar a possibilidade de que o patch exija acesso à origem original, adera aos pontos listados na seção a seguir: Impedindo que um patch exija acesso à fonte [de instalação original.](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md)

Para minimizar a possibilidade de que o patch não seja desfeito por uma transformação de personalização subsequente, normalmente o patch é instalado primeiro, seguido pela personalização. A instalação de transformaçãos de personalização primeiro e, em seguida, o patch, pode quebrar a personalização. Para obter mais informações sobre como corrigir aplicativos personalizados, consulte [Patching Customed Applications](patching-customized-applications.md).

 

 



