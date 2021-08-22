---
description: Saiba mais Windows conceitos do Instalador que começam com a letra A, como a fase de acessibilidade e aquisição.
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (Windows Instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715e051d584ada5c96fbc8ac5cdf717b666276f81ea6f94331217a766074bace
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066476"
---
# <a name="a-windows-installer"></a>A (Windows Instalador)

A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**Acessibilidade**
</dt> <dd>

Implementação de design para tornar a interface do usuário do instalador acessível a todos os usuários. Para obter mais informações sobre acessibilidade, consulte o tópico de visão geral: [Acessibilidade](accessibility.md).

</dd> <dt>

<span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**fase de aquisição**
</dt> <dd>

Fase de instalação durante a qual o instalador determina o procedimento. A fase de aquisição começa quando um aplicativo ou usuário instrui [*Windows Instalador*](m-gly.md) a instalar um aplicativo ou recurso. Em seguida, o instalador consulta o [*banco de*](i-gly.md) dados para obter informações, pois gera o script [*de execução*](e-gly.md) para a instalação. Para obter mais informações sobre as fases de uma instalação, consulte [Mecanismo de Instalação](installation-mechanism.md).

</dd> <dt>

<span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**Ação**
</dt> <dd>

Muitas das funções executadas pelo Windows Instalador são encapsuladas em ações. Cada ação especifica a execução de uma função específica e o fluxo de procedimento total da instalação é prescrito pela sequência de ações nas tabelas [*Sequence*](s-gly.md). [*As ações padrão*](s-gly.md) são criadas Windows Instalador. [*As ações*](c-gly.md) personalizadas são escritas pelo autor do pacote de [*instalação*](p-gly.md).

</dd> <dt>

<span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Modo de aprovação do administrador**
</dt> <dd>

O estado de aprovação habilitado pela UAC (Proteção de Conta de Usuário) que executa todos os usuários com privilégios mínimos, incluindo administradores. Os usuários precisam fornecer consentimento para elevar instalações que exigem privilégios de administrador.

</dd> <dt>

<span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**Publicidade**
</dt> <dd>

Capacidade de disponibilizar as interfaces necessárias para carregar e disponibilizar um aplicativo sem instalar o aplicativo. Quando um usuário ou aplicativo ativa uma interface anunciada, o instalador continua a instalar os componentes necessários. Os dois tipos de publicidade estão [*atribuindo*](/windows) e [*publicando*](p-gly.md). Para obter mais informações, consulte [*também install-on-demand*](i-gly.md). Para obter mais informações sobre como o instalador anuncia aplicativos, consulte [Anúncio](advertisement.md).

</dd> <dt>

<span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Serviço de Informações do Aplicativo (AIS)**
</dt> <dd>

Um serviço de sistema do Windows Vista que facilita o início de instalações que exigem privilégios elevados para ser executado. Fornece a interface do usuário de consentimento usada pelo Controle de Conta de Usuário para solicitar autorização de administrador a um usuário.

</dd> <dt>

<span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**Atribuir**
</dt> <dd>

Disponibiliza um aplicativo e o torna exibido como se ele tivesse sido instalado para um usuário, sem realmente instalá-lo. Atribuir adiciona atalhos e ícones ao **menu** Iniciar, associa arquivos apropriados e grava entradas do Registro para o aplicativo. Quando um usuário tenta abrir um aplicativo atribuído, o instalador instala o aplicativo. Atribuir e [*publicar são*](p-gly.md) dois métodos de [*publicidade.*](/windows) Para obter mais informações, consulte [Anúncio](advertisement.md).

</dd> <dt>

<span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**execução assíncrona**
</dt> <dd>

[*Ação personalizada*](c-gly.md) durante a qual o instalador executa threads separados da ação personalizada e da instalação atual simultaneamente. Para obter mais informações, consulte Ações personalizadas síncronas e [assíncronas](synchronous-and-asynchronous-custom-actions.md).

</dd> </dl>

 

 
