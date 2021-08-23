---
description: Instmsi.exe é o pacote redistribuível para a instalação do Windows Installer&\# 160;2.0 e versões anteriores do Windows Installer. Consulte Windows Redistribuíveis do Instalador para os redistribuíveis do Windows Installer&\# 160;3.0 e versões posteriores.
ms.assetid: 74ea4530-3a73-4169-b0b7-f0272229192d
title: Instmsi.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2177fbb145dbfe2817dba2207cff95e5d80b801cc2f442085ba396f461870f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946114"
---
# <a name="instmsiexe"></a>Instmsi.exe

Instmsi.exe é o pacote redistribuível para a instalação do Windows Installer 2.0 e versões anteriores do Windows Installer. Consulte [Windows Redistribuíveis](windows-installer-redistributables.md) do Instalador para os redistribuíveis do Windows Installer 3.0 e versões posteriores.

Para obter mais informações sobre qual versão do Windows Installer foi enviada com seu sistema operacional, consulte Versões lançadas [do Windows Installer](released-versions-of-windows-installer.md).

Alguns redistribuíveis não devem ser executados em determinadas versões do sistema operacional. A tabela a seguir descreve qual Instmsi é compatível com qual sistema operacional.



| Se Instmsi.exe instalar esta versão do Windows Installer | Instmsi.exe pode ser executado nesses sistemas operacionais                    | Instmsi.exe não deve ser executado nesses sistemas operacionais                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Windows Instalador versão 1.0                                 | Windows 95, Windows 98, Windows NT 4.0+SP3                           | Windows Eu, Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008 |
| Windows Instalador versão 1.1                                 | Windows 95, Windows 98, Windows NT 4.0+SP3                           | Windows Eu, Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008 |
| Windows Instalador versão 1.2                                 | Windows 95, Windows 98, Windows Me, Windows NT 4.0+SP3               | Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008             |
| Windows Instalador versão 2.0                                 | Windows 95, Windows 98, Windows Me, Windows NT 4.0+SP6, Windows 2000 | Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008                           |



 

Por exemplo, um aplicativo que redistribui o Windows Installer versão 1.1 deve verificar se o sistema operacional é Windows NT 4.0 SP3 ou Windows 98/95 antes de executar o pacote redistribuível. Os aplicativos que usam o pacote redistribuível também devem garantir que a versão ANSI do Instalador do Windows esteja instalada no Windows 98/95 e que a versão Unicode esteja instalada no Windows NT ou Windows 2000. Observe que alguns aplicativos renomeam a versão Unicode como InstMsiW.

## <a name="syntax"></a>Syntax

**Opções instmsi** 

## <a name="command-line-options"></a>Opções de linha de comando

As opções de linha de comando não são sensíveis a maiúsculas e minúsculas.



| Opção                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /q                         | Para uso por aplicativos que redistribuem o Windows instalador como parte de um aplicativo de inicialização. Nenhuma interface do usuário é apresentada ao usuário. O aplicativo de inicialização deve verificar o código de retorno para determinar se uma reinicialização é necessária para concluir a instalação do Windows Instalador.                                                                                                                                                                                                                          |
| /t                         | Usado apenas para fins de depuração.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /c:"msiinst /delayreboot"  | A opção de reinicialização atrasada. Impede que o Instmsi solicitar ao usuário uma reinicialização, mesmo que ele tenha que substituir os arquivos que estavam em uso durante a instalação. Se o Instmsi for invocado com essa opção, ele retornará ERROR SUCCESS REBOOT REQUIRED se tiver que substituir os arquivos \_ \_ que estavam em \_ uso. Se ele não tiver que substituir os arquivos que estavam em uso, ele retornará ERROR \_ SUCCESS. Disponível com o Instmsi para Windows Installer 2.0 ou posterior. Consulte a seção de comentários para obter informações adicionais sobre reinicializações atrasadas.<br/> |
| /c:"msiinst /delayrebootq" | A versão silenciosa da opção de reinicialização atrasada. Ele não apresenta nenhuma interface do usuário para o usuário. Caso contrário, o comportamento será idêntico à opção anterior. Disponível com o Instmsi para Windows Installer 2.0 ou posterior. Consulte a seção de comentários para obter informações adicionais sobre reinicializações atrasadas.<br/>                                                                                                                                                                                                                           |
| /?                         | Exibe a ajuda.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Comentários

[Inicializar aplicativos](bootstrapping.md) que usam Instmsi.exe instalar o Windows instalador com outro aplicativo pode exigir uma reinicialização adicional do sistema. Isso é potencialmente uma reinicialização extra além das reinicializações necessárias para instalar o aplicativo.

A opção de reinicialização atrasada só é recomendada para desenvolvedores de instalação que querem eliminar uma reinicialização extra causada pelo uso Instmsi.exe com um aplicativo de instalação que instala arquivos que estão em uso.

Os desenvolvedores devem fazer o seguinte em seu aplicativo de instalação para usar a opção de reinicialização atrasada. Essa opção não está disponível com versões Instmsi.exe que instalam versões do Window Installer anteriores à versão 2.0:

**Para usar a opção de reinicialização atrasada**

1.  Chame Instmsi.exe com uma das opções de linha de comando de reinicialização atrasada.
2.  Trate o retorno de ERROR \_ SUCCESS ou ERROR SUCCESS REBOOT \_ \_ \_ REQUIRED como significa êxito.
3.  Obter o caminho para a pasta que contém os binários Windows instalador recém-instalados do valor InstallerLocation em:

    **HKEY \_ Instalador \_ do** \\  \\  \\  \\ **CurrentVersion** Windows Microsoft MACHINE \\  Software LOCAL

    Esse valor é do tipo **REG \_ SZ.**

4.  De definir o diretório atual para o caminho obtido na etapa 3.
5.  Invoque o Msiexec no pacote do aplicativo e execute outro código de instalação específico para o aplicativo. Se o aplicativo de instalação usar [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), o aplicativo deverá carregar MSI.DLL do local obtido na etapa 3.
    > [!Note]  
    > Os aplicativos que chamam **LoadLibrary** no novo MSI.DLL no local obtido na etapa 3 devem garantir que uma versão mais antiga do MSI.DLL ainda não tenha sido carregada dentro do processo. Se uma versão mais antiga do MSI.DLL tiver sido carregada dentro do processo, ela deverá ser descarregada do espaço de endereço do processo antes da chamada **loadLibrary** para o novo MSI.DLL.

     

6.  Se a etapa (5) não exigir uma reinicialização e se Instmsi.exe tiver retornado ERROR SUCCESS REBOOT REQUIRED na etapa \_ \_ (1), solicitará que o usuário conclua a instalação dos binários do instalador do Windows no \_ sistema. No entanto, se ocorrer uma reinicialização na etapa (5), nenhuma etapa adicional será necessária.

Instmsi.exe está disponível no Windows [componentes do SDK para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inicialização](bootstrapping.md)
</dt> <dt>

[Inicialização de download da Internet](internet-download-bootstrapping.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis lançados](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Windows Ferramentas de desenvolvimento do instalador](windows-installer-development-tools.md)
</dt> </dl>

 

 




