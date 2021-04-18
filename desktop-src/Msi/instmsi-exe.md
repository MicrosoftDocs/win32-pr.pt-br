---
description: Instmsi.exe é o pacote redistribuível para instalar o Windows Installer&\# 160; 2.0 e versões anteriores do Windows Installer. Consulte Windows Installer redistribuíveis para os pacotes redistribuíveis para Windows Installer&\# 160; 3.0 e versões posteriores.
ms.assetid: 74ea4530-3a73-4169-b0b7-f0272229192d
title: Instmsi.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 229d748cda68731627a6af2af992e321755b5ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105792499"
---
# <a name="instmsiexe"></a>Instmsi.exe

Instmsi.exe é o pacote redistribuível para instalar o Windows Installer 2,0 e versões anteriores do Windows Installer. Consulte [Windows Installer redistribuíveis](windows-installer-redistributables.md) para os pacotes redistribuíveis para Windows Installer 3,0 e versões posteriores.

Para obter mais informações sobre qual versão do Windows Installer foi fornecida com seu sistema operacional, consulte [versões lançadas do Windows Installer](released-versions-of-windows-installer.md).

Alguns redistribuíveis não devem ser executados em determinadas versões do sistema operacional. A tabela a seguir descreve qual Instmsi é compatível em qual sistema operacional.



| Se Instmsi.exe instalar esta versão do Windows Installer | Instmsi.exe pode ser executado nesses sistemas operacionais                    | Instmsi.exe não deve ser executado nesses sistemas operacionais                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Windows Installer versão 1,0                                 | Windows 95, Windows 98, Windows NT 4.0 + SP3                           | Windows me, Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008 |
| Windows Installer versão 1,1                                 | Windows 95, Windows 98, Windows NT 4.0 + SP3                           | Windows me, Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008 |
| Windows Installer versão 1,2                                 | Windows 95, Windows 98, Windows me, Windows NT 4.0 + SP3               | Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008             |
| Windows Installer versão 2,0                                 | Windows 95, Windows 98, Windows me, Windows NT 4.0 + SP6, Windows 2000 | Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008                           |



 

Por exemplo, um aplicativo que redistribui Windows Installer versão 1,1 deve verificar se o sistema operacional é o Windows NT 4,0 SP3 ou o Windows 98/95 antes de executar o pacote redistribuível. Os aplicativos que usam o pacote redistribuível também devem garantir que a versão ANSI do Windows Installer esteja instalada no Windows 98/95 e que a versão Unicode esteja instalada no Windows NT ou no Windows 2000. Observe que alguns aplicativos renomeam a versão Unicode para InstMsiW.

## <a name="syntax"></a>Syntax

 *Opções* Instmsi

## <a name="command-line-options"></a>Opções de linha de comando

As opções de linha de comando não diferenciam maiúsculas de minúsculas.



| Opção                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /q                         | Para uso por aplicativos que redistribuem o Windows Installer como parte de um aplicativo de inicialização. Nenhuma IU é apresentada ao usuário. O aplicativo de inicialização deve verificar o código de retorno para determinar se uma reinicialização é necessária para concluir a instalação do Windows Installer.                                                                                                                                                                                                                          |
| /t                         | Usado somente para fins de depuração.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /c: "msiinst/delayreboot"  | A opção de reinicialização atrasada. Impede que o Instmsi solicite uma reinicialização ao usuário, mesmo que tenha que substituir arquivos que estavam em uso durante a instalação. Se Instmsi for invocado com essa opção, retornará um erro com \_ êxito \_ reinicialização \_ necessária se tiver que substituir os arquivos que estavam em uso. Se não tiver de substituir os arquivos que estavam em uso, ele retornará êxito de erro \_ . Disponível com o Instmsi para Windows Installer 2,0 ou posterior. Consulte a seção comentários para obter informações adicionais sobre reinicializações atrasadas.<br/> |
| /c: "msiinst/delayrebootq" | A versão silenciosa da opção de reinicialização atrasada. Ele não apresenta nenhuma interface de usuário para o usuário. Caso contrário, o comportamento será idêntico à opção anterior. Disponível com o Instmsi para Windows Installer 2,0 ou posterior. Consulte a seção comentários para obter informações adicionais sobre reinicializações atrasadas.<br/>                                                                                                                                                                                                                           |
| /?                         | Exibe a ajuda.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Comentários

Os aplicativos de [inicialização](bootstrapping.md) que usam o Instmsi.exe para instalar o Windows Installer com outro aplicativo podem exigir uma reinicialização extra do sistema. Isso é potencialmente uma reinicialização extra além de quaisquer reinicializações necessárias para instalar o aplicativo.

A opção de reinicialização atrasada só é recomendada para os desenvolvedores de instalação que desejam eliminar uma reinicialização extra causada pelo uso de Instmsi.exe com um aplicativo de instalação que instala arquivos que estão em uso.

Os desenvolvedores devem fazer o seguinte em seu aplicativo de instalação para usar a opção de reinicialização atrasada. Essa opção não está disponível com Instmsi.exe versões que instalam versões anteriores à versão 2,0 do Windows Installer:

**Para usar a opção de reinicialização atrasada**

1.  Chame Instmsi.exe com uma das opções de linha de comando de reinicialização atrasada.
2.  Trate o retorno de êxito de erro \_ ou \_ êxito na \_ reinicialização de erro \_ necessária, como significado do sucesso.
3.  Obtenha o caminho para a pasta que contém os binários de Windows Installer recentemente instalados do valor InstallerLocation em:

    **HKEY \_ \_** Instalador de \\ **software** do computador local \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ 

    Esse valor é do tipo **reg \_ sz**.

4.  Defina o diretório atual para o caminho obtido na etapa 3.
5.  Invoque o msiexec no pacote do aplicativo e execute outro código de instalação específico para o aplicativo. Se o aplicativo de instalação usar [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), o aplicativo deverá carregar MSI.DLL do local obtido na etapa 3.
    > [!Note]  
    > Os aplicativos que chamam **LoadLibrary** no novo MSI.DLL no local obtido na etapa 3 devem garantir que uma versão mais antiga do MSI.DLL ainda não tenha sido carregada dentro do processo. Se uma versão mais antiga do MSI.DLL tiver sido carregada no processo, ela deverá ser descarregada do espaço de endereço do processo antes da chamada **LoadLibrary** para o novo MSI.DLL.

     

6.  Se Step (5) não exigir uma reinicialização e se Instmsi.exe tiver retornado erro de \_ \_ reinicialização de êxito \_ necessário na etapa (1), solicite ao usuário uma reinicialização para concluir a configuração dos binários de Windows Installer no sistema. No entanto, se uma reinicialização ocorrer na etapa (5), nenhuma etapa adicional será necessária.

Instmsi.exe está disponível nos [componentes de SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inicialização](bootstrapping.md)
</dt> <dt>

[Inicialização de download da Internet](internet-download-bootstrapping.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Ferramentas de desenvolvimento Windows Installer](windows-installer-development-tools.md)
</dt> </dl>

 

 




