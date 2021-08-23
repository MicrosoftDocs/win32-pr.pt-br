---
description: O Windows instalador redistribuível é um pacote de atualização de software.
ms.assetid: 8491dfa6-b9be-4e37-8a61-a405c8eb0ab0
title: Redistribuíveis do Windows Installer
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: 831abe9a19f8b2d4999229b1d40e701c5869aa79e6dda9f0933ab8117656652b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526696"
---
# <a name="windows-installer-redistributables"></a>Redistribuíveis do Windows Installer

Windows O instalador 4.5 e anterior está disponível como um pacote de atualização de software redistribuível. Consulte a seção Versões lançadas [do Windows Instalador](released-versions-of-windows-installer.md) para determinar quais produtos foram enviados versões do Windows Instalador. O pacote de atualização redistribuível para uma versão é disponibilizado após o lançamento do produto que é disponibilizado com uma versão Windows Installer específica.

> [!NOTE]
> Não há nenhum redistribuível para Windows Installer 5.0. Esta versão está incluída com o sistema operacional no Windows 7, Windows Server 2008 R2 e versões posteriores de cliente e servidor (incluindo Windows 10).

## <a name="obtaining-the-windows-installer-redistributable-45-and-earlier"></a>Obtendo o Windows Instalador Redistribuível (4.5 e versões anteriores)

-   Você pode encontrar todos os redistribuíveis Windows instalador disponíveis no Centro [de Download da Microsoft.](https://www.microsoft.com/Downloads/)
-   O download do [pacote redistribuível Windows Installer 4.5](https://support.microsoft.com/kb/942288) está disponível em: https://go.microsoft.com/fwlink/p/?LinkID=101159 .
-   O nome do redistribuível que instala o Windows Installer 4.5 em computadores baseados em x86 que executam o Windows Vista, o Windows Vista com Service Pack 1 (SP1) e o Windows Server 2008 é Windows6.0-KB942288-v2-x86.MSU.
-   O nome do redistribuível que instala o Windows Installer 4.5 em computadores baseados em x64 que executam o Windows Vista, o Windows Vista com SP1 e o Windows Server 2008 é Windows6.0-KB942288-v2-x64.MSU.
-   O nome do redistribuível que instala o Windows Installer 4.5 em computadores do Itanium-Based Systems que executam o Windows Vista, o Windows Vista com SP1 e o Windows Server 2008 é Windows6.0-KB942288-v2-ia64.MSU.
-   O nome do redistribuível que instala o Windows Installer 4.5 em computadores baseados em x86 que executam o Windows XP com o Service Pack 2 (SP2) e o Windows XP com Service Pack 3 (SP3) é WindowsXP-KB942288-v3-x86.exe.
-   O nome do redistribuível que instala o Windows Installer 4.5 em computadores baseados em x86 que executam o Windows Server 2003 com o Service Pack 1 (SP1) e o Windows Server 2003 com o Service Pack 2 (SP2) é WindowsServer2003-KB942288-v4-x86.exe.
-   O nome do redistribuível que instala o Windows Installer 4.5 em computadores baseados em x64 que executam o Windows Server 2003 com SP1 e Windows Server 2003 com SP2 é WindowsServer2003-KB942288-v4-x64.exe.
-   O nome do redistribuível que instala o Windows Installer 4.5 em computadores do Itanium-Based Systems que executam o Windows Server 2003 com SP1 e Windows Server 2003 com SP2 é WindowsServer2003-KB942288-v4-ia64.exe.
-   Não há nenhum redistribuível que instale Windows Installer 4.0. Esta versão do instalador Windows é acompanhada com Windows Vista.
-   O nome do redistribuível que instala o Windows 3.1 é WindowsInstaller-KB893803-v2-x86.exe. O download do [pacote Windows Instalador 3.1 Redistribuível (v2)](https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c) está disponível em: https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c .
    > [!Note]  
    > Se você atualizou para o Windows Installer 3.1 instalando o Windows Server 2003 com SP1 ou uma versão anterior desse redistribuível, talvez também seja necessário instalar a Atualização para [o Service Pack 1 do Windows Server 2003 (KB898715)](https://www.microsoft.com/downloads/details.aspx?FamilyID=8b4e6b93-1886-4d47-a18d-35581c42eca0) para obter todas as atualizações disponíveis no [Instalador do Windows 3.1 Redistribuível (v2)](https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c).

     

-   O redistribuível que instala Windows Instalador 3.0 é WindowsInstaller-KB884016-v2-x86.exe. O download do [Windows Instalador 3.0 Redistribuível](https://www.microsoft.com/downloads/details.aspx?FamilyID=5fbc5470-b259-4733-a914-a956122e08e8) está disponível em: https://www.microsoft.com/downloads/details.aspx?FamilyID=5fbc5470-b259-4733-a914-a956122e08e8 .
-   O Windows Instalador 2.0 usou uma convenção de nomenba anterior para o redistribuível: [Instmsi.exe](instmsi-exe.md). O redistribuível para instalar ou atualizar para o Windows Installer 2.0 no Windows 2000 não deve ser usado para instalar ou atualizar o Windows Installer 2.0 no Windows Server 2003 e Windows XP.

    O download do [Windows 2.0 Redistribuível para Windows NT 4.0 e Windows 2000 está](https://www.microsoft.com/downloads/details.aspx?FamilyID=4b6140f9-2d36-4977-8fa1-6f8a0f5dca8f) disponível em https://www.microsoft.com/downloads/details.aspx?FamilyID=4b6140f9-2d36-4977-8fa1-6f8a0f5dca8f .

## <a name="installing-the-windows-installer-redistributable-45-and-earlier"></a>Instalando o Windows Instalador Redistribuível do Windows (4.5 e versões anteriores)

O Windows Instalador do Windows 4.5 é fornecido para sistemas operacionais Windows Vista e Windows Server 2008 como um arquivo .msu e deve ser instalado usando o instalador autônomo de atualização do [Windows](https://support.microsoft.com/kb/934307/) (Wusa.exe).)

Os sistemas operacionais Windows Installer 4.5 para sistemas operacionais Windows XP e Windows Server 2003 podem ser instalados usando a sintaxe e as opções de linha de comando a seguir.

Os Windows Instalador 3.1 e Windows Instalador 3.0 podem ser instalados usando a sintaxe e as opções de linha de comando a seguir.

### <a name="syntax"></a>Syntax

Use a sintaxe a seguir para instalar os redistribuíveis do Windows Installer 4.5 no Windows XP e Windows Server 2003.

```CMD
<Name of the Redistributable>\[<options>\]*
```

### <a name="command-line-options"></a>Opções de Linha de Comando

Os Windows pacotes de atualização de software redistribuíveis do instalador usam as seguintes opções de linha de comando que não são sensíveis a maiúsculas e minúsculas.



| Opção     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /norestart | Impede que o pacote redistribuível solicita que o usuário reinicialize mesmo que ele tenha que substituir os arquivos que estavam em uso durante a instalação. Se o pacote de atualização for invocado com essa opção, ele retornará **ERROR \_ SUCCESS REBOOT \_ \_ REQUIRED** se tiver que substituir os arquivos que estavam em uso.<br/> Se ele não tiver que substituir os arquivos que estavam em uso, ele **retornará ERROR \_ SUCCESS**. Consulte a seção de comentários para obter informações adicionais sobre reinicializações atrasadas.<br/> |
| /quiet     | Para uso por aplicativos que redistribuem o Windows instalador como parte de um aplicativo de inicialização. Uma interface do usuário não é apresentada ao usuário. O aplicativo de inicialização deve verificar o código de retorno para determinar se uma reinicialização é necessária para concluir a instalação do Windows Instalador.<br/>                                                                                                                                                |
| /help      | Exibe ajuda em todas as opções disponíveis.                                                                                                                                                                                                                                                                                                                                                                                                                                     |

### <a name="delayed-restart-on-windows-vista-and-windows-server-2008"></a>Reinicialização atrasada no Windows Vista e Windows Server 2008

A opção de linha de comando /norestart impede wusa.exe reiniciar o computador. No entanto, se um arquivo que está sendo atualizado pelo pacote MSU estiver em uso, o pacote não será aplicado ao computador até que o usuário reinicie o computador. Isso significa que os aplicativos que usam o Windows Installer 4.5 redistribuível para o Windows Vista e o Windows Server 2008 não podem usar a funcionalidade do instalador do Windows 4.5 até que o computador seja reiniciado.

### <a name="delayed-restart-on-windows-xp-and-windows-server-2003"></a>Reinicialização atrasada no Windows XP e Windows Server 2003

É recomendável que o serviço Windows instalador seja interrompido ao usar o pacote de atualização. Quando o pacote é executado no modo de interface do usuário completo, ele detecta se o serviço Windows Instalador está em execução e solicita que o usuário pare o serviço. Se o usuário continuar sem interromper o serviço, a atualização substituirá Windows Instalador.

[Inicializar aplicativos](bootstrapping.md) que usam o pacote redistribuível para instalar o instalador do Windows com outro aplicativo pode exigir uma reinicialização adicional do sistema, além das reinicializações necessárias para instalar o aplicativo. A opção de reinicialização atrasada só é recomendada para casos em que é necessário eliminar uma reinicialização extra causada pela instalação de arquivos que estão em uso. Os desenvolvedores devem fazer o seguinte em seu aplicativo de instalação para usar a opção de reinicialização atrasada.

-   Chame o pacote redistribuível com a opção de linha de comando /norestart.
-   Trate o retorno de **ERROR \_ SUCCESS ou** ERROR SUCCESS REBOOT **\_ \_ \_ REQUIRED** como significa êxito.
-   Invoque o Msiexec no pacote do aplicativo e execute outro código de instalação específico para o aplicativo. Se o aplicativo de instalação usar [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), o aplicativo deverá carregar MSI.DLL do diretório do sistema. Se nenhuma reinicialização ocorrer e se o redistribuível tiver retornado **ERROR \_ SUCCESS REBOOT \_ \_ REQUIRED**, solicitará que o usuário conclua a instalação dos binários Windows Installer. Se ocorrer uma reinicialização, nenhuma etapa adicional será necessária.
    > [!Note]  
    > Os aplicativos que chamam [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) no novo MSI.DLL após o pacote redistribuível retornarem êxito devem garantir que uma versão mais antiga do MSI.DLL ainda não tenha sido carregada dentro do processo. Se uma versão mais antiga do MSI.DLL foi carregada, ela deve ser descarregada do espaço de endereço do processo antes de chamar **LoadLibrary** para o novo MSI.DLL.

     

Para obter mais informações, [consulte Windows Inicialização do Instalador do](windows-installer-bootstrapping.md).

 

 
