---
description: Uma lista das propriedades de Windows Installer fornecendo valores gravados na chave de registro de desinstalação.
ms.assetid: f831cc62-4b19-4285-8bb1-6080567ac985
title: Propriedades de Windows Installer para a chave de registro de desinstalação
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: 90174cabed7a1d9ff0ca21b532c459a1026787a6
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/30/2021
ms.locfileid: "105994500"
---
# <a name="windows-installer-properties-for-the-uninstall-registry-key"></a>Propriedades de Windows Installer para a chave de registro de desinstalação

As seguintes propriedades do instalador fornecem os valores gravados na chave do registro:

**HKEY \_ \_** \\ Desinstalação do **software** do computador local \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ 

Os valores são armazenados em uma subchave identificada pelo GUID do código do produto do aplicativo.



| Valor               | Propriedade Windows Installer                                                                                                                                                                                                                                                                                                                                           |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName         | Propriedade [**ProductName**](productname.md)                                                                                                                                                                                                                                                                                                                          |
| DisplayVersion      | Derivado da propriedade [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Publicador           | Propriedade [**manufacturer**](manufacturer.md)                                                                                                                                                                                                                                                                                                                        |
| VersionMinor        | Derivado da propriedade [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| VersionMajor        | Derivado da propriedade [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Versão             | Derivado da propriedade [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| HelpLink            | Propriedade [**ARPHELPLINK**](arphelplink.md)                                                                                                                                                                                                                                                                                                                          |
| HelpTelephone       | Propriedade [**ARPHELPTELEPHONE**](arphelptelephone.md)                                                                                                                                                                                                                                                                                                                |
| InstallDate         | A última vez em que este produto recebeu o serviço. O valor dessa propriedade é substituído cada vez que um patch é aplicado ou removido do produto ou a opção de [linha de comando](command-line-options.md) /v é usada para reparar o produto. Se o produto não tiver recebido nenhum reparo ou patches, essa propriedade conterá a hora em que este produto foi instalado neste computador. |
| InstallLocation     | Propriedade [**ARPINSTALLLOCATION**](arpinstalllocation.md)                                                                                                                                                                                                                                                                                                            |
| Instalar       | Propriedade [**SourceDir**](sourcedir.md)                                                                                                                                                                                                                                                                                                                              |
| URLInfoAbout        | Propriedade [**ARPURLINFOABOUT**](arpurlinfoabout.md)                                                                                                                                                                                                                                                                                                                  |
| URLUpdateInfo       | Propriedade [**ARPURLUPDATEINFO**](arpurlupdateinfo.md)                                                                                                                                                                                                                                                                                                                |
| AuthorizedCDFPrefix | Propriedade [**ARPAUTHORIZEDCDFPREFIX**](arpauthorizedcdfprefix.md)                                                                                                                                                                                                                                                                                                    |
| Comentários            | Propriedade [**ARPCOMMENTS**](arpcomments.md) <br/> Comentários fornecidos ao painel de controle **Adicionar ou remover programas** .<br/>                                                                                                                                                                                                                                |
| Contact             | Propriedade [**ARPCONTACT**](arpcontact.md) <br/> Contato fornecido para o painel de controle **Adicionar ou remover programas** .<br/>                                                                                                                                                                                                                                   |
| EstimatedSize       | Determinado e definido pelo Windows Installer.                                                                                                                                                                                                                                                                                                                         |
| Idioma            | Propriedade [**ProductLanguage**](productlanguage.md)                                                                                                                                                                                                                                                                                                                  |
| ModifyPath          | Determinado e definido pelo Windows Installer.                                                                                                                                                                                                                                                                                                                         |
| Leiame              | Propriedade [**ARPREADME**](arpreadme.md) <br/> Leiame fornecido para o painel de controle **Adicionar ou remover programas** .<br/>                                                                                                                                                                                                                                      |
| UninstallString     | Determinado e definido por Windows Installer.                                                                                                                                                                                                                                                                                                                             |
| SettingsIdentifier  | Propriedade [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre propriedades](about-properties.md)
</dt> <dt>

[Configurando adicionar/remover programas com Windows Installer](configuring-add-remove-programs-with-windows-installer.md)
</dt> <dt>

[Referência de propriedade](property-reference.md)
</dt> <dt>

[Usando propriedades](using-properties.md)
</dt> </dl>

 

 




