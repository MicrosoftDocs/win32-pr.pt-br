---
description: Um assembly privado é um assembly implantado com um aplicativo e está disponível para uso exclusivo desse aplicativo.
ms.assetid: 5E0E7423-85BD-4ED0-9149-9541F4D2371F
title: Sobre assemblies privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c785b30ca8654071a9816aaf9a11ecc69a029f605d06f39f44a6a490a2a7aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142609"
---
# <a name="about-private-assemblies"></a>Sobre assemblies privados

Um assembly privado é um assembly implantado com um aplicativo e está disponível para uso exclusivo desse aplicativo. Ou seja, outros aplicativos não compartilham o assembly privado. Assemblies privados são um dos métodos que podem ser usados para criar [aplicativos isolados.](isolated-applications.md) Para obter mais informações, consulte [Sobre aplicativos isolados e assemblies lado a lado.](about-isolated-applications-and-side-by-side-assemblies.md)

Assemblies privados devem ser projetados para trabalhar lado a lado com outras versões do assembly no sistema. Para obter mais informações, [consulte Diretrizes para criar assemblies](guidelines-for-creating-side-by-side-assemblies.md)lado a lado.

Assemblies privados devem ser acompanhados por um [manifesto do assembly](assembly-manifests.md). Observe que as restrições de nome se aplicam ao empacotar uma DLL como um assembly privado para acomodar a maneira como Windows pesquisa assemblies privados. Ao pesquisar assemblies privados, o método recomendado é incluir o manifesto do assembly na DLL como um recurso. Nesse caso, a ID do recurso deve ser igual a 1 e o nome do assembly privado pode ser o mesmo que o nome da DLL. Por exemplo, se o nome da DLL for MICROSOFT.WINDOWS.MYSAMPLE.DLL, o valor do atributo name usado no **elemento assemblyIdentity** do manifesto também poderá ser Microsoft. Windows.mysample. Um método alternativo de pesquisa de assemblies privados é fornecer o manifesto do assembly em um arquivo separado. Nesse caso, o nome do assembly e seu manifesto devem ser diferentes do nome da DLL. Por exemplo, Microsoft. Windows.mysampleAsm, Microsoft. Windows.mysampleAsm.manifest e Microsoft.Windows.mysample.dll. Para obter mais informações sobre como pesquisas lado a lado para assemblies privados, consulte [Sequência de pesquisa de assembly](assembly-searching-sequence.md).

Assemblies privados são instalados em uma pasta da estrutura de diretório do aplicativo. Normalmente, essa é a pasta que contém o arquivo executável do aplicativo. Assemblies privados podem ser implantados na mesma pasta que o aplicativo, em uma pasta com o mesmo nome que o assembly ou em uma subpasta específica do idioma com o mesmo nome que o assembly. Por exemplo, use uma das estruturas de diretório a seguir para implantar um assembly privado, Microsoft.tools.pop, sem nenhuma linguagem especificada.



| Estrutura do diretório                                       | Descrição                                                                                            |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| APPDIR \\MICROSOFT.TOOLS.POP.DLL                           | O manifesto é implantado como um recurso na DLL.                                                     |
| Appdir \\ Microsoft.Tools.Pop.MANIFEST                      | O manifesto é implantado como um arquivo separado.                                                           |
| APPDIR \\ MICROSOFT. Ferramentas. POP \\MICROSOFT.TOOLS.POP.DLL      | O manifesto é implantado como um recurso na DLL, que está em uma subpasta com o nome do assembly. |
| Appdir \\ Microsoft.Tools.Pop \\ Microsoft.Tools.Pop.MANIFEST | O manifesto é implantado como um arquivo separado em uma subpasta que tem o nome do assembly.                 |



 

> [!IMPORTANT]
>
> Para versões do sistema operacional Windows antes do Windows 7 e do Windows Server 2008 R2, os assemblies privados nativos devem ser implantados na pasta que contém o arquivo executável do aplicativo. Não há suporte para a instalação em uma pasta específica do idioma ou na pasta com o mesmo nome que o assembly para assemblies privados nativos.

 

Use uma das estruturas de diretório a seguir para implantar um assembly privado, Microsoft.tools.pop, com uma linguagem especificada. No exemplo a seguir, o idioma usado por Microsoft.Tools.Pop é inglês (Estados Unidos) e o código de idioma é en-us. Você deve substituir o código de linguagem DHTML correto para o assembly.

``` syntax
appdir\en-us\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop.MANIFEST
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.MANIFEST
```

Assemblies privados podem ser instalados por qualquer método de instalação que possa copiar o arquivo do assembly para essa pasta, como o **comando xcopy.** Para obter mais informações sobre como instalar assemblies privados usando o instalador Windows, consulte [Instalação de assemblies Win32](../msi/installation-of-win32-assemblies.md).

Assemblies privados também podem ser instalados em sistemas operacionais anteriores Windows XP. Nesse caso, o assembly deve ser registrado e nesses sistemas operacionais o manifesto não é usado. Uma cópia do assembly privado é instalada em uma pasta privada para uso exclusivo do aplicativo. Outra versão do assembly pode ser registrada globalmente no sistema e disponível para qualquer aplicativo que se a bind a ele. A versão global do assembly pode ser a versão instalada com o aplicativo ou uma versão anterior. Para obter mais informações, [consulte Redirecionamento de DLL/COM Windows](dll-com-redirection-on-windows.md). Um assembly também pode ser instalado como um assembly compartilhado para uso por vários aplicativos. Para obter mais informações, consulte [Assemblies compartilhados](/windows/desktop/Msi/shared-assemblies).

Observe que as etapas para criar um assembly privado são idênticas àquelas para criar um assembly compartilhado com duas exceções:

-   Um assembly privado não precisa ser assinado e **publickeyToken** não é necessário no **elemento assemblyIdentity** do manifesto do assembly.
-   Assemblies privados podem ser instalados na pasta do aplicativo usando qualquer tecnologia de instalação. Assemblies privados não precisam ser instalados usando o Windows Instalador.

 

 
