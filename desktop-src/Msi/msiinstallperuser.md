---
description: As propriedades MSIINSTALLPERUSER e ALLUSERS podem ser definidas pelo usuário no momento da instalação, por meio da interface do usuário ou em uma linha de comando, para solicitar que o Windows Installer instale um pacote de uso duplo para o usuário atual ou todos os usuários do computador.
ms.assetid: 17eb24e4-8464-4724-9768-4b58446ee4bc
title: Propriedade MSIINSTALLPERUSER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fa54026c859b5f4f610fd54aec2df3ca518ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752638"
---
# <a name="msiinstallperuser-property"></a>Propriedade MSIINSTALLPERUSER

As propriedades **MSIINSTALLPERUSER** e [**AllUsers**](allusers.md) podem ser definidas pelo usuário no momento da instalação, por meio da interface do usuário ou em uma linha de comando, para solicitar que o Windows Installer instale um pacote de uso duplo para o usuário atual ou todos os usuários do computador. Para usar a propriedade **MSIINSTALLPERUSER** , o valor da propriedade [**AllUsers**](allusers.md) deve ser 2 e o pacote precisa ter sido criado para ser capaz de ser instalado no contexto por usuário ou por máquina. Para obter informações sobre como criar um pacote de uso duplo, consulte [criação de pacote único](single-package-authoring.md). Se o valor da propriedade **AllUsers** não for igual a 2, o valor da propriedade **MSIINSTALLPERUSER** será ignorado e não terá efeito sobre a instalação. O valor da propriedade **MSIINSTALLPERUSER** é ignorado ao instalar o pacote usando Windows Installer 4,5 ou anterior.

Para solicitar que o Windows Installer instale o pacote de uso duplo no [contexto de instalação](installation-context.md)por máquina, o usuário pode definir o valor da propriedade **MSIINSTALLPERUSER** como uma cadeia de caracteres vazia ("") e o valor da propriedade [**AllUsers**](allusers.md) como 2 usando uma interface de usuário criada ou uma linha de comando.

Para solicitar que o Windows Installer instale o pacote de uso duplo no [contexto de instalação](installation-context.md)por usuário, o usuário pode definir o valor da propriedade **MSIINSTALLPERUSER** como 1 e o valor da propriedade [**AllUsers**](allusers.md) como 2 usando uma interface de usuário criada ou uma linha de comando.

Se o valor da propriedade [**AllUsers**](allusers.md) não for igual a 2, o Windows Installer ignorará o valor da propriedade **MSIINSTALLPERUSER** . Se Windows Installer instalar o aplicativo no contexto por máquina, ele redefinirá o valor da propriedade **AllUsers** como 1. Se Windows Installer instalar o aplicativo no contexto por usuário, ele redefinirá o valor da propriedade **AllUsers** como uma cadeia de caracteres vazia (""). Os aplicativos que foram instalados por usuário, portanto, recebem todas as atualizações ou reparos em uma base por usuário e aplicativos instalados por computador recebem atualizações ou reparos em uma base por máquina.

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** a propriedade **MSIINSTALLPERUSER** é ignorada pelas versões anteriores à Windows Installer 5,0.

## <a name="default-value"></a>Valor padrão

O contexto de instalação padrão recomendado é por usuário para um pacote de uso duplo. Autor MSIINSTALLPERUSER = 1 e ALLUSERS = 2 na [tabela de propriedades](property-table.md) do pacote de uso duplo para especificar por usuário como o contexto de instalação padrão.

## <a name="remarks"></a>Comentários

Você pode garantir que a propriedade **MSIINSTALLPERUSER** não tenha sido definida definindo seu valor como uma cadeia de caracteres vazia (""), MSIINSTALLPERUSER = "".

O contexto de instalação determina os valores das propriedades [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**startupfolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)e [**CommonFiles64Folder**](commonfiles64folder.md) . O contexto de instalação determina as partes do registro em que as entradas na [tabela de registro](registry-table.md) e na [tabela RemoveRegistry](removeregistry-table.md), com-1 na coluna raiz, são gravadas ou removidas. Para obter informações sobre o contexto de instalação, consulte [contexto de instalação](installation-context.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[**ALLUSERS**](allusers.md)
</dt> <dt>

[Contexto de instalação](installation-context.md)
</dt> <dt>

[Criação de pacote único](single-package-authoring.md)
</dt> </dl>

 

 




