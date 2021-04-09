---
description: A configuração por aplicativo redireciona a dependência de um aplicativo específico de uma versão de um assembly lado a lado para outra versão do assembly.
ms.assetid: b7988385-c87e-443c-8ec3-84ab3c172eab
title: Configuração por aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b17543c9972deefe2a2beda1f5eeba1c5ace2ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171283"
---
# <a name="per-application-configuration"></a>Configuração por aplicativo

A configuração por aplicativo redireciona a dependência de um aplicativo específico de uma versão de um assembly lado a lado para outra versão do assembly. Uma configuração por aplicativo pode se tornar necessária se a operação correta de um aplicativo específico exigir uma versão de assembly diferente da versão normalmente especificada como configuração [padrão](default-configuration.md) ou [configuração de Publicador](publisher-configuration.md). Por exemplo, uma atualização global da versão do assembly pelo Publicador pode corrigir o assembly, mas interromper esse aplicativo específico. Nesse caso, a configuração por aplicativo pode ser usada para permitir que o aplicativo continue a ser executado com a versão anterior do assembly.

A partir do Windows Server 2003, a configuração por aplicativo sempre substitui a [configuração padrão](default-configuration.md) por aplicativo. A configuração por aplicativo substitui a [configuração do editor](publisher-configuration.md) em uma base por aplicativo somente se o arquivo de configuração do [aplicativo](application-configuration-files.md) especificar *Apply = "no"* em **publisherPolicy Apply** e houver uma entrada correspondente presente no banco de dados de compatibilidade de aplicativos.

> [!Note]  
> No Windows XP, a configuração por aplicativo substitui a configuração [padrão](default-configuration.md) e a [configuração do editor](publisher-configuration.md) em uma base por aplicativo. Para obter informações, consulte [configuração por aplicativo no Windows XP](per-application-configuration-on-windows-xp.md).

 

A partir do Windows Server 2003, uma configuração por aplicativo substituirá uma [configuração de Publicador](publisher-configuration.md) se o [arquivo de configuração de aplicativo](application-configuration-files.md) especificar *Apply = "Yes"* em **publisherPolicy Apply** e o sinalizador EnableAppConfig for definido para o aplicativo no banco de dados de compatibilidade de aplicativos. Essa capacidade de substituir uma configuração de Publicador usando uma configuração por aplicativo permite que o aplicativo seja executado em modo de modo de execução. Para obter mais informações sobre o banco de dados e a compatibilidade de aplicativos, consulte o kit de ferramentas de compatibilidade de aplicativos do Windows. Você pode obter o kit de ferramentas de compatibilidade de aplicativos do Windows a partir do [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/) .

> [!Note]  
> Se você enviar componentes com um [arquivo de configuração de aplicativo](application-configuration-files.md) (arquivo. config) que especifica *Apply = "no"* em **publisherPolicy Apply**, isso fará com que a geração do contexto de ativação falhe. A configuração por aplicativo será ignorada se você enviar componentes com um arquivo. config especificando *Apply = "Yes"* em **publisherPolicy Apply**.

 

Os administradores de aplicativos podem implementar uma configuração por aplicativo Criando e instalando arquivos de configuração de aplicativos e atualizando o banco de dados de compatibilidade de aplicativos. O arquivo de configuração de aplicativo deve ser implantado e instalado na mesma pasta que o arquivo executável do aplicativo. Para obter uma lista do esquema de arquivo, consulte [esquema de arquivo de configuração de aplicativo](application-configuration-file-schema.md). O banco de dados de compatibilidade de aplicativos deve ser distribuído conforme descrito no kit de ferramentas de compatibilidade de aplicativos.

> [!Note]  
> Se seu aplicativo for executado em modo de segurança, ele não receberá correções importantes ou correções de bugs que o editor do assembly pode emitir como arquivos de configuração do Publicador. O aplicativo que usa a configuração por aplicativo pode, portanto, permanecer inseguro ou continuar a funcionar incorretamente mesmo depois que um novo assembly com essas correções for aplicado ao sistema. Por esse motivo, os desenvolvedores de aplicativos nunca devem enviar um aplicativo com uma configuração por aplicativo. A configuração por aplicativo só deve ser usada por administradores corporativos como uma correção temporária quando o aplicativo é interrompido por uma configuração de Publicador. Nesse caso, a solução permanente é que os desenvolvedores do assembly e os desenvolvedores do aplicativo precisarão trabalhar juntos para garantir que os assemblies com a configuração do Publicador sejam totalmente compatíveis com versões anteriores.

 

Veja a seguir um exemplo de um arquivo de configuração de aplicativo. Para obter mais informações, consulte arquivos de configuração do aplicativo.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<configuration>
 <windows>
  <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity  processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
   <publisherPolicy apply="no"/>                     
   <dependentAssembly>
    <assemblyIdentity type="win32" processorArchitecture="x86" name="Microsoft.Windows.SampleAssembly" publicKeyToken="0000000000000000"/>
    <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
   </dependentAssembly>
  </assemblyBinding>
 </windows>
</configuration>
```

O administrador do aplicativo deve adicionar as entradas necessárias ao banco de dados de compatibilidade de aplicativos. Baixe e instale o kit de ferramentas de compatibilidade de aplicativos do Windows 2,6 do [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/) . Crie um novo personalizado ou atualize seu banco de dados existente usando o administrador de compatibilidade conforme descrito no kit de ferramentas. A correção de compatibilidade que você deseja escolher para a camada de compatibilidade para seu aplicativo é EnableAppConfig. Você deve sempre testar os aplicativos antes de instalar um novo banco de dados de compatibilidade.

 

 



