---
description: O Windows Installer redistribuível é um pacote de atualização de software.
ms.assetid: 8491dfa6-b9be-4e37-8a61-a405c8eb0ab0
title: Redistribuíveis do Windows Installer
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: 9fc175a96ae1d2daed9798981b0dbe679505975e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748751"
---
# <a name="windows-installer-redistributables"></a>Redistribuíveis do Windows Installer

Windows Installer 4,5 e anterior estão disponíveis como um pacote de atualização de software redistribuível. Consulte a seção [versões lançadas do Windows Installer](released-versions-of-windows-installer.md) para determinar quais produtos foram fornecidos com versões do Windows Installer. O pacote de atualização redistribuível para uma versão é disponibilizado após o lançamento do produto fornecido com uma versão específica do Windows Installer.

> [!NOTE]
> Não há pacotes redistribuíveis para o Windows Installer 5,0. Essa versão está incluída no sistema operacional no Windows 7, no Windows Server 2008 R2 e em versões de cliente e servidor posteriores (incluindo o Windows 10).

## <a name="obtaining-the-windows-installer-redistributable-45-and-earlier"></a>Obtendo o Windows Installer redistribuível (4,5 e anterior)

-   Você pode encontrar todos os redistribuíveis Windows Installer disponíveis no [centro de download da Microsoft](https://www.microsoft.com/Downloads/).
-   O download para o [pacote redistribuível do Windows Installer 4,5](https://support.microsoft.com/kb/942288) está disponível em: https://go.microsoft.com/fwlink/p/?LinkID=101159 .
-   O nome do redistribuível que instala o Windows Installer 4,5 em computadores baseados em x86 que executam o Windows Vista, o Windows Vista com Service Pack 1 (SP1) e o Windows Server 2008 é o Windows 6.0-KB942288-v2-x86. MSU.
-   O nome do redistribuível que instala o Windows Installer 4,5 em computadores baseados em x64 que executam o Windows Vista, o Windows Vista com SP1 e o Windows Server 2008 é o Windows 6.0-KB942288-v2-x64. MSU.
-   O nome do redistribuível que instala o Windows Installer 4,5 em computadores Itanium-Based sistemas que executam o Windows Vista, o Windows Vista com SP1 e o Windows Server 2008 é o Windows 6.0-KB942288-v2-ia64. MSU.
-   O nome do redistribuível que instala o Windows Installer 4,5 em computadores baseados em x86 que executam o Windows XP com Service Pack 2 (SP2) e o Windows XP com Service Pack 3 (SP3) é WindowsXP-KB942288-v3-x86.exe.
-   O nome do redistribuível que instala o Windows Installer 4,5 em computadores baseados em x86 que executam o Windows Server 2003 com Service Pack 1 (SP1) e o Windows Server 2003 com Service Pack 2 (SP2) é WindowsServer2003-KB942288-v4-x86.exe.
-   O nome do redistribuível que instala o Windows Installer 4,5 em computadores baseados em x64 que executam o Windows Server 2003 com SP1 e o Windows Server 2003 com SP2 é WindowsServer2003-KB942288-v4-x64.exe.
-   O nome do redistribuível que instala o Windows Installer 4,5 em computadores Itanium-Based sistemas que executam o Windows Server 2003 com SP1 e o Windows Server 2003 com SP2 é WindowsServer2003-KB942288-v4-ia64.exe.
-   Não há redistribuível que instale o Windows Installer 4,0. Esta versão do Windows Installer é fornecida com o Windows Vista.
-   O nome do redistribuível que instala o Windows Installer 3,1 é WindowsInstaller-KB893803-v2-x86.exe. O download para o pacote [redistribuível do Windows Installer 3,1 (v2)](https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c) está disponível em: https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c .
    > [!Note]  
    > Se você atualizou para o Windows Installer 3,1 Instalando o Windows Server 2003 com SP1 ou uma versão anterior desse redistribuível, talvez também precise instalar a [atualização do Windows server 2003 Service Pack 1 (KB898715)](https://www.microsoft.com/downloads/details.aspx?FamilyID=8b4e6b93-1886-4d47-a18d-35581c42eca0) para obter todas as atualizações disponíveis em [Windows Installer 3,1 redistribuível (v2)](https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c).

     

-   O redistribuível que instala o Windows Installer 3,0 é WindowsInstaller-KB884016-v2-x86.exe. O download para o [Windows Installer 3,0 redistribuível](https://www.microsoft.com/downloads/details.aspx?FamilyID=5fbc5470-b259-4733-a914-a956122e08e8) está disponível em: https://www.microsoft.com/downloads/details.aspx?FamilyID=5fbc5470-b259-4733-a914-a956122e08e8 .
-   O Windows Installer 2,0 usou uma Convenção de Nomenclatura anterior para o redistribuível: [Instmsi.exe](instmsi-exe.md). Os pacotes redistribuíveis para instalação ou atualização para o Windows Installer 2,0 no Windows 2000 não devem ser usados para instalar ou atualizar Windows Installer 2,0 no Windows Server 2003 e no Windows XP.

    O download para o [Windows Installer 2,0 redistribuível para Windows NT 4,0 e windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=4b6140f9-2d36-4977-8fa1-6f8a0f5dca8f) está disponível em https://www.microsoft.com/downloads/details.aspx?FamilyID=4b6140f9-2d36-4977-8fa1-6f8a0f5dca8f .

## <a name="installing-the-windows-installer-redistributable-45-and-earlier"></a>Instalando o Windows Installer redistribuível (4,5 e anterior)

O Windows Installer 4,5 resdistributable é fornecido para sistemas operacionais Windows Vista e Windows Server 2008 como um arquivo. msu e deve ser instalado usando o [instalador Windows Update](https://support.microsoft.com/kb/934307/) autônomo (Wusa.exe).

Os sistemas operacionais Windows Installer 4,5 redistribuíveis para Windows XP e Windows Server 2003 podem ser instalados usando a seguinte sintaxe de linha de comando e opções.

Os redistribuíveis Windows Installer 3,1 e Windows Installer 3,0 podem ser instalados usando a seguinte sintaxe de linha de comando e opções.

### <a name="syntax"></a>Syntax

Use a sintaxe a seguir para instalar os pacotes redistribuíveis para o Windows Installer 4,5 no Windows XP e no Windows Server 2003.

```CMD
<Name of the Redistributable>\[<options>\]*
```

### <a name="command-line-options"></a>Opções de Linha de Comando

Os pacotes de atualização de software Windows Installer redistribuíveis usam as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas.



| Opção     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /norestart | Impede que o pacote redistribuível solicite ao usuário a reinicialização, mesmo que precise substituir os arquivos que estavam em uso durante a instalação. Se o pacote de atualização for invocado com essa opção, retornará um **erro com \_ êxito \_ reinicialização \_ necessária** se tiver que substituir os arquivos que estavam em uso.<br/> Se não tiver de substituir os arquivos que estavam em uso, ele retornará **\_ êxito de erro**. Consulte a seção comentários para obter informações adicionais sobre reinicializações atrasadas.<br/> |
| /quiet     | Para uso por aplicativos que redistribuem o Windows Installer como parte de um aplicativo de inicialização. Uma interface do usuário (IU) não é apresentada ao usuário. O aplicativo de inicialização deve verificar o código de retorno para determinar se uma reinicialização é necessária para concluir a instalação do Windows Installer.<br/>                                                                                                                                                |
| /help      | Exibe a ajuda em todas as opções disponíveis.                                                                                                                                                                                                                                                                                                                                                                                                                                     |

### <a name="delayed-restart-on-windows-vista-and-windows-server-2008"></a>Reinicialização atrasada no Windows Vista e no Windows Server 2008

A opção de linha de comando/norestart impede que wusa.exe reinicie o computador. No entanto, se um arquivo que está sendo atualizado pelo pacote MSU estiver em uso, o pacote não será aplicado ao computador até que o usuário reinicie o computador. Isso significa que os aplicativos que usam o Windows Installer 4,5 redistribuível para Windows Vista e Windows Server 2008 não podem usar a funcionalidade Windows Installer 4,5 até que o computador seja reiniciado.

### <a name="delayed-restart-on-windows-xp-and-windows-server-2003"></a>Reinicialização atrasada no Windows XP e no Windows Server 2003

É recomendável que o serviço Windows Installer seja interrompido ao usar o pacote de atualização. Quando o pacote é executado no modo de interface do usuário completo, ele detecta se o serviço de Windows Installer está em execução e solicita que o usuário interrompa o serviço. Se o usuário continuar sem parar o serviço, a atualização substituirá Windows Installer.

Os aplicativos de [inicialização](bootstrapping.md) que usam o pacote redistribuível para instalar o Windows Installer com outro aplicativo podem exigir uma reinicialização extra do sistema, além de reinicializações necessárias para instalar o aplicativo. A opção de reinicialização atrasada só é recomendada para casos em que é necessário eliminar uma reinicialização extra causada pela instalação de arquivos que estão em uso. Os desenvolvedores devem fazer o seguinte em seu aplicativo de instalação para usar a opção de reinicialização atrasada.

-   Chame o pacote redistribuível com a opção de linha de comando/norestart.
-   Trate o retorno de êxito **de \_ erro** ou **\_ êxito na \_ reinicialização \_ de erro necessária** , como significado do sucesso.
-   Invoque o msiexec no pacote do aplicativo e execute outro código de instalação específico para o aplicativo. Se o aplicativo de instalação usar o [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), o aplicativo deverá carregar MSI.DLL do diretório do sistema. Se nenhuma reinicialização ocorrer e se o redistribuível retornou uma **\_ \_ reinicialização \_ de êxito de erro necessária**, solicite ao usuário uma reinicialização para concluir a configuração dos binários de Windows Installer. Se ocorrer uma reinicialização, nenhuma etapa adicional será necessária.
    > [!Note]  
    > Os aplicativos que chamam [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) no novo MSI.DLL após o pacote redistribuível retornam êxito devem garantir que uma versão mais antiga do MSI.DLL ainda não tenha sido carregada dentro do processo. Se uma versão mais antiga do MSI.DLL tiver sido carregada, ela deverá ser descarregada do espaço de endereço do processo antes de chamar **LoadLibrary** para o novo MSI.DLL.

     

Para obter mais informações, consulte [inicialização de Windows Installer](windows-installer-bootstrapping.md).

 

 
