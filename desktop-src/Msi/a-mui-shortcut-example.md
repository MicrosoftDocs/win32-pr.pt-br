---
description: Esta seção descreve como adicionar cadeias de caracteres de recursos à tabela de atalho Windows Installer para uso com MUI (Multilingual User Interfaces).
ms.assetid: f521cfb8-32a8-4b62-b258-5b99cc3e0416
title: Um exemplo de atalho do MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0392713c1eaedabaa989baecd79478a9b329e955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752056"
---
# <a name="a-mui-shortcut-example"></a>Um exemplo de atalho do MUI

Esta seção descreve como adicionar cadeias de caracteres de recursos à tabela de [atalho](shortcut-table.md) Windows Installer para uso com MUI (Multilingual User Interfaces).

**Windows Installer 2,0 e Windows Installer 3,0:** Sem suporte. Este exemplo requer Windows Installer 4,0.

Consulte a documentação da [MUI (Multilingual User interface)](/windows/desktop/Intl/multilingual-user-interface) para obter informações sobre como desenvolver aplicativos habilitados para MUI.

Para adicionar as cadeias de caracteres de recurso usadas pelas interfaces de usuário multilíngue do Windows Vista a um pacote Windows Installer:

1.  Adicione as informações de todos os arquivos de idioma e neutros ao idioma à [tabela de arquivos](file-table.md). Por exemplo, os arquivos podem consistir em um arquivo com neutralidade de idioma (msimsg.dll) e arquivos de idioma para inglês (msimsgen.dll. mui), japonês (msimsgja.dll. mui) e chinês (msimsgcs.dll. mui). Cada arquivo pode pertencer a um componente diferente. Cada arquivo pode ter um nome de arquivo longo e curto. No caso deste exemplo, as informações a seguir podem ser adicionadas à [tabela de arquivos](file-table.md).

    [Tabela de arquivos](file-table.md) (parcial)

    

    | Arquivo        | Componente\_     | FileName                     |
    |-------------|-----------------|------------------------------|
    | msimsgmuija | MSIMSG \_ MUI \_ ja | msimsgja.dll\|msimsg.dll. mui |
    | msimsgmuics | MSIMSG \_ MUI \_ cs | msimsgcs.dll\|msimsg.dll. mui |
    | msimsgmuien | MSIMSG \_ MUI \_ en | msimsgen.dll\|msimsg.dll. mui |
    | msimsgdll   | MSIMSG          | msimsg.dll                   |

    

     

2.  Adicione informações à [tabela de componentes](component-table.md) para esses componentes. Cada componente tem um identificador GUID exclusivo que deve ser inserido no campo ComponentID da tabela de componentes. O arquivo que pertence ao componente pode servir como o caminho Keypara esse componente. O diretório que contém cada componente pode ser especificado no campo diretório \_ . As informações a seguir podem ser adicionadas à tabela de componentes.

    [Tabela de componentes](component-table.md) (parcial)

    

    | Componente       | Diretório\_   | KeyPath     |
    |-----------------|---------------|-------------|
    | MSIMSG \_ MUI \_ ja | MUIFolder \_ ja | msimsgmuija |
    | MSIMSG \_ MUI \_ cs | MUIFolder \_ cs | msimsgmuics |
    | MSIMSG \_ MUI \_ en | MUIFolder \_ en | msimsgmuien |
    | MSIMSG          | MUIFolder     | msimsgdll   |

    

     

3.  Edite a tabela de [diretórios](directory-table.md) para que os componentes sejam instalados nos diretórios corretos. Certifique-se de incluir informações sobre o diretório em que o atalho será instalado. Por exemplo, as informações a seguir podem ser adicionadas à tabela de diretório de um pacote que instala os componentes e um atalho localizado no diretório DesktopFolder

    [Tabela de diretórios](directory-table.md) (parcial)

    

    | Diretório     | Pai do diretório \_ | DefaultDir |
    |---------------|-------------------|------------|
    | TARGETDIR     |                   | SourceDir  |
    | MsiTest       | TARGETDIR         | MsiTest:.  |
    | MUIFolder     | MsiTest           | INTERFACE        |
    | MUIFolder \_ cs | MUIFolder         | cs-CZ      |
    | MUIFolder \_ en | MUIFolder         | en-US      |
    | MUIFolder \_ ja | MUIFolder         | ja-JP      |
    | DesktopFolder | TARGETDIR         | .          |

    

     

4.  Adicione uma linha à tabela de [atalho](shortcut-table.md) para cada atalho. Por exemplo, a tabela de [atalho](shortcut-table.md) pode conter as seguintes informações para dois atalhos, Quick1 e Quick2, instalados no diretório DirectoryFolder. Cada atalho pertence ao recurso especificado no campo de destino. O ícone associado ao atalho pode ser especificado no \_ campo ícone e na tabela de [ícones](icon-table.md) .

    [Tabela de atalho](shortcut-table.md) (parcial)

    

    | Atalho | Diretório\_   | Componente\_ | Destino               | ícone             |
    |----------|---------------|-------------|----------------------|------------------|
    | Quick1   | DesktopFolder | MSIMSG      | FeatureChild1 \_ local | HelpFileIcon.exe |
    | Quick2   | DesktopFolder | MSIMSG      | FeatureChild1 \_ local | HelpFileIcon.exe |

    

     

5.  Adicione informações à tabela de [tabela de recursos](feature-table.md) para o recurso que possui o atalho pertence. Quando o atalho é ativado, o instalador verifica se todos os componentes pertencentes a esse recurso estão instalados antes de iniciar o arquivo de chave do componente especificado na \_ coluna componente da tabela de [atalho](shortcut-table.md) . No caso deste exemplo, as informações a seguir podem ser adicionadas à tabela de tabela de recursos para o \_ recurso local FeatureParent1.

    [Tabela de recursos](feature-table.md) (parcial)

    

    | Recurso               | Pai do recurso \_       | Título                 | Atributos |
    |-----------------------|-----------------------|-----------------------|------------|
    | FeatureParent1 \_ local |                       | FeatureParent1 \_ local | 16         |
    | FeatureChild1 \_ local  | FeatureParent1 \_ local | FeatureParent1 \_ local | 0          |

    

     

6.  Para cada novo atalho, adicione as informações de cadeia de caracteres do recurso aos campos DisplayResourceDLL, DisplayResourceId, DescriptionResourceDLL e DescriptionResourceId da [tabela de atalho](shortcut-table.md). Os campos DisplayResourceDLL e DescriptionResourceDLL contêm a cadeia de caracteres do recurso no formato de cadeia de caracteres [formatada](formatted.md) . A cadeia de caracteres formatada pode usar a \[ \# Convenção *FileKey* \] do formato [formatado](formatted.md) . Adicione os índices de exibição e descrição para as cadeias de caracteres de recurso nos campos DisplayResourceId e DescriptionResourceId.

    [Tabela de atalho](shortcut-table.md) (parcial)

    

    | Atalho | DisplayResourceDLL | DisplayResourceId | DescriptionResourceDLL | DescriptionResourceId |
    |----------|--------------------|-------------------|------------------------|-----------------------|
    | Quick1   | \[\#msimsgdll\]    | 36                | \[\#msimsgdll\]        | 37                    |
    | Quick2   | \[\#msimsgdll\]    | 38                | \[\#msimsgdll\]        | 39                    |

    

     

7.  Depois de instalar o pacote, teste para garantir que a interface do usuário multilíngüe esteja funcionando conforme o esperado.

 

 
