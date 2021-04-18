---
description: Um assembly privado é um assembly que é implantado com um aplicativo e está disponível para uso exclusivo desse aplicativo.
ms.assetid: 5E0E7423-85BD-4ED0-9149-9541F4D2371F
title: Sobre assemblies privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7ccfe8c63a8435a33085f607c2040a0a42345c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751931"
---
# <a name="about-private-assemblies"></a>Sobre assemblies privados

Um assembly privado é um assembly que é implantado com um aplicativo e está disponível para uso exclusivo desse aplicativo. Ou seja, outros aplicativos não compartilham o assembly particular. Os assemblies privados são um dos métodos que podem ser usados para criar [aplicativos isolados](isolated-applications.md). Para obter mais informações, consulte [sobre aplicativos isolados e assemblies lado a lado](about-isolated-applications-and-side-by-side-assemblies.md).

Os assemblies privados devem ser projetados para funcionar lado a lado com outras versões do assembly no sistema. Para obter mais informações, consulte [diretrizes para criar assemblies lado a lado](guidelines-for-creating-side-by-side-assemblies.md).

Assemblies privados devem ser acompanhados por um [manifesto do assembly](assembly-manifests.md). Observe que as restrições de nome se aplicam ao empacotar uma DLL como um assembly privado para acomodar a maneira como o Windows procura assemblies particulares. Ao pesquisar assemblies particulares, o método recomendado é incluir o manifesto do assembly na DLL como um recurso. Nesse caso, a ID do recurso deve ser igual a 1 e o nome do assembly privado pode ser o mesmo que o nome da DLL. Por exemplo, se o nome da DLL for MICROSOFT.WINDOWS.MYSAMPLE.DLL, o valor do atributo name usado no elemento **AssemblyIdentity** do manifesto também poderá ser Microsoft. Windows. MySample. Um método alternativo de Pesquisar assemblies privados é fornecer o manifesto do assembly em um arquivo separado. Nesse caso, o nome do assembly e seu manifesto devem ser diferentes do nome da DLL. Por exemplo, Microsoft. Windows. mysampleAsm, Microsoft. Windows. mysampleAsm. manifest e Microsoft.Windows.mysample.dll. Para obter mais informações sobre como as pesquisas lado a lado de assemblies privados, consulte [sequência de pesquisa de assembly](assembly-searching-sequence.md).

Os assemblies privados são instalados em uma pasta da estrutura de diretórios do aplicativo. Normalmente, essa é a pasta que contém o arquivo executável do aplicativo. Os assemblies privados podem ser implantados na mesma pasta que o aplicativo, em uma pasta com o mesmo nome que o assembly ou em uma subpasta específica de idioma com o mesmo nome que o assembly. Por exemplo, use uma das seguintes estruturas de diretório para implantar um assembly privado, Microsoft. Tools. pop, sem nenhum idioma especificado.



| Estrutura do diretório                                       | Descrição                                                                                            |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| \\MICROSOFT.TOOLS.POP.DLL appdir                           | O manifesto é implantado como um recurso na DLL.                                                     |
| Appdir \\ Microsoft. Tools. Popup. manifest                      | O manifesto é implantado como um arquivo separado.                                                           |
| APPDIR \\ Microsoft. Ferramentas. \\MICROSOFT.TOOLS.POP.DLL pop      | O manifesto é implantado como um recurso na DLL, que está em uma subpasta com o nome do assembly. |
| Appdir \\ Microsoft. Tools. pop \\ Microsoft. Tools. Popup. manifest | O manifesto é implantado como um arquivo separado em uma subpasta que tem o nome do assembly.                 |



 

> [!IMPORTANT]
>
> Para versões do sistema operacional Windows antes do Windows 7 e do Windows Server 2008 R2, os assemblies privados nativos devem ser implantados na pasta que contém o arquivo executável do aplicativo. A instalação em uma pasta específica de idioma ou na pasta com o mesmo nome que o assembly não tem suporte para assemblies particulares nativos.

 

Use uma das seguintes estruturas de diretório para implantar um assembly privado, Microsoft. Tools. pop, com um idioma especificado. No exemplo a seguir, o idioma usado por Microsoft. Tools. pop é inglês (Estados Unidos) e o código de idioma é en-US. Você deve substituir o código de idioma DHTML correto para seu assembly.

``` syntax
appdir\en-us\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop.MANIFEST
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.MANIFEST
```

Os assemblies privados podem ser instalados por qualquer método de instalação que possa copiar o arquivo do assembly para essa pasta, como o comando **xcopy** . Para obter mais informações sobre como instalar assemblies privados usando o Windows Installer, consulte [instalação de assemblies do Win32](../msi/installation-of-win32-assemblies.md).

Os assemblies privados também podem ser instalados em sistemas operacionais anteriores ao Windows XP. Nesse caso, o assembly deve ser registrado e, nesses sistemas operacionais, o manifesto não é usado. Uma cópia do assembly privado é instalada em uma pasta particular para o uso exclusivo do aplicativo. Outra versão do assembly pode ser registrada globalmente no sistema e disponível para qualquer aplicativo que se vincule a ele. A versão global do assembly pode ser a versão instalada com o aplicativo ou uma versão anterior. Para obter mais informações, consulte [redirecionamento de dll/com no Windows](dll-com-redirection-on-windows.md). Um assembly também pode ser instalado como um assembly compartilhado para uso por vários aplicativos. Para obter mais informações, consulte [assemblies compartilhados](/windows/desktop/Msi/shared-assemblies).

Observe que as etapas para criar um assembly privado são idênticas àquelas para criar um assembly compartilhado com duas exceções:

-   Um assembly privado não precisa ser assinado e o **publickeyToken** não é necessário no elemento **AssemblyIdentity** do manifesto do assembly.
-   Os assemblies privados podem ser instalados na pasta do aplicativo usando qualquer tecnologia de instalação. Não é necessário instalar assemblies privados usando o Windows Installer.

 

 
