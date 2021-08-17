---
description: Esta seção descreve como adicionar cadeias de caracteres de recurso à tabela Windows atalho do instalador para uso com interfaces de usuário multilíngues (MUI).
ms.assetid: f521cfb8-32a8-4b62-b258-5b99cc3e0416
title: Um exemplo de atalho da MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b38f674a63e854fbcd4439229c5aded5b0efe6cfc17d3e475f8a52f30db949
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640283"
---
# <a name="a-mui-shortcut-example"></a>Um exemplo de atalho da MUI

Esta seção descreve como adicionar cadeias de caracteres de recurso à tabela Windows [atalho](shortcut-table.md) do instalador para uso com interfaces de usuário multilíngues (MUI).

**Windows Instalador 2.0 e Windows Instalador 3.0:** Sem suporte. Este exemplo requer Windows Instalador 4.0.

Consulte a [documentação Interface de Usuário Multilíngue (MUI)](/windows/desktop/Intl/multilingual-user-interface) para obter informações sobre como desenvolver aplicativos habilitados para MUI.

Para adicionar as cadeias de caracteres de recurso usadas Windows Interfaces do Usuário Multilíngues do Vista a um pacote Windows Instalador:

1.  Adicione as informações de todos os arquivos de idioma neutros e de idioma à [Tabela de Arquivos](file-table.md). Por exemplo, os arquivos podem consistir em um arquivo neutro em idioma (msimsg.dll) e arquivos de idioma para inglês (msimsgen.dll.mui), japonês (msimsgja.dll.mui) e chinês (msimsgcs.dll.mui). Cada arquivo pode pertencer a um componente diferente. Cada arquivo pode ter um nome de arquivo longo e curto. No caso deste exemplo, as informações a seguir podem ser adicionadas à [Tabela de Arquivos](file-table.md).

    [Tabela de arquivos](file-table.md) (parcial)

    

    | Arquivo        | Componente\_     | FileName                     |
    |-------------|-----------------|------------------------------|
    | msimsgmuija | MSIMSG \_ MUI \_ JA | msimsgja.dll\|msimsg.dll.mui |
    | msimsgmuics | MSIMSG \_ MUI \_ CS | msimsgcs.dll\|msimsg.dll.mui |
    | msimsgmuhin | MSIMSG \_ MUI \_ EN | msimsgen.dll\|msimsg.dll.mui |
    | msimsgdll   | MSIMSG          | msimsg.dll                   |

    

     

2.  Adicione informações à tabela [Componente para](component-table.md) esses componentes. Cada componente tem um identificador GUID exclusivo que deve ser inserido no campo ComponentId da tabela Component. O arquivo que pertence ao componente pode servir como o KeyPath para esse componente. O diretório que contém cada componente pode ser especificado no campo \_ Diretório. As informações a seguir podem ser adicionadas à tabela Componente.

    [Tabela de componentes](component-table.md) (parcial)

    

    | Componente       | Diretório\_   | KeyPath     |
    |-----------------|---------------|-------------|
    | MSIMSG \_ MUI \_ JA | MUIFolder \_ JA | msimsgmuija |
    | MSIMSG \_ MUI \_ CS | MUIFolder \_ CS | msimsgmuics |
    | MSIMSG \_ MUI \_ EN | MUIFolder \_ EN | msimsgmuhin |
    | MSIMSG          | MUIFolder     | msimsgdll   |

    

     

3.  Edite [a tabela](directory-table.md) Diretório para que os componentes sejam instalados nos diretórios corretos. Certifique-se de incluir informações sobre o diretório em que o atalho será instalado. Por exemplo, as informações a seguir podem ser adicionadas à tabela Diretório de um pacote que instala os componentes e um atalho localizado no diretório DesktopFolder.

    [Tabela de diretórios](directory-table.md) (parcial)

    

    | Diretório     | Pai do \_ Diretório | Defaultdir |
    |---------------|-------------------|------------|
    | Targetdir     |                   | SourceDir  |
    | MsiTest       | Targetdir         | MsiTest:.  |
    | MUIFolder     | MsiTest           | Mui        |
    | MUIFolder \_ CS | MUIFolder         | cs-CZ      |
    | MUIFolder \_ EN | MUIFolder         | pt-BR      |
    | MUIFolder \_ JA | MUIFolder         | ja-JP      |
    | DesktopFolder | Targetdir         | .          |

    

     

4.  Adicione uma linha à tabela [Atalho](shortcut-table.md) para cada atalho. Por exemplo, a tabela [Atalho](shortcut-table.md) pode conter as seguintes informações para dois atalhos, Quick1 e Quick2, instalados no diretório DirectoryFolder. Cada atalho pertence ao recurso especificado no campo Destino. O ícone associado ao atalho pode ser especificado no campo Ícone \_ e na [tabela Ícone.](icon-table.md)

    [Tabela de atalho](shortcut-table.md) (parcial)

    

    | Atalho | Diretório\_   | Componente\_ | Destino               | ícone             |
    |----------|---------------|-------------|----------------------|------------------|
    | Quick1   | DesktopFolder | MSIMSG      | FeatureChild1 \_ Local | HelpFileIcon.exe |
    | Quick2   | DesktopFolder | MSIMSG      | FeatureChild1 \_ Local | HelpFileIcon.exe |

    

     

5.  Adicione informações à tabela [Tabela de Recursos](feature-table.md) para o recurso que possui o atalho. Quando o atalho é ativado, o instalador verifica se todos os componentes que pertencem a esse recurso estão instalados antes de iniciar o arquivo de chave do componente especificado na coluna Componente da tabela \_ [Atalho.](shortcut-table.md) No caso deste exemplo, as informações a seguir podem ser adicionadas à tabela Tabela de Recursos para o recurso Local FeatureParent1. \_

    [Tabela de recursos](feature-table.md) (parcial)

    

    | Recurso               | Pai do \_ recurso       | Título                 | Atributos |
    |-----------------------|-----------------------|-----------------------|------------|
    | FeatureParent1 \_ Local |                       | FeatureParent1 \_ Local | 16         |
    | FeatureChild1 \_ Local  | FeatureParent1 \_ Local | FeatureParent1 \_ Local | 0          |

    

     

6.  Para cada novo atalho, adicione as informações de cadeia de caracteres de recurso aos campos DisplayResourceDLL, DisplayResourceId, DescriptionResourceDLL e DescriptionResourceId da tabela [atalho](shortcut-table.md). Os campos DisplayResourceDLL e DescriptionResourceDLL contêm a cadeia de caracteres de recurso no formato de cadeia de caracteres [formatada.](formatted.md) A cadeia de caracteres formatada pode usar \[ \# *a convenção filekey* \] do formato [Formatado.](formatted.md) Adicione os índices de exibição e descrição para as cadeias de caracteres de recurso nos campos DisplayResourceId e DescriptionResourceId.

    [Tabela de atalho](shortcut-table.md) (parcial)

    

    | Atalho | DisplayResourceDLL | DisplayResourceId | DescriptionResourceDLL | DescriptionResourceId |
    |----------|--------------------|-------------------|------------------------|-----------------------|
    | Quick1   | \[\#msimsgdll\]    | 36                | \[\#msimsgdll\]        | 37                    |
    | Quick2   | \[\#msimsgdll\]    | 38                | \[\#msimsgdll\]        | 39                    |

    

     

7.  Depois de instalar o pacote, teste para garantir que o Interface de Usuário Multilíngue está funcionando conforme o esperado.

 

 
