---
description: A aplicação de patches do UAC (controle de conta de usuário) permite que os autores de instalações de Windows Installer identifiquem patches assinados digitalmente que podem ser aplicados no futuro por usuários não administradores.
ms.assetid: f7d64f61-24c8-4037-a10b-d68d0e9e3c42
title: Aplicação de patch de UAC (controle de conta de usuário)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d111a39245ab15b24c1734d278a8e0a477e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837296"
---
# <a name="user-account-control-uac-patching"></a>Aplicação de patch de UAC (controle de conta de usuário)

A aplicação de patches do UAC ( [*controle de conta de usuário*](u-gly.md) ) permite que os autores de instalações de Windows Installer identifiquem patches assinados digitalmente que podem ser aplicados no futuro por usuários não administradores.

Se a assinatura digital não corresponder ao certificado, o Windows Vista exibirá uma caixa de diálogo do UAC solicitando a autorização do administrador antes de instalar o patch. Em sistemas anteriores ao Windows Vista, o instalador não aplicará um patch assinado que não corresponda ao certificado.

Se um não administrador tentar aplicar um patch a um aplicativo e as seguintes condições não tiverem sido atendidas, o Windows Vista notificará o usuário de que a autorização do administrador é necessária antes de instalar o patch. Um não administrador pode continuar instalando o patch, sem a necessidade de obter autorização de administrador adicional, desde que as condições a seguir sejam atendidas.

-   O aplicativo foi instalado no Windows Vista ou no Windows XP usando Windows Installer 3,0 ou posterior.

    **Windows Server 2008:** Sem suporte.

-   Se o aplicativo tiver sido instalado no Windows XP, o aplicativo também deverá ter sido instalado a partir de mídia removível, como um CD-ROM ou um disco de DVD. Essa restrição não se aplicará se o aplicativo tiver sido instalado no Windows Vista.
-   O aplicativo não foi instalado a partir de uma imagem de origem de [instalação administrativa](administrative-installation.md) .
-   O aplicativo foi originalmente instalado por computador. Para obter informações sobre como habilitar não administradores para aplicar patches a aplicativos gerenciados por usuário após o patch ter sido aprovado como confiável por um administrador, consulte [aplicação de patch Per-User aplicativos gerenciados](patching-per-user-managed-applications.md).
-   A [tabela MsiPatchCertificate](msipatchcertificate-table.md) está presente no pacote do instalador de janela (arquivo. msi) e contém as informações necessárias para habilitar o UAC. A tabela e as informações podem ter sido incluídas no pacote de instalação original ou adicionadas ao pacote por um arquivo de patch Windows Installer (arquivo. msp).
-   Os patches são assinados digitalmente por um certificado listado na [tabela MsiPatchCertificate](msipatchcertificate-table.md). Para obter mais informações sobre certificados de assinatura digital, consulte [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md).
-   A assinatura digital no pacote de patch pode ser verificada em relação ao certificado na [tabela MsiPatchCertificate](msipatchcertificate-table.md). Para obter mais informações sobre o uso de assinaturas digitais, certificados digitais e [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), consulte a seção [segurança](https://msdn.microsoft.com/library/cc527452.aspx) do SDK (Software Development Kit) do Microsoft Windows.
-   O certificado de signatário usado para verificar a assinatura digital no pacote de patch é válido e não foi revogado.
    > [!Note]  
    > Embora não seja possível assinar um patch usando um certificado expirado, a avaliação de uma assinatura digital em um patch não falhará se o certificado tiver expirado. A avaliação usa a [tabela MsiPatchCertificate](msipatchcertificate-table.md)atual, que consiste na tabela MsiPatchCertificate no pacote original e quaisquer alterações na tabela por patches sequenciados antes do atual. Um patch pode adicionar novos certificados à tabela MsiPatchCertificate para avaliar os patches sequenciados após o patch atual. Um certificado revogado é sempre rejeitado.

     

-   A aplicação de patches com privilégios mínimos não foi desabilitada pela definição da propriedade [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) ou da política [DisableLUAPatching](disableluapatching.md) .

Um patch que foi aplicado usando a aplicação de patch do UAC também pode ser removido por um não administrador.

Os administradores podem aplicar patches a produtos instalados por computador, independentemente da configuração do UAC do aplicativo.

Você pode determinar se a aplicação de patches com privilégios mínimos está habilitada para um aplicativo usando a função [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) para consultar a \_ propriedade de aplicativo lua AUTORIZAda do InstallProperty \_ \_ ou usando o método [**ProductInfo**](installer-productinfo.md) para consultar a propriedade "AuthorizedLUAApp". Se o valor de uma das propriedades for 1, o aplicativo será habilitado para aplicação de patch de conta de usuário com privilégios mínimos.

Um administrador pode desabilitar a aplicação de patches com privilégios mínimos no computador definindo a política [DisableLUAPatching](disableluapatching.md) como 1. Você pode definir a propriedade [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) como 1 durante a instalação inicial de um aplicativo para evitar a aplicação de patches com privilégios mínimos somente para esse aplicativo.

Essa funcionalidade está disponível a partir do Windows Installer versão 3,0. A aplicação de patch de UAC (controle de conta de usuário) foi chamada aplicação de patches de LUA (conta de usuário com privilégios mínimos) no Windows XP. A aplicação de patches de LUA não está disponível no Windows 2000 e no Windows Server 2003.

Para obter mais informações sobre compatibilidade de aplicativos e desenvolvimento de aplicativos que são compatíveis com o UAC (controle de conta de usuário), consulte as informações do UAC fornecidas no [Microsoft TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)).

 

 
