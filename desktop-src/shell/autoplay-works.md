---
description: A criação de um aplicativo habilitado para AutoRun é um procedimento simples. Este tópico usa o CD-ROM como um exemplo (foi a primeira mídia para implementar essa tecnologia), mas hoje há muitos tipos de mídia diferentes que podem usá-lo.
title: Criando um aplicativo AutoRun-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0d01f4a2-64c4-4b31-9fc9-361da6825ab8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 24a944b011c926d1638e5d0bcb0d35fc348e5783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090030"
---
# <a name="creating-an-autorun-enabled-application"></a>Criando um aplicativo AutoRun-Enabled

A criação de um aplicativo habilitado para AutoRun é um procedimento simples. Este tópico usa o CD-ROM como um exemplo (foi a primeira mídia para implementar essa tecnologia), mas hoje há muitos tipos de mídia diferentes que podem usá-lo.

Para habilitar o AutoRun em seu aplicativo, você simplesmente inclui dois arquivos essenciais:

-   Um arquivo autorun. inf
-   Um aplicativo de inicialização

Quando um usuário insere um disco em uma unidade de CD-ROM em um computador compatível com AutoRun, o sistema verifica imediatamente se o disco tem um sistema de arquivos de computador pessoal. Se tiver, o sistema pesquisará um arquivo chamado [autorun. inf](#creating-an-autoruninf-file). Esse arquivo especifica um aplicativo de instalação que será executado junto com uma variedade de configurações opcionais. O aplicativo de inicialização normalmente instala, desinstala, configura e, talvez, executa o aplicativo.

-   [Criando um arquivo autorun. inf](#creating-an-autoruninf-file)
-   [A \[ \] seção DeviceInstall](#the-deviceinstall-section)
-   [Tópicos relacionados](#related-topics)

## <a name="creating-an-autoruninf-file"></a>Criando um arquivo autorun. inf

Autorun. inf é um arquivo de texto localizado no diretório raiz do CD-ROM que contém seu aplicativo. Sua função principal é fornecer ao sistema o nome e o local do programa de inicialização do aplicativo que será executado quando o disco for inserido.

> [!Note]  
> Não há suporte para arquivos autorun. inf no Windows XP para unidades que retornam \_ removível de unidade de [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).

 

O arquivo autorun. inf também pode conter informações opcionais, incluindo:

-   O nome de um arquivo que contém um ícone que representará a unidade de CD-ROM do aplicativo. Esse ícone será exibido pelo Windows Explorer no lugar do ícone de unidade padrão.
-   Comandos adicionais para o menu de atalho que é exibido quando o usuário clica com o botão direito do mouse no ícone do CD-ROM. Você também pode especificar o comando padrão que é executado quando o usuário clica duas vezes no ícone.

Os arquivos autorun. inf são semelhantes aos arquivos. ini. Elas consistem em uma ou mais seções, cada uma com um nome entre colchetes. Cada seção contém uma série de comandos que serão executados pelo shell quando o disco for inserido. Há duas seções que estão definidas no momento para arquivos autorun. inf.

-   A seção **\[ autorun \]** contém os comandos padrão de Autorun. Todos os arquivos autorun. inf devem ter uma seção de **\[ autorun \]** .
-   Uma seção opcional **\[ autorun. \] Alpha** pode ser incluída para sistemas em execução em computadores baseados em RISC. Quando um disco é inserido em uma unidade de CD-ROM em um sistema baseado em RISC, o Shell executará os comandos nesta seção em vez daqueles na seção de **\[ autorun \]** .

> [!Note]  
> O Shell verifica primeiro uma seção específica da arquitetura. Se ele não encontrar um, ele usará as informações na seção **\[ autorun \]** . Depois que o Shell encontra uma seção, ele ignora todas as outras, portanto, cada seção deve ser independente.

 

Cada seção contém uma série de comandos que determinam como ocorre a operação de execução automática. Há cinco comandos disponíveis.



| Comando                         | Descrição                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [DefaultIcon](autorun-cmds.md) | Especifica o ícone padrão para o aplicativo.                                        |
| [cone](autorun-cmds.md)        | Especifica o caminho e o nome do arquivo de um ícone específico do aplicativo para a unidade de CD-ROM. |
| [open](autorun-cmds.md)        | Especifica o caminho e o nome de arquivo do aplicativo de inicialização.                           |
| [useautorun](autorun-cmds.md)  | Especifica que os recursos de reprodução automática v2 devem ser usados se houver suporte.                       |
| [Shell](autorun-cmds.md)       | Define o comando padrão no menu de atalho do CD-ROM.                             |
| [verbo do Shell \_](autorun-cmds.md) | Adiciona comandos ao menu de atalho do CD-ROM.                                           |



 

Veja a seguir um exemplo de um arquivo autorun. inf simples. Ele especifica Filename.exe como o aplicativo de inicialização. O segundo ícone no Filename.exe representará a unidade de CD-ROM em vez do ícone de unidade padrão.


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



Este exemplo de Autorun. inf executa aplicativos de inicialização diferentes, dependendo do tipo de computador.


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a>A \[ \] seção DeviceInstall

Você pode usar a seção **\[ DeviceInstall \]** em qualquer mídia removível. Há suporte apenas no Windows XP. Você usa **DriverPath** para especificar um caminho de diretório no qual o Windows XP procura por arquivos de driver, o que impede uma pesquisa demorada por todo o conteúdo.

Use a seção **\[ DeviceInstall \]** com uma instalação de driver para especificar diretórios em que o Windows XP deve pesquisar arquivos de driver na mídia. No Windows XP, toda a mídia não é mais pesquisada por padrão, portanto, exigir **\[ DeviceInstall \]** para especificar locais de pesquisa. A seguir estão as únicas mídias removíveis que o Windows XP pesquisa totalmente sem uma seção **\[ DeviceInstall \]** em um arquivo autorun. inf.

-   Disquetes encontrados nas unidades A ou B.
-   Mídia de CD/DVD com menos de 1 gigabyte (GB) de tamanho.

Todas as outras mídias devem incluir uma seção **\[ DeviceInstall \]** para o Windows XP detectar quaisquer drivers armazenados nessa mídia.

> [!Note]  
> Assim como acontece com a seção **\[ autorun \]** , a seção **\[ DeviceInstall \]** pode ser específica da arquitetura.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como implementar aplicativos de inicialização autorun](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[Gravando um aplicativo de instalação de dispositivo](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
