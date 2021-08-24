---
description: Atualmente, cada instalação que tenta usar o instalador do Windows começa verificando se o instalador está presente no computador do usuário e se ele não está presente, se o usuário e o computador estão prontos para instalar o Windows Installer.
ms.assetid: a5174284-2a8c-4510-accf-641fda5be98d
title: Inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c590d00fa9d6ac63f93caa287f34b9f2bf25357bd36ab9ea3fb9ce87e81291d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145709"
---
# <a name="bootstrapping"></a>Inicialização

Atualmente, cada instalação que tenta usar o instalador do Windows começa verificando se o instalador está presente no computador do usuário e se ele não está presente, se o usuário e o computador estão prontos para instalar o Windows Installer. Um aplicativo de [Instmsi.exe](instmsi-exe.md) está disponível com o SDK do Windows Installer que contém toda a lógica e a funcionalidade para instalar o Windows Instalador. No entanto, um aplicativo de inicialização deve gerenciar essa instalação.

O aplicativo de inicialização deve primeiro verificar se Windows Instalador está instalado no momento. Os aplicativos podem obter a versão do Windows Instalador atualmente instalado usando [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc). Se Windows instalador não estiver instalado no momento, o aplicativo de inicialização deverá consultar o sistema operacional para determinar qual versão do Instmsi.exe é necessária. Depois que a instalação do Windows Installer for iniciada, o aplicativo de inicialização deverá manipular códigos de retorno do aplicativo Instmsi.exe e manipular qualquer reinicialização que seja incorrida durante a instalação do Windows Installer. Para obter mais informações, [consulte Determining the Windows Installer Version](determining-the-windows-installer-version.md)

O exemplo a seguir demonstra como o aplicativo de instalação que instala o Microsoft Office 2000 verifica o sistema do usuário e configura a instalação do Windows Installer. Este exemplo é escrito especificamente para instalar Office 2000 e deve ser usado apenas como uma referência geral.

Quando um usuário insere um Office 2000 CD-ROM em seu computador, o Setup.exe tenta iniciar o modo de manutenção, o aplicativo de instalação ou não faz nada, de acordo com as necessidades do usuário. A seção a seguir descreve como o aplicativo de instalação do Office 2000, chamado Setup.exe, qualifica o usuário e seu computador, constrói uma linha de comando e instala o instalador do Windows usando o aplicativo Msiexec.exe.

## <a name="how-setupexe-bootstraps-the-windows-installer-when-installing-office-2000"></a>Como Setup.exe inicializa o instalador Windows ao instalar o Office 2000

1.  O usuário insere um Office 2000 CD-ROM no computador. O Windows sistema operacional Setup.exe usando a opção /autorun e o arquivo Autorun.inf. O arquivo Autorun.inf é encontrado na raiz do cd-rom Office 2000 e contém as seguintes seções:

    \[Autorun\]

     

    \[Office Características\]

     

    \[Informações do produto\]

     

    \[ServicePack \] .

    A seção Executar automaticamente contém uma linha de comando que executa o aplicativo Setup.exe, executa o ícone usado para exibir o disco e contém informações para adicionar uma opção "Instalar" e uma opção "Configurar" ao menu de contexto do \[ \] CD-ROM.

    A \[ Office recursos \] contém uma lista de recursos e pares de nomes de recursos.

    A \[ seção Informações do Produto especifica o nome e a versão do \] aplicativo.

    A seção ServicePack permite que um administrador de rede de definir o nível de service pack \[ \] mínimo necessário. O administrador de rede pode usar esta seção para autor do texto de uma mensagem de alerta exibida se o sistema operacional local não tiver os dados service pack.

    A seguir está um exemplo de Autorun.inf.

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

2.  O Setup.exe aplicativo verifica o \_ mutex MsiPromptForCD. Windows O instalador cria esse mutex quando solicita que o usuário insira o CD-ROM. A presença do mutex indica que Windows Instalador está executando uma instalação que solicitou o Office 2000 CD-ROM. Nesse caso, o Setup.exe é imediatamente final e permite que a instalação Office 2000 continue. Se o mutex estiver ausente, o aplicativo Setup.exe continua na etapa 3 em que uma chave do Registro é avaliada para determinar se Office 2000 está instalado.
3.  O Setup.exe aplicativo verifica a presença da chave do Registro do Office9:

    **HKCU/Software/Microsoft/Office/9.0/Common/General/InstallProductID**

    Se essa chave do Registro não existir, o aplicativo Setup.exe continuará na etapa 6 em que o sistema operacional é verificado para determinar se ele se qualifica para a instalação do Office 2000.

4.  Se a Office do Registro 2000 existir, o aplicativo Setup.exe verificará o estado de instalação atual chamando [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea). Um estado de retorno de InstallState Default indica que o Office 2000 já está instalado e o aplicativo Setup.exe continua na etapa 5 em que o Office 2000 está marcado para executar \_ da origem.

    Se Office 2000 não estiver instalado, o aplicativo Setup.exe continuará na etapa 6 em que o sistema operacional é verificado para determinar se ele se qualifica para a instalação do Office 2000.

5.  O Setup.exe aplicativo chama [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) para cada um dos recursos na seção **\[ OfficeFeatures \]** do arquivo Autorun.inf. Se qualquer um desses recursos retornar INSTALLSTATE SOURCE, isso indicará que o recurso está sendo executado da origem e o aplicativo \_ Setup.exe será imediatamente executado.

    Se nenhum dos recursos retornar INSTALLSTATE SOURCE, o aplicativo Setup.exe iniciará o aplicativo instalador, Msiexec.exe, e apresentará o modo de manutenção do instalador do Windows antes de \_ sair.

6.  O Setup.exe aplicativo determina se o sistema operacional se qualifica para uma instalação do Office 2000. Windows XP é necessário para instalar o Office 2000. Se o sistema operacional exigir uma atualização service pack para se qualificar para o Office 2000, o aplicativo Setup.exe exibirá o texto especificado no arquivo Autorun.inf. Se o sistema operacional não se qualificar para o Office 2000 ou uma atualização do Office 2000, o aplicativo Setup.exe exibirá uma mensagem que impede que o usuário continue.

    Se o sistema operacional se qualificar para o Office 2000, o aplicativo Setup.exe continuará na etapa 7, que determina se o Windows Installer está instalado no computador do usuário.

7.  Se Windows instalador existir no computador do usuário, o aplicativo Setup.exe iniciará o aplicativo Msiexec.exe e passará o arquivo Office 2000 .msi para ele.

    Se Windows Instalador do Windows não estiver instalado no computador local, o aplicativo Setup.exe continuará na etapa 8, que determina se o sistema operacional se qualifica para ter Windows Instalador instalado.

8.  Se o computador local estiver qualificado para Windows instalado, o aplicativo Setup.exe executa a versão correta do aplicativo Instmsi.exe instalador para a plataforma. Setup.exe pode passar a opção de linha de comando "/q" para suprimir a interface do usuário e impedir que o usuário altere as opções de configuração de instalação.
9.  O Setup.exe aplicativo carrega o arquivo Msi.dll recém-instalado e executa uma chamada para a [**função MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) para instalar o aplicativo do usuário.

## <a name="setupexe-command-line-parameters"></a>Setup.exe de linha de comando

O Setup.exe aplicativo permite que administradores e usuários passem opções de linha de comando para o Msiexec.exe aplicativo. Para obter mais informações, consulte [Opções de linha de comando](command-line-options.md). A tabela a seguir lista as opções de comando que podem ser usadas com Setup.exe.



| Opção                       | Uso                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /autorun                     | setup.exe /autorun                                                                                                                           | Executa o Autorun.inf descrito acima.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| /a                           | setup.exe /a                                                                                                                                 | Inicia uma instalação administrativa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| /j                           | \[u \| m \] *Pacote* ou <br/> \[u \| m \] *Package* /t *Transform List*<br/> ou <br/> \[u \| m \] *Package* /g *LanguageID*<br/> | Anuncia um produto. Essa opção ignora os valores de propriedade inseridos na linha de comando. u Anunciar ao usuário atual.<br/> m Anunciar para todos os usuários do computador.<br/> g Identificador de idioma<br/> t Aplica a transformação ao pacote anunciado.<br/>                                                                                                                                                                                                                        |
| /I                           | setup.exe /I Office9.msi /t ProgramMgmt.mst                                                                                                  | Especifica o arquivo .msi que Setup.exe deve ser instalado. Se a opção /I não estiver incluída, Setup.exe usará o arquivo Office9.msi.                                                                                                                                                                                                                                                                                                                                                                                 |
| /o<*valor da* = *propriedade*> | setup.exe /o CDKEY=111111-1111                                                                                                               | Define propriedades no arquivo .msi dados. Setup.exe passá-los para msiexec conforme escrito.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| /q                           | setup.exe /q                                                                                                                                 | De definir o nível da interface do usuário da instalação. /q no UI (/qn para msiexec.) /qb basic UI<br/> /qr interface do usuário reduzida.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| /m\#                         | setup.exe /m4                                                                                                                                | Dá suporte a várias licenças de acordo com Selecionar contratos. Essa propriedade é usada na ação personalizada Verificação de Licença para gravar o certificado LV. A opção /m deve ser seguida pelo número de desbloqueios permitidos. O valor especificado pela opção /m deve ser definido como a propriedade "M" no arquivo Office9.msi dados. Se nenhum valor for especificado, mas a opção /m for usada com a instalação, o valor de 0 deverá ser definido. A opção /m é necessária para dar suporte a Selecionar clientes usando um CD ou uma rede. |
| /settings                    | setup.exe /settings mysettings.ini                                                                                                           | permite que os administradores especifiquem um arquivo de .ini que contém todas as configurações personalizadas a serem passadas durante a instalação do Office 2000. Consulte a descrição do arquivo de .ini abaixo.                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="using-an-ini-file"></a>Usando um arquivo de .ini

A criação de um arquivo de inicialização pode ser mais fácil do que criar uma linha de comando longa. Usando a opção/Settings, o aplicativo de Setup.exe lê o arquivo de .ini especificado e constrói uma linha de comando para passar para o aplicativo Msiexec.exe. Somente as propriedades com suporte na linha de comando têm suporte no arquivo .ini. Se uma propriedade ou um valor for encontrado tanto no arquivo de .ini quanto na linha de comando, as configurações de linha de comando substituirão as configurações de arquivo de .ini.

O formato do arquivo de .ini é:

\[MSI\]

 

\[MST\]

 

\[options\]

 

\[Vídeo\]

A \[ \] seção msi do arquivo de .ini especifica o caminho para o pacote de instalação da instalação do. Isso corresponde à opção/I na linha de comando.

A \[ \] seção MST do arquivo de .ini especifica o caminho para as transformações usadas com essa instalação. Isso corresponde à opção/j na linha de comando. Várias transformações são indicadas em uma linha diferente, usando MST1 MST (N). Quando analisada na linha de comando, a lista no arquivo de .ini é transformada da esquerda para a direita. Observe que o número associado ao título MST (N) está presente apenas para manter identificadores exclusivos e não tem um significado programático.

A \[ \] seção Opções permite que os administradores de rede definam e substituam Propriedades nos arquivos .msi ou. MST. As opções definidas no arquivo de .ini são adicionadas à linha de comando usando a opção/o. Cada opção na seção Option deve ter um nome de propriedade e um valor.

A \[ \] seção exibição é usada para definir o nível de interface do usuário usado durante a instalação. Isso corresponde à opção/q na linha de comando. Os valores válidos são None, Basic, Reduced e Full.

Arquivo de .ini de exemplo

\[MSI\]

 

MSI = \\ \\ sourceshare \\ office2000 \\Office2000.msi

 

\[MST\]

 

MST1 = \\ \\ sourceshare \\ office2000 \\ trns1. MST

 

MST2 = \\ \\ sourceshare \\ office2000 \\ trns2. MST

 

\[Opções\]

 

PUBLICproperty = seu valor

\[Vídeo\]

 

Exibir = nenhum

 

