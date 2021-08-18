---
description: Use o procedimento a seguir para desenvolver um novo aplicativo ou atualizar um aplicativo existente para usar os assemblies lado a lado disponíveis da Microsoft ou de outros editores de assembly lado a lado.
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: Usando assemblies lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60170dc4873f03dfc17769f91106e02b591e0b1db81695d773a35b392a2c7dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141709"
---
# <a name="using-side-by-side-assemblies"></a>Usando assemblies lado a lado

Use o procedimento a seguir para desenvolver um novo aplicativo ou atualizar um aplicativo existente para usar os [assemblies](about-side-by-side-assemblies-.md) lado a lado disponíveis da Microsoft ou de outros editores de assembly lado a lado. Para ver uma lista dos assemblies lado a lado atualmente fornecidos pela Microsoft, consulte Assemblies lado a lado da [Microsoft com suporte.](supported-microsoft-side-by-side-assemblies.md) Observe que o aplicativo deve ser executado em pelo menos Windows XP para instalar os assemblies como assemblies lado a lado. Para obter mais informações, [consulte Diretrizes para criar assemblies](guidelines-for-creating-side-by-side-assemblies.md)lado a lado.

**Para adicionar um assembly lado a lado a um aplicativo**

1.  Identifique os assemblies lado a lado que seu aplicativo requer. Começando com Windows XP, esses assemblies lado a lado e seus manifestos de assembly são instalados com o sistema operacional, mas não são registrados globalmente.
2.  Use um editor XML para criar um manifesto [do aplicativo](application-manifests.md). Consulte o manifesto do aplicativo de exemplo abaixo. Para obter mais informações, consulte [Manifestos de aplicativo na](application-manifests.md) Referência [de arquivos de manifesto](manifest-files-reference.md).
3.  Insira valores de atributo no subelemento [*assembly de contexto DEFIdentity*](d-sbscs-gly.md) do manifesto do aplicativo que define exclusivamente o aplicativo. Para obter mais informações sobre o assembly de contexto de **DEFIdentity**, consulte [Manifestos do aplicativo](application-manifests.md).
4.  Se o assembly contiver assemblies dependentes, insira valores de atributo no assembly de contexto [*REFIdentity*](r-sbscs-gly.md) correspondente subelementos do manifesto do aplicativo. Para obter mais informações sobre o assembly de contexto **REFIdentity**, consulte [Manifestos do aplicativo](application-manifests.md).

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  Você pode incluir o manifesto do aplicativo no arquivo de header executável binário do aplicativo.

    Nesse caso, adicione também a seguinte linha ao arquivo de header do aplicativo:

    <dl> CREATEPROCESS \_ MANIFEST \_ RESOURCE \_ ID RT \_ MANIFEST "YourApp.exe.manifest"  
    </dl>

    Como alternativa, você pode colocar um arquivo de manifesto separado no mesmo diretório que o arquivo executável do aplicativo. O sistema operacional carrega o manifesto do sistema de arquivos primeiro e, em seguida, verifica a seção de recursos do executável. A versão do sistema de arquivos tem precedência.

6.  [Assemblies compartilhados](/windows/desktop/Msi/shared-assemblies) devem ser instalados usando o [Windows Installer](../msi/windows-installer-portal.md) versão 2.0. Autor de um Windows instalador de dados conforme descrito em [How Do I Install Win32 Assemblies for Side-by-side Sharing on Windows XP?.](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).
7.  [Assemblies privados](/windows/desktop/Msi/private-assemblies) podem ser instalados usando o [Windows Installer](../msi/windows-installer-portal.md) versão 2.0. Autor de um Windows instalador de dados conforme descrito em [How Do I Install Win32 Assemblies](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)for the Private Use of an Application on Windows XP? . Você também pode usar qualquer outro instalador para copiar um assembly privado e seu manifesto na mesma pasta que o arquivo executável do aplicativo.
8.  Teste seu aplicativo para garantir os resultados. Observe que o computador de teste não deve ter o assembly lado a lado registrado.
9.  Implante seu aplicativo ou atualize como um Windows instalador.

## <a name="example-application-manifest"></a>Manifesto do aplicativo de exemplo

Veja a seguir um exemplo de um manifesto do aplicativo:

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

 

 
