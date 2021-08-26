---
description: Uma lista das propriedades do Windows Instalador que dão valores gravados na chave do Registro de Desinstalar.
ms.assetid: f831cc62-4b19-4285-8bb1-6080567ac985
title: Windows Propriedades do instalador para a chave do Registro de desinstalação
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: b898cd2a83a05783141ddf1fb4a7cbebb783bbcd7640526c5b653afa434d2175
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810310"
---
# <a name="windows-installer-properties-for-the-uninstall-registry-key"></a>Windows Propriedades do instalador para a chave do Registro de desinstalação

As seguintes propriedades do instalador dão os valores gravados na chave do Registro:

**HKEY \_ Desinstalação do Software LOCAL \_ MACHINE** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ 

Os valores são armazenados em uma sub-chave identificada pelo GUID do código do produto do aplicativo.



| Valor               | Windows Propriedade do instalador                                                                                                                                                                                                                                                                                                                                           |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName         | [**Propriedade ProductName**](productname.md)                                                                                                                                                                                                                                                                                                                          |
| DisplayVersion      | Derivado da [**propriedade ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Publisher           | [**Propriedade Manufacturer**](manufacturer.md)                                                                                                                                                                                                                                                                                                                        |
| VersionMinor        | Derivado da [**propriedade ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| VersionMajor        | Derivado da [**propriedade ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Versão             | Derivado da [**propriedade ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| HelpLink            | [**Propriedade ARPHELPLINK**](arphelplink.md)                                                                                                                                                                                                                                                                                                                          |
| HelpTelephone       | [**Propriedade ARPHELPTELEPHONE**](arphelptelephone.md)                                                                                                                                                                                                                                                                                                                |
| InstallDate         | A última vez que esse produto recebeu o serviço. O valor dessa propriedade é substituído sempre que um patch é aplicado ou removido do produto ou a Opção de Linha de Comando [/v](command-line-options.md) é usada para reparar o produto. Se o produto não tiver recebido reparos ou patches, essa propriedade conterá a hora em que esse produto foi instalado neste computador. |
| InstallLocation     | [**Propriedade ARPINSTALLLOCATION**](arpinstalllocation.md)                                                                                                                                                                                                                                                                                                            |
| InstallSource       | [**Propriedade SourceDir**](sourcedir.md)                                                                                                                                                                                                                                                                                                                              |
| URLInfoAbout        | [**Propriedade ARPURLINFOABOUT**](arpurlinfoabout.md)                                                                                                                                                                                                                                                                                                                  |
| URLUpdateInfo       | [**Propriedade ARPURLUPDATEINFO**](arpurlupdateinfo.md)                                                                                                                                                                                                                                                                                                                |
| AuthorizedCDFPrefix | [**Propriedade ARPAUTHORIZEDCDFPREFIX**](arpauthorizedcdfprefix.md)                                                                                                                                                                                                                                                                                                    |
| Comentários            | [**Propriedade ARPCOMMENTS**](arpcomments.md) <br/> Comentários fornecidos ao **painel de controle Adicionar ou Remover** Programas.<br/>                                                                                                                                                                                                                                |
| Contact             | [**Propriedade ARPCONTACT**](arpcontact.md) <br/> Contato fornecido para o **painel de controle Adicionar ou Remover** Programas.<br/>                                                                                                                                                                                                                                   |
| EstimatedSize       | Determinado e definido pelo Windows Instalador.                                                                                                                                                                                                                                                                                                                         |
| Idioma            | [**Propriedade ProductLanguage**](productlanguage.md)                                                                                                                                                                                                                                                                                                                  |
| ModifyPath          | Determinado e definido pelo Windows Instalador.                                                                                                                                                                                                                                                                                                                         |
| Leiame              | [**Propriedade ARPREADME**](arpreadme.md) <br/> Leiame fornecido para o **painel de controle Adicionar ou Remover** Programas.<br/>                                                                                                                                                                                                                                      |
| UninstallString     | Determinado e definido pelo Windows Instalador.                                                                                                                                                                                                                                                                                                                             |
| ConfiguraçõesIdentificador  | [**Propriedade MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre propriedades](about-properties.md)
</dt> <dt>

[Configurando Adicionar/Remover Programas com Windows Instalador](configuring-add-remove-programs-with-windows-installer.md)
</dt> <dt>

[Referência de propriedade](property-reference.md)
</dt> <dt>

[Usando propriedades](using-properties.md)
</dt> </dl>

 

 




