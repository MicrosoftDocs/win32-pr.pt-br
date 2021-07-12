---
description: Personalização da aparência e do comportamento de uma pasta individual com Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Como personalizar pastas com Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a671b169c4b025683cdd220ee3a920b4d592488
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581744"
---
# <a name="how-to-customize-folders-with-desktopini"></a>Como personalizar pastas com Desktop.ini

As pastas do sistema de arquivos normalmente são exibidas com um ícone padrão e um conjunto de propriedades, que especificam, por exemplo, se a pasta é compartilhada. Você pode personalizar a aparência e o comportamento de uma pasta individual criando um arquivo Desktop.ini para essa pasta.

## <a name="instructions"></a>Instruções

### <a name="using-desktopini-files"></a>Usando Desktop.ini arquivos

As pastas normalmente são exibidas com o ícone de pasta padrão. Um uso comum do arquivo Desktop.ini é atribuir um ícone personalizado ou uma imagem em miniatura a uma pasta. Você também pode usar Desktop.ini para criar uma *infotip* que exibe informações sobre a pasta e controla alguns aspectos do comportamento da pasta, como especificar nomes localizados para a pasta ou itens na pasta.

**Use o procedimento a seguir para personalizar o estilo de uma pasta com Desktop.ini:**

1.  Use [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) para tornar a pasta uma pasta do sistema. Isso define o bit somente leitura na pasta para indicar que o comportamento especial reservado para Desktop.ini deve ser habilitado. Você também pode tornar uma pasta do sistema uma pasta do sistema na linha de comando usando **atrib +s** *FolderName.*
2.  Crie um Desktop.ini para a pasta. Você deve marcá-lo *como oculto* *e sistema* para garantir que ele seja oculto dos usuários normais.
3.  Certifique-se de Desktop.ini arquivo que você cria está no formato Unicode. Isso é necessário para armazenar as cadeias de caracteres localizadas que podem ser exibidas aos usuários.

### <a name="creating-a-desktopini-file"></a>Criando um arquivo Desktop.ini dados

O Desktop.ini arquivo é um arquivo de texto que permite que você especifique como uma pasta do sistema de arquivos é exibida. O \[ . A seção ShellClassInfo permite personalizar a exibição da pasta \] atribuindo valores a várias entradas:

| Valor             | Descrição                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ConfirmFileOp** | De definir essa entrada como 0 para evitar um aviso "Você está excluindo uma pasta do sistema" ao excluir ou mover a pasta.                                                                                                                                                                                                                                                                  |
| **NoSharing**     | Não há suporte no Windows Vista ou posterior. De definir essa entrada como 1 para impedir que a pasta seja compartilhada.                                                                                                                                                                                                                                                                       |
| **Iconfile**      | Se você quiser especificar um ícone personalizado para a pasta, de definir essa entrada como o nome de arquivo do ícone. A extensão de nome de arquivo .ico é preferencial, mas também é possível especificar arquivos .bmp ou arquivos .exe e .dll que contêm ícones. Se você usar um caminho relativo, o ícone estará disponível para as pessoas que visualizam a pasta pela rede. Você também deve definir a **entrada IconIndex.** |
| **IconIndex**     | De definir essa entrada para especificar o índice de um ícone personalizado. Se o arquivo atribuído a **IconFile** contiver apenas um único ícone, de definir **IconIndex** como 0.                                                                                                                                                                                                                               |
| **InfoTip**       | De definir essa entrada como uma cadeia de caracteres de texto informacional. Ele é exibido como uma infotip quando o cursor fica sobre a pasta. Se o usuário clicar na pasta, o texto de informações será exibido no bloco de informações da pasta, abaixo das informações padrão.                                                                                                                      |



 

As ilustrações a seguir são da pasta Música com um arquivo Desktop.ini personalizado. A pasta agora:

-   Tem um ícone personalizado.
-   Não exibirá um aviso "Você está excluindo uma pasta do sistema" se a pasta for movida ou excluída.
-   Não pode ser compartilhada.
-   Exibe texto informacional quando o cursor fica sobre a pasta.

As opções de pasta nas ilustrações a seguir são definidas para mostrar arquivos ocultos para que Desktop.ini seja visível. A pasta tem esta aparência:

![captura de tela da pasta com o ícone personalizado](images/webview4.jpg)

Quando o cursor passar o mouse sobre a pasta, a infotip será exibida.

![captura de tela da pasta com uma infotip](images/webview6.jpg)

O ícone personalizado substitui o ícone de pasta em todos os lugares em que o nome da pasta é exibido.

![captura de tela do ícone personalizado substituindo o ícone de pasta](images/webview5.jpg)

O arquivo desktop.ini a seguir foi usado para personalizar a pasta Música, conforme visto nas ilustrações anteriores.


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



