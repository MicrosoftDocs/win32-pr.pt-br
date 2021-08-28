---
description: No Windows XP, a configuração por aplicativo substitui a configuração padrão e a configuração do editor por aplicativo.
ms.assetid: 5b55d12d-8805-4820-91af-5ef583de3463
title: Configuração por aplicativo no Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f07860a42951e073403e8145037074c35e6ec6a267736381f6beab385f3bb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127456"
---
# <a name="per-application-configuration-on-windows-xp"></a>Configuração por aplicativo no Windows XP

No Windows XP, a configuração por [](default-configuration.md) aplicativo substitui [](publisher-configuration.md) a configuração padrão e a configuração do editor por aplicativo. Isso redireciona a dependência de um aplicativo específico de uma versão de um assembly lado a lado para outra versão especificada do assembly.

> [!Note]  
> A partir do Windows Server 2003, a [](publisher-configuration.md) configuração por aplicativo substituirá [](application-configuration-files.md) a configuração do editor por aplicativo somente se o arquivo de configuração do aplicativo especificar *apply="no"* em **publisherPolicy** e houver uma entrada correspondente presente no banco de dados de Compatibilidade do Aplicativo. A configuração por aplicativo sempre substitui a [configuração padrão](default-configuration.md). Para obter informações, [consulte configuração por aplicativo.](per-application-configuration.md)

 

Uma configuração por aplicativo poderá se tornar necessária se a operação correta de um aplicativo específico exigir uma versão de assembly diferente da versão normalmente especificada como uma configuração padrão ou de editor. Por exemplo, uma atualização global da versão do assembly pelo publicador pode corrigir o assembly, mas quebrar esse aplicativo específico. Nesse caso, a configuração por aplicativo pode ser usada para permitir que o aplicativo continue a ser executado com a versão anterior do assembly. Outro exemplo, uma instalação service pack que contém [](publisher-configuration.md) uma atualização de assembly pode usar a configuração do editor para redirecionar as dependências de todos os aplicativos e assemblies no sistema da versão 1.0.0.0 para 1.0.1.0. Se houver um aplicativo que exija a versão 1.0.0.0 para funcionar corretamente, ele poderá ser redirecionado para a versão 1.0.0.0 usando a configuração por aplicativo.

Os administradores de aplicativos podem implementar uma configuração por aplicativo, por meio da definição e instalação de arquivos [de configuração de aplicativo.](application-configuration-files.md) Eles redirecionam um aplicativo específico da dependência de uma versão de um assembly lado a lado para a dependência de outra versão. [*Os arquivos de configuração*](/windows/desktop/Msi/a-gly) de aplicativo podem substituir [os](publisher-configuration-files.md) arquivos de configuração do editor e a configuração padrão especificada pelos [manifestos do](application-manifests.md) aplicativo e pelos [manifestos do assembly](assembly-manifests.md). O arquivo de configuração do aplicativo inclui informações usadas pelo carregador [**quando CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) é chamado.

Para configurar um aplicativo para substituir o manifesto do aplicativo e a configuração do editor, um desenvolvedor deve ter um arquivo de configuração de aplicativo. O arquivo de configuração do aplicativo é implantado e instalado na mesma pasta que o arquivo executável do aplicativo. Para uma listagem do esquema de arquivo, consulte Esquema de arquivo de [configuração de aplicativo](application-configuration-file-schema.md).

Observe que, se o aplicativo usar a configuração por aplicativo, ele não receberá correções de segurança importantes ou correções de bugs que o editor do assembly possa emitir como arquivos de configuração do editor. Um aplicativo que usa a configuração por aplicativo pode, portanto, permanecer inseguro ou continuar a funcionar incorretamente mesmo depois que um novo assembly com essas correções é aplicado ao sistema. Por esse motivo, os desenvolvedores de aplicativos nunca devem enviar um aplicativo com uma configuração por aplicativo. A configuração por aplicativo só deve ser usada por administradores corporativos como uma correção temporária quando o aplicativo é desfeito por uma configuração de editor. Nesse caso, a solução permanente é que os desenvolvedores do assembly e os desenvolvedores do aplicativo precisarão trabalhar juntos para garantir que os assemblies com a configuração do editor sejam totalmente compatíveis com versões anteriores.

A seguir está um exemplo de um arquivo de configuração de aplicativo. Para obter mais informações, consulte [Arquivos de configuração de aplicativo.](application-configuration-files.md)

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

 

 
