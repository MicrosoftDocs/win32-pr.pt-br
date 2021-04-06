---
description: Use o procedimento a seguir para desenvolver um novo aplicativo ou atualizar um aplicativo existente, para usar os assemblies lado a lado disponíveis da Microsoft ou de outros publicadores de assembly lado a lado.
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: Usando assemblies lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1992562a0868918de2901a7ca88033784af6ef1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826995"
---
# <a name="using-side-by-side-assemblies"></a>Usando assemblies lado a lado

Use o procedimento a seguir para desenvolver um novo aplicativo ou atualizar um aplicativo existente, para usar os [assemblies](about-side-by-side-assemblies-.md) lado a lado disponíveis da Microsoft ou de outros publicadores de assembly lado a lado. Para obter uma lista dos assemblies lado a lado fornecidos atualmente pela Microsoft, consulte [assemblies lado a lado da Microsoft com suporte](supported-microsoft-side-by-side-assemblies.md). Observe que o aplicativo deve ser executado em pelo menos o Windows XP para instalar os assemblies como assemblies lado a lado. Para obter mais informações, consulte [diretrizes para criar assemblies lado a lado](guidelines-for-creating-side-by-side-assemblies.md).

**Para adicionar um assembly lado a lado a um aplicativo**

1.  Identifique os assemblies lado a lado que seu aplicativo requer. A partir do Windows XP, esses assemblies lado a lado e seus manifestos de assembly são instalados com o sistema operacional, mas não são registrados globalmente.
2.  Use um editor de XML para criar um [manifesto de aplicativo](application-manifests.md). Consulte o exemplo de manifesto do aplicativo abaixo. Para obter mais informações, consulte [manifestos do aplicativo](application-manifests.md) na [referência de arquivos de manifesto](manifest-files-reference.md).
3.  Insira valores de atributo no subelemento [*AssemblyIdentity do contexto def*](d-sbscs-gly.md) do manifesto do aplicativo que define exclusivamente o aplicativo. Para obter mais informações sobre o **AssemblyIdentity** de contexto def, consulte [manifestos do aplicativo](application-manifests.md).
4.  Se o assembly contiver assemblies dependentes, insira valores de atributo nos subelementos de [*AssemblyIdentity de contexto de referência*](r-sbscs-gly.md) correspondente do manifesto do aplicativo. Para obter mais informações sobre o **AssemblyIdentity** de contexto de referência, consulte [manifestos de aplicativo](application-manifests.md).

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  Você pode incluir o manifesto do aplicativo no arquivo de cabeçalho executável binário do aplicativo.

    Nesse caso, adicione também a seguinte linha ao arquivo de cabeçalho do aplicativo:

    <dl> Manifesto de ID de recurso de manifesto de CREATEPROCESS \_ \_ \_ \_ "YourApp.exe. manifest"  
    </dl>

    Como alternativa, você pode posicionar um arquivo de manifesto separado no mesmo diretório que o arquivo executável do aplicativo. O sistema operacional carrega o manifesto do sistema de arquivos primeiro e, em seguida, verifica a seção de recursos do executável. A versão do sistema de arquivos tem precedência.

6.  Os [assemblies compartilhados](/windows/desktop/Msi/shared-assemblies) devem ser instalados usando o [Windows Installer](../msi/windows-installer-portal.md) versão 2,0. Crie um pacote de Windows Installer conforme descrito em [como instalar assemblies do Win32 para compartilhamento lado a lado no Windows XP?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).
7.  Os [assemblies privados](/windows/desktop/Msi/private-assemblies) podem ser instalados usando o [Windows Installer](../msi/windows-installer-portal.md) versão 2,0. Crie um pacote de Windows Installer conforme descrito em [como instalar assemblies do Win32 para o uso particular de um aplicativo no Windows XP?](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md). Você também pode usar qualquer outro instalador para copiar um assembly privado e seu manifesto na mesma pasta que o arquivo executável do aplicativo.
8.  Teste seu aplicativo para garantir os resultados. Observe que seu computador de teste não deve ter o assembly lado a lado registrado.
9.  Implante seu aplicativo ou atualize-o como um pacote Windows Installer.

## <a name="example-application-manifest"></a>Exemplo de manifesto do aplicativo

Veja a seguir um exemplo de um manifesto de aplicativo:

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity type="win32" name="Microsoft.Windows.mysampleapp" version="1.0.0.0" processorArchitecture="x86"/>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="a5aaf5ba15723d5"/>
    </dependentAssembly>
  </dependency>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Tools.MyPrivateDll" version="2.5.0.0" processorArchitecture="x86"/>
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
