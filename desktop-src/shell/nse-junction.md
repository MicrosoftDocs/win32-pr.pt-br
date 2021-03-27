---
description: A raiz de uma extensão de namespace é normalmente exibida pelo Windows Explorer como uma pasta nos modos de exibição de árvore e de pasta.
title: Especificando o local de uma extensão de namespace
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2c1fdd5d-b359-4d5c-a20e-0622f3a1cb1d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7617c7361c5f2ae76331c5f1b59eb845f6806395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828910"
---
# <a name="specifying-a-namespace-extensions-location"></a>Especificando o local de uma extensão de namespace

A raiz de uma extensão de namespace é normalmente exibida pelo Windows Explorer como uma pasta nos modos de exibição de árvore e de pasta. Para que o Windows Explorer exiba os arquivos e as subpastas da extensão, você deve especificar onde a pasta raiz está localizada na hierarquia de namespace do Shell. Esse local é conhecido como ponto de *junção*.

-   [Usando pastas virtuais como pontos de junção](#using-virtual-folders-as-junction-points)
-   [Usando pastas do sistema de arquivos como pontos de junção](#using-file-system-folders-as-junction-points)
-   [Abrindo uma exibição de uma extensão de namespace](#opening-a-view-of-a-namespace-extension)

## <a name="using-virtual-folders-as-junction-points"></a>Usando pastas virtuais como pontos de junção

A maneira mais simples de definir o ponto de junção de uma extensão é tornar a pasta raiz uma subpasta de uma pasta virtual do sistema. Esse tipo de ponto de junção é chamado de *ponto de junção virtual*. As pastas **Desktop** e **meu computador** são os locais típicos para pontos de junção virtuais, mas você também pode definir um ponto de junção virtual em um computador remoto ou nas pastas **meus locais de rede**, **Internet Explorer** e **painel de controle** .

Para definir um ponto de junção virtual, crie uma subchave da chave que representa a pasta virtual apropriada e nomeie-a com a forma de cadeia de caracteres do identificador de classe da extensão (CLSID). O CLSID registrado seria exibido da seguinte maneira.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  Virtual Folder Name
                     NameSpace
                        {Extension CLSID}
                           (Default) = Junction Point Name
```

O *nome da pasta virtual* é uma das subchaves na tabela a seguir.



| Localização          | Nome da pasta virtual                        |
|-------------------|--------------------------------------------|
| Painel de Controle     | **ControlPanel**                           |
| Área de trabalho           | **Área de trabalho**                                |
| Rede inteira    | **NetworkNeighborhood** \\ **EntireNetwork** |
| Meu Computador       | **Meu**                             |
| Meus locais de rede | **NetworkNeighborhood**                    |
| Computador remoto   | **Computador_remoto**                         |
| Arquivos de usuários       | **UsersFiles**                             |



 

Extensões remotas devem ser inicializadas com [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).

## <a name="using-file-system-folders-as-junction-points"></a>Usando pastas do sistema de arquivos como pontos de junção

Há duas maneiras de definir pastas do sistema de arquivos como pontos de junção. A abordagem mais simples é criar uma pasta no local apropriado e acrescentar um ponto ao nome da pasta, seguido pelo formato da cadeia de caracteres do CLSID de sua extensão. Somente o nome da pasta ficará visível no Windows Explorer. O exemplo a seguir cria um ponto de junção com um nome de exibição de MyFolder.


```
MyFolder.{Extension CLSID}
```



Como alternativa, você pode definir uma pasta nomeada de forma convencional como um ponto de junção:

-   Tornando a pasta somente leitura.
-   Tornando a pasta uma pasta do sistema chamando [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).
-   Colocar um arquivo de Desktop.ini oculto na pasta que inclui o CLSID da extensão.

Desktop.ini é um arquivo de texto padrão que pode ser adicionado a qualquer pasta para personalizar determinados aspectos do comportamento da pasta. Para obter uma discussão geral sobre como usar esse arquivo, consulte [como personalizar pastas com Desktop.ini](how-to-customize-folders-with-desktop-ini.md). Para definir uma pasta como um ponto de junção, o \[ . \] A seção ShellClassInfo de Desktop.ini deve conter o CLSID da extensão da seguinte maneira:


```
[.ShellClassInfo]
CLSID={Extension CLSID}
```



## <a name="opening-a-view-of-a-namespace-extension"></a>Abrindo uma exibição de uma extensão de namespace

Quando um usuário navega em um ponto de junção, o Windows Explorer cria automaticamente uma exibição da pasta raiz. Você também pode criar uma exibição iniciando explicitamente Explorer.exe com o CLSID da extensão como um argumento. Você pode, por exemplo, usar essa abordagem para iniciar uma exibição de uma extensão de um menu de atalho ou atalho. Por exemplo, para iniciar uma exibição de MyExtension que inclui um modo de exibição de árvore, você pode usar a seguinte cadeia de caracteres de comando.


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID}
```



Uma cadeia de caracteres de comando alternativa pode ser usada para iniciar uma exibição de um objeto dentro da extensão. Esse recurso seria útil, por exemplo, para uma extensão que usa uma exibição de pasta para permitir que os usuários exibam o conteúdo de um dos vários arquivos compactados.


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID},objectname
```



O parâmetro *objectname* é o nome do objeto a ser exibido. O Windows Explorer converte o nome para seu PIDL correspondente e passa o PIDL para o método [**IPersistFolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) do novo objeto de pasta.

> [!Note]  
> A cadeia de caracteres CLSID deve ser precedida por um par de dois-pontos (::) ou o comando falhará. O sinalizador de barra e (/e) usado nas duas linhas de comando de exemplo mostradas anteriormente instrui o Windows Explorer a exibir um modo de exibição de árvore. O sinalizador deve ser separado dos dois dois-pontos por uma vírgula. Se você não quiser um modo de exibição de árvore, omita o sinalizador/e e a vírgula.

 

 

 



