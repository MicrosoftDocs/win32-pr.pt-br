---
description: No Windows XP, a configuração por aplicativo substitui a configuração padrão e a configuração do editor em uma base por aplicativo.
ms.assetid: 5b55d12d-8805-4820-91af-5ef583de3463
title: Configuração por aplicativo no Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6fa2e14e24e48be84247a23feecddf2784fbc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829777"
---
# <a name="per-application-configuration-on-windows-xp"></a>Configuração por aplicativo no Windows XP

No Windows XP, a configuração por aplicativo substitui a configuração [padrão](default-configuration.md) e a [configuração do editor](publisher-configuration.md) em uma base por aplicativo. Isso redireciona a dependência de um aplicativo específico de uma versão de um assembly lado a lado para outra versão especificada do assembly.

> [!Note]  
> A partir do Windows Server 2003, a configuração por aplicativo substitui a [configuração do editor](publisher-configuration.md) em uma base por aplicativo somente se o arquivo de [configuração do aplicativo](application-configuration-files.md) especifica *Apply = "no"* em **publisherPolicy Apply** e há uma entrada correspondente presente no banco de dados de compatibilidade de aplicativos. A configuração por aplicativo sempre substitui a [configuração padrão](default-configuration.md). Para obter informações [, consulte configuração por aplicativo](per-application-configuration.md).

 

Uma configuração por aplicativo pode se tornar necessária se a operação correta de um aplicativo específico exigir uma versão de assembly diferente da versão normalmente especificada como uma configuração padrão ou de Publicador. Por exemplo, uma atualização global da versão do assembly pelo Publicador pode corrigir o assembly, mas interromper esse aplicativo específico. Nesse caso, a configuração por aplicativo pode ser usada para permitir que o aplicativo continue a ser executado com a versão anterior do assembly. Outro exemplo, um service pack instalação que contém uma atualização de assembly pode usar a [configuração do editor](publisher-configuration.md) para redirecionar as dependências de todos os aplicativos e assemblies no sistema da versão 1.0.0.0 para 1.0.1.0. Se houver um aplicativo que exija que a versão 1.0.0.0 funcione corretamente, ele poderá ser redirecionado para a versão 1.0.0.0 usando a configuração por aplicativo.

Os administradores de aplicativos podem implementar uma configuração por aplicativo Criando e instalando [arquivos de configuração de aplicativo](application-configuration-files.md). Eles redirecionam um aplicativo específico de dependência em uma versão de um assembly lado a lado para dependência de outra versão. Os arquivos de [*configuração do aplicativo*](/windows/desktop/Msi/a-gly) podem substituir os arquivos de [configuração do Publicador](publisher-configuration-files.md) e a configuração padrão especificada por [manifestos de aplicativo](application-manifests.md) e [manifestos de assembly](assembly-manifests.md). O arquivo de configuração do aplicativo inclui informações usadas pelo carregador quando [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) é chamado.

Para configurar um aplicativo para substituir o manifesto do aplicativo e a configuração do Publicador, um desenvolvedor deve criar um arquivo de configuração de aplicativo. O arquivo de configuração de aplicativo é então implantado e instalado na mesma pasta que o arquivo executável do aplicativo. Para obter uma lista do esquema de arquivo, consulte [esquema de arquivo de configuração de aplicativo](application-configuration-file-schema.md).

Observe que, se seu aplicativo usar a configuração por aplicativo, ele não receberá correções de segurança importantes ou correções de bugs que o editor do assembly pode emitir como arquivos de configuração do Publicador. O aplicativo que usa a configuração por aplicativo pode, portanto, permanecer inseguro ou continuar a funcionar incorretamente mesmo depois que um novo assembly com essas correções for aplicado ao sistema. Por esse motivo, os desenvolvedores de aplicativos nunca devem enviar um aplicativo com uma configuração por aplicativo. A configuração por aplicativo só deve ser usada por administradores corporativos como uma correção temporária quando o aplicativo é interrompido por uma configuração de Publicador. Nesse caso, a solução permanente é que os desenvolvedores do assembly e os desenvolvedores do aplicativo precisarão trabalhar juntos para garantir que os assemblies com a configuração do Publicador sejam totalmente compatíveis com versões anteriores.

Veja a seguir um exemplo de um arquivo de configuração de aplicativo. Para obter mais informações, consulte [arquivos de configuração do aplicativo](application-configuration-files.md).

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<configuration>
  <windows>
    <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
      <assemblyIdentity 
          name="Microsoft.Windows.mysampleApp" 
          processorArchitecture="x86" 
          version="1.0.0.0" type="win32"/>
        <dependentAssembly>
          <assemblyIdentity type="win32" 
              name="Microsoft.Windows.SampleAssembly" 
              processorArchitecture="x86" 
              publicKeyToken="0000000000000000"/>
          <bindingRedirect 
              oldVersion="2.0.0.0" 
              newVersion="2.0.1.0"/>
        </dependentAssembly>
    </assemblyBinding>
   </windows>
</configuration>
```

 

 
