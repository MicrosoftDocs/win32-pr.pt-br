---
description: Saiba mais sobre os conceitos de Windows Installer que começam com a letra A, como A fase de acessibilidade e aquisição.
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea91c044553ec374f28309a86002a386961d2c9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011119"
---
# <a name="a-windows-installer"></a>A (Windows Installer)

A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**acessibilidade**
</dt> <dd>

Implementação de design para tornar a interface do usuário do instalador acessível a todos os usuários. Para obter mais informações sobre acessibilidade, consulte o tópico Visão geral: [acessibilidade](accessibility.md).

</dd> <dt>

<span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**fase de aquisição**
</dt> <dd>

Fase de instalação durante a qual o instalador determina o procedimento. A fase de aquisição começa quando um aplicativo ou usuário instrui [*Windows Installer*](m-gly.md) instalar um aplicativo ou recurso. Em seguida, o instalador consulta o [*banco de dados*](i-gly.md) para obter informações à medida que gera o [*script de execução*](e-gly.md) para a instalação. Para obter mais informações sobre as fases de uma instalação, consulte [mecanismo de instalação](installation-mechanism.md).

</dd> <dt>

<span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**Action**
</dt> <dd>

Muitas das funções executadas por Windows Installer são encapsuladas em ações. Cada ação especifica a execução de uma função específica e o fluxo de procedimento total da instalação é prescrito pela sequência de ações nas tabelas de [*sequência*](s-gly.md). As [*ações padrão*](s-gly.md) são criadas em Windows Installer. As [*ações personalizadas*](c-gly.md) são gravadas pelo autor do [*pacote*](p-gly.md)de instalação.

</dd> <dt>

<span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Modo de aprovação de administrador**
</dt> <dd>

O estado de aprovação habilitado pela proteção de conta de usuário (UAC) que executa todos os usuários com privilégios mínimos, incluindo administradores. Os usuários precisam fornecer consentimento para elevar as instalações que exigem privilégios de administrador.

</dd> <dt>

<span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**anuncia**
</dt> <dd>

Capacidade de tornar as interfaces necessárias para carregar e tornar um aplicativo disponível sem instalar o aplicativo. Quando um usuário ou aplicativo ativa uma interface anunciada, o instalador continua a instalar os componentes necessários. Os dois tipos de publicidade são [*atribuição*](/windows) e [*publicação*](p-gly.md). Para obter mais informações, consulte também [*instalar sob demanda*](i-gly.md). Para obter mais informações sobre como o instalador anuncia aplicativos, consulte [anúncio](advertisement.md).

</dd> <dt>

<span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**AIS (serviço de informações de aplicativo)**
</dt> <dd>

Um serviço de sistema do Windows Vista que facilita a execução de instalações que exigem privilégios elevados para serem executadas. Fornece a IU de consentimento usada pelo controle de conta de usuário para solicitar a autorização de um usuário para o administrador.

</dd> <dt>

<span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**atribuindo**
</dt> <dd>

Disponibiliza um aplicativo e o faz aparecer como se ele fosse instalado em um usuário, sem realmente instalá-lo. A atribuição de adicionar atalhos e ícones ao menu **Iniciar** , associa arquivos apropriados e grava entradas do registro para o aplicativo. Quando um usuário tenta abrir um aplicativo atribuído, o instalador instala o aplicativo. A atribuição e a [*publicação*](p-gly.md) são dois métodos de [*publicidade*](/windows). Para obter mais informações, consulte [anúncio](advertisement.md).

</dd> <dt>

<span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**execução assíncrona**
</dt> <dd>

[*Ação personalizada*](c-gly.md) durante a qual o instalador executa threads separados da ação personalizada e a instalação atual simultaneamente. Para obter mais informações, consulte [ações personalizadas síncronas e assíncronas](synchronous-and-asynchronous-custom-actions.md).

</dd> </dl>

 

 
