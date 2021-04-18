---
description: Atualmente, cada instalação que tenta usar o Windows Installer começa verificando se o instalador está presente no computador do usuário e, se não estiver presente, se o usuário e o computador estão prontos para instalar Windows Installer.
ms.assetid: a5174284-2a8c-4510-accf-641fda5be98d
title: Inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff743acbcd2dfc81b0e912e5be84c363f34614ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751208"
---
# <a name="bootstrapping"></a>Inicialização

Atualmente, cada instalação que tenta usar o Windows Installer começa verificando se o instalador está presente no computador do usuário e, se não estiver presente, se o usuário e o computador estão prontos para instalar Windows Installer. Um aplicativo de instalação [Instmsi.exe](instmsi-exe.md) está disponível com o SDK do Windows Installer que contém toda a lógica e funcionalidade para instalar o Windows Installer. No entanto, um aplicativo de inicialização deve gerenciar essa instalação.

O aplicativo de inicialização deve primeiro verificar se Windows Installer está instalado no momento. Os aplicativos podem obter a versão do Windows Installer instalada atualmente usando [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc). Se o Windows Installer não estiver instalado no momento, o aplicativo de inicialização deverá consultar o sistema operacional para determinar qual versão do Instmsi.exe é necessária. Depois que a instalação do Windows Installer foi iniciada, o aplicativo de inicialização deve manipular códigos de retorno do aplicativo Instmsi.exe e lidar com qualquer reinicialização incorrida durante a instalação do Windows Installer. Para obter mais informações, consulte [determinando a versão de Windows Installer](determining-the-windows-installer-version.md)

O exemplo a seguir demonstra como o aplicativo de instalação que instala o Microsoft Office 2000 verifica o sistema do usuário e configura a instalação do Windows Installer. Este exemplo foi escrito especificamente para instalar o Office 2000 e deve ser usado apenas como referência geral.

Quando um usuário insere um CD-ROM do Office 2000 em seu computador, Setup.exe tenta iniciar o modo de manutenção, o aplicativo de instalação ou não faz nada, de acordo com as necessidades do usuário. A seção a seguir descreve como o aplicativo de instalação do Office 2000, chamado Setup.exe, qualifica o usuário e seu computador, constrói uma linha de comando e instala Windows Installer usando o aplicativo Msiexec.exe.

## <a name="how-setupexe-bootstraps-the-windows-installer-when-installing-office-2000"></a>Como o Setup.exe Inicializa o Windows Installer ao instalar o Office 2000

1.  O usuário insere um CD-ROM do Office 2000 em seu computador. O sistema operacional Windows inicia Setup.exe usando o comutador/autorun e o arquivo autorun. inf. O arquivo autorun. inf é encontrado na raiz do CD-ROM do Office 2000 e contém as seguintes seções:

    \[Execução\]

     

    \[Recursos do Office\]

     

    \[Informações do produto\]

     

    \[Service Pack \] .

    A \[ \] seção autorun contém uma linha de comando que executa o aplicativo Setup.exe, executa o ícone usado para exibir o disco e contém informações para adicionar uma opção "instalar" e uma opção "configurar" no menu de contexto do CD-ROM.

    A \[ seção recursos do Office \] contém uma lista de recursos e pares de nome de recurso.

    A \[ seção informações do produto \] especifica o nome e a versão do aplicativo.

    A \[ seção Service Pack \] permite que um administrador de rede defina o nível mínimo necessário de Service Pack. O administrador de rede pode usar esta seção para criar o texto de uma mensagem de alerta exibida se o sistema operacional local não tiver o service pack necessário.

    Veja a seguir um exemplo de Autorun. inf.

    ``` syntax
    [autorun] 
    OPEN=setup.EXE /AUTORUN /KEY:Software\Microsoft\Office\9.0\Common\General\InstallProductID
    ICON=setup.EXE,1
    shell\configure=&Configure
    shell\configure\command=setup.EXE
    shell\install=&Install
    shell\install\command=setup.EXE
    [OfficeFeatures]
    Feature1=ACCESSFiles
    Feature2=OfficeFiles
    Feature3=WORDFiles
    Feature4=EXCELFiles
    Feature5=PPTFiles
    [ProductInformation]
    DisplayName=Microsoft Office 9
    Version=9.0
    ProductCode={product guid}
    [ServicePack]
    MessageText="The operating system does not have a required service pack. Please download and install this from www.microsoft.com."
    SPLevel=3
    ```

2.  O aplicativo Setup.exe verifica o \_ mutex MsiPromptForCD. Windows Installer cria esse mutex quando solicita que o usuário insira o CD-ROM. A presença do mutex indica que Windows Installer está executando uma instalação que solicitou o CD-ROM do Office 2000. Nesse caso, o aplicativo Setup.exe é fechado imediatamente e permite que a instalação do Office 2000 continue. Se o mutex estiver ausente, o aplicativo Setup.exe continuará na etapa 3, em que uma chave do registro é avaliada para determinar se o Office 2000 está instalado.
3.  O aplicativo Setup.exe verifica a presença da chave do registro Office9:

    **HKCU/Software/Microsoft/Office/9.0/comum/geral/InstallProductID**

    Se essa chave do registro não existir, o aplicativo Setup.exe continuará na etapa 6, em que o sistema operacional é verificado para determinar se ele é qualificado para a instalação do Office 2000.

4.  Se a chave do registro do Office 2000 existir, o aplicativo Setup.exe verificará o estado de instalação atual chamando [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea). Um estado de retorno do padrão InstallState \_ indica que o office 2000 já está instalado e o Setup.exe aplicativo continua na etapa 5, em que o office 2000 é verificado para execução da origem.

    Se o Office 2000 não estiver instalado, o aplicativo Setup.exe continuará na etapa 6, em que o sistema operacional é verificado para determinar se ele é qualificado para a instalação do Office 2000.

5.  O aplicativo Setup.exe chama [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) para cada um dos recursos na seção **\[ OfficeFeatures \]** do arquivo autorun. inf. Se qualquer um desses recursos retornar \_ a origem InstallState, isso indica que o recurso está sendo executado a partir da origem e o aplicativo Setup.exe é fechado imediatamente.

    Se nenhum dos recursos retornar a origem INSTALLstate \_ , o aplicativo Setup.exe iniciará o aplicativo instalador, Msiexec.exe e apresentará o Windows Installer modo de manutenção antes de sair.

6.  O aplicativo Setup.exe determina se o sistema operacional é qualificado para uma instalação do Office 2000. O Windows XP é necessário para instalar o Office 2000. Se o sistema operacional exigir uma atualização service pack para se qualificar para o Office 2000, o aplicativo Setup.exe exibirá o texto especificado no arquivo autorun. inf. Se o sistema operacional não estiver qualificado para o Office 2000 ou uma atualização do Office 2000, o aplicativo Setup.exe exibirá uma mensagem que impede que o usuário continue.

    Se o sistema operacional for qualificado para o Office 2000, o aplicativo Setup.exe continuará na etapa 7, que determina se o Windows Installer está instalado no computador do usuário.

7.  Se Windows Installer existir no computador do usuário, o aplicativo Setup.exe iniciará o aplicativo Msiexec.exe e passará o arquivo. msi do Office 2000 para ele.

    Se o Windows Installer não estiver instalado no computador local, o aplicativo Setup.exe continuará na etapa 8, que determina se o sistema operacional é qualificado para ter Windows Installer instalado.

8.  Se o computador local estiver qualificado para ter Windows Installer instalado, o aplicativo Setup.exe executará a versão correta do aplicativo Instmsi.exe Installer para a plataforma. Setup.exe pode passar a opção de linha de comando "/q" para suprimir a interface do usuário e impedir que o usuário altere as opções de configuração de instalação.
9.  O aplicativo Setup.exe carrega o arquivo de Msi.dll recém-instalado e executa uma chamada para a função [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) para instalar o aplicativo do usuário.

## <a name="setupexe-command-line-parameters"></a>Setup.exe parâmetros de linha de comando

O aplicativo Setup.exe permite que administradores e usuários passem opções de linha de comando para o aplicativo Msiexec.exe. Para obter mais informações, consulte [Opções de linha de comando](command-line-options.md). A tabela a seguir lista as opções de comando que podem ser usadas com Setup.exe.



| Opção                       | Uso                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /autorun                     | setup.exe/autorun                                                                                                                           | Executa o autorun. inf descrito acima.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| /a                           | setup.exe /a                                                                                                                                 | Inicia uma instalação administrativa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| /j                           | \[\| \] *pacote* u m ou <br/> \[pacote de u \| m \]  /T de *lista de transformação*<br/> ou <br/> \[\| \] *pacote* u m/g *LanguageID*<br/> | Anuncia um produto. Essa opção ignora todos os valores de propriedade inseridos na linha de comando. u anunciar para o usuário atual.<br/> m anunciar para todos os usuários do computador.<br/> identificador de idioma g<br/> t aplica a transformação ao pacote anunciado.<br/>                                                                                                                                                                                                                        |
| /I                           | setup.exe/I Office9.msi/t ProgramMgmt. MST                                                                                                  | Especifica o arquivo. msi que Setup.exe será instalado. Se a opção/I não for incluída, Setup.exe usará o arquivo Office9.msi.                                                                                                                                                                                                                                                                                                                                                                                 |
| /o< = *valor* da propriedade> | setup.exe/o CDKEY = 111111-1111                                                                                                               | Define as propriedades no arquivo. msi. Setup.exe passa essas para msiexec como escrito.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| /q                           | setup.exe/q                                                                                                                                 | Defina o nível da interface do usuário na instalação. /q sem interface do usuário (/qn para msiexec.)/QB Basic UI<br/> interface do usuário reduzida do/QR.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| opção\#                         | setup.exe/M4                                                                                                                                | Dá suporte a várias licenças de acordo com os contratos selecionados. Essa propriedade é usada pela ação personalizada de verificação de licença para gravar o certificado LV. A opção/m deve ser seguida pelo número de desbloqueios permitidos. O valor especificado pela opção/m deve ser definido como a propriedade "M" no arquivo de Office9.msi. Se nenhum valor for especificado, mas a opção/m for usada com a instalação, o valor de 0 deverá ser definido. A opção/m é necessária para dar suporte a clientes selecionados usando um CD ou uma rede. |
| /Settings                    | setup.exe/Settings mysettings.ini                                                                                                           | Permite que os administradores especifiquem um arquivo. ini contendo todas as configurações personalizadas a serem passadas durante a instalação do Office 2000. Consulte a descrição do arquivo. ini abaixo.                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="using-an-ini-file"></a>Usando um arquivo. ini

A criação de um arquivo de inicialização pode ser mais fácil do que criar uma linha de comando longa. Usando a opção/Settings, o aplicativo Setup.exe lê o arquivo. ini especificado e constrói uma linha de comando para passar para o aplicativo Msiexec.exe. Somente as propriedades com suporte na linha de comando têm suporte no arquivo. ini. Se uma propriedade ou um valor for encontrado no arquivo. ini e na linha de comando, as configurações de linha de comando substituirão as configurações do arquivo. ini.

O formato do arquivo. ini é:

\[MSI\]

 

\[MST\]

 

\[options\]

 

\[Vídeo\]

A \[ \] seção msi do arquivo. ini especifica o caminho para o pacote de instalação da instalação do. Isso corresponde à opção/I na linha de comando.

A \[ \] seção MST do arquivo. ini especifica o caminho para as transformações usadas com essa instalação. Isso corresponde à opção/j na linha de comando. Várias transformações são indicadas em uma linha diferente, usando MST1 MST (N). Quando analisada na linha de comando, a lista no arquivo. ini é transformada da esquerda para a direita. Observe que o número associado ao título MST (N) está presente apenas para manter identificadores exclusivos e não tem um significado programático.

A \[ seção de opções \] permite que os administradores de rede definam e substituam as propriedades nos arquivos. msi ou. MST. As opções definidas no arquivo. ini são adicionadas à linha de comando usando a opção/o. Cada opção na seção Option deve ter um nome de propriedade e um valor.

A \[ \] seção exibição é usada para definir o nível de interface do usuário usado durante a instalação. Isso corresponde à opção/q na linha de comando. Os valores válidos são None, Basic, Reduced e Full.

Arquivo. ini de exemplo

\[MSI\]

 

MSI = \\ \\ sourceshare \\ office2000 \\Office2000.msi

 

\[MST\]

 

MST1 = \\ \\ sourceshare \\ office2000 \\ trns1. MST

 

MST2 = \\ \\ sourceshare \\ office2000 \\ trns2. MST

 

\[Opções\]

 

PUBLICproperty = seu valor

\[Vídeo\]

 

Exibir = nenhum

 

