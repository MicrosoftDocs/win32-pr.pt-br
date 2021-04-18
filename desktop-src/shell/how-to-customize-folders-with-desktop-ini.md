---
description: Personalizando a aparência e o comportamento de uma pasta individual com Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Como Personalizar pastas com Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaac3e6a96257e63b5e4210da0aa6e6e1db77eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571163"
---
# <a name="how-to-customize-folders-with-desktopini"></a>Como Personalizar pastas com Desktop.ini

As pastas do sistema de arquivos são normalmente exibidas com um ícone padrão e um conjunto de propriedades, que especificam, por exemplo, se a pasta é compartilhada. Você pode personalizar a aparência e o comportamento de uma pasta individual criando um arquivo de Desktop.ini para essa pasta.

## <a name="instructions"></a>Instruções

### <a name="using-desktopini-files"></a>Usando arquivos Desktop.ini

Normalmente, as pastas são exibidas com o ícone de pasta padrão. Um uso comum do arquivo de Desktop.ini é atribuir um ícone personalizado ou uma imagem em miniatura a uma pasta. Você também pode usar Desktop.ini para criar um *InfoTip* que exibe informações sobre a pasta e controla alguns aspectos do comportamento da pasta, como especificar nomes localizados para a pasta ou os itens na pasta.

**Use o procedimento a seguir para personalizar o estilo de uma pasta com Desktop.ini:**

1.  Use [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) para tornar a pasta uma pasta do sistema. Isso define o bit somente leitura na pasta para indicar que o comportamento especial reservado para Desktop.ini deve ser habilitado. Você também pode tornar uma pasta de uma pasta do sistema a partir da linha de comando usando **attrib + s** *nome_da_pasta*.
2.  Crie um arquivo de Desktop.ini para a pasta. Você deve marcá-lo como *oculto* e *sistema* para garantir que ele fique oculto dos usuários normais.
3.  Verifique se o arquivo de Desktop.ini que você cria está no formato Unicode. Isso é necessário para armazenar as cadeias de caracteres localizadas que podem ser exibidas aos usuários.

### <a name="creating-a-desktopini-file"></a>Criando um arquivo de Desktop.ini

O arquivo de Desktop.ini é um arquivo de texto que permite especificar como uma pasta do sistema de arquivos é exibida. O \[ . ShellClassInfo \] seção, permite que você personalize a exibição da pasta atribuindo valores a várias entradas:

|                   |                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Entrada**         | **Valor**                                                                                                                                                                                                                                                                                                                                                                      |
| **ConfirmFileOp** | Defina essa entrada como 0 para evitar um aviso "você está excluindo uma pasta do sistema" ao excluir ou mover a pasta.                                                                                                                                                                                                                                                                  |
| **Nosharing**     | Sem suporte no Windows Vista ou posterior. Defina essa entrada como 1 para impedir que a pasta seja compartilhada.                                                                                                                                                                                                                                                                       |
| **Ícone**      | Se você quiser especificar um ícone personalizado para a pasta, defina essa entrada como o nome do arquivo do ícone. A extensão de nome de arquivo. ico é preferida, mas também é possível especificar arquivos. bmp ou. exe e. dll que contêm ícones. Se você usar um caminho relativo, o ícone estará disponível para as pessoas que exibirem a pasta pela rede. Você também deve definir a entrada **IconIndex** . |
| **IconIndex**     | Defina essa entrada para especificar o índice para um ícone personalizado. Se o arquivo atribuído a **IconFile** contiver apenas um único ícone, defina **IconIndex** como 0.                                                                                                                                                                                                                               |
| **InfoTip**       | Defina essa entrada como uma cadeia de caracteres de texto informativa. Ele é exibido como um InfoTip quando o cursor passa sobre a pasta. Se o usuário clicar na pasta, o texto das informações será exibido no bloco de informações da pasta, abaixo das informações padrão.                                                                                                                      |



 

As ilustrações a seguir são da pasta música com um arquivo de Desktop.ini personalizado. A pasta agora:

-   Tem um ícone personalizado.
-   Não exibirá um aviso "você está excluindo uma pasta do sistema" se a pasta for movida ou excluída.
-   Não pode ser compartilhada.
-   Exibe o texto informativo quando o cursor passa sobre a pasta.

As opções de pasta nas ilustrações a seguir são definidas para mostrar arquivos ocultos para que Desktop.ini seja visível. A pasta tem a seguinte aparência:

![captura de tela da pasta com o ícone personalizado](images/webview4.jpg)

Quando o cursor passa sobre a pasta, o InfoTip é exibido.

![captura de tela da pasta com um InfoTip](images/webview6.jpg)

O ícone personalizado substitui o ícone de pasta em todos os lugares em que o nome da pasta é exibido.

![captura de tela do ícone personalizado substituindo ícone de pasta](images/webview5.jpg)

O arquivo de desktop.ini a seguir foi usado para personalizar a pasta música, como visto nas ilustrações anteriores.


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



