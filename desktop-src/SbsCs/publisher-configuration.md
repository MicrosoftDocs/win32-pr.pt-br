---
description: Um arquivo de configuração do publicador redireciona globalmente aplicativos e assemblies que têm uma dependência em uma versão de um assembly lado a lado para usar outra versão do mesmo assembly.
ms.assetid: 9146c81e-8f43-4854-bbc4-1daaeb5fdda8
title: Publisher Configuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1134fa29775fc34384f5da19e660d91de10532110304caf8b6ecacbb92fec87e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141949"
---
# <a name="publisher-configuration"></a>Publisher Configuração

Um [arquivo de configuração](publisher-configuration-files.md) do publicador redireciona globalmente aplicativos e assemblies que têm uma dependência em uma versão de um assembly lado a lado para usar outra versão do mesmo assembly. Isso permite que aplicativos e assemblies usem o assembly atualizado sem a necessidade de recriar todos os aplicativos afetados.

[Publisher arquivos](publisher-configuration-files.md) de configuração podem ser fornecidos pelo editor de um assembly ao emissão de uma nova versão do assembly com correções de bugs compatíveis ou atualizações de segurança. A versão atualizada deve ser totalmente compatível com versões anteriores. Um arquivo de configuração do publicador nunca deve ser usado para adicionar novos recursos, a menos que a atualização seja totalmente compatível com versões anteriores. Publisher arquivos de configuração nunca devem ser usados para incrementar a versão principal ou secundária de um assembly. Por exemplo, não redirecione o assembly versão 6.0.0.0 para 7.0.0.0 ou para 6.1.0.0.

Publisher arquivos de configuração devem ser emitidos apenas pelo editor do assembly. Os desenvolvedores de assembly devem assinar assemblies compartilhados lado a lado e arquivos de configuração do editor. Use a mesma chave para assinar o assembly e os arquivos de configuração do publicador associados. Publisher arquivos de configuração devem ser assinados usando as mesmas ferramentas usadas para assemblies, consulte Exemplo de assinatura de [assembly](assembly-signing-example.md) e Criando arquivos [assinados e catálogos](creating-signed-files-and-catalogs.md).

Normalmente, a nova versão de um assembly e o arquivo de configuração do publicador associado serão instalados em uma service pack atualização. Publisher arquivos de configuração nunca devem ser fornecidos com aplicativos como um redistribuível porque a instalação de um arquivo de configuração do publicador redireciona globalmente assemblies no sistema. Se o assembly que está sendo atualizado for fornecido como um redistribuível, o editor deverá fornecer os dois exemplos a seguir.

-   Um Windows do instalador (arquivo .msi) que inclui a nova versão do assembly com a configuração do publicador. Isso pode ser instalado como um service pack ou QFE porque, nesse caso, o cliente optou por atualizar globalmente o sistema. Esta versão do pacote nunca deve ser instalada por aplicativos.
-   Um Windows módulo de mesclagem do instalador (arquivo .msm) que inclui apenas a nova versão do assembly. Essa versão pode ser incluída com aplicativos.

Os aplicativos que exigem uma versão mínima do assembly deverão estado de sua dependência na versão mínima, se a versão mínima não estiver disponível em um sistema, o aplicativo falhará ao iniciar. Se ele estiver disponível como um redistribuível, ele deverá ser incluído na configuração do aplicativo.

Por exemplo, instalar o arquivo [de](publisher-configuration-files.md) configuração do editor a seguir redireciona a associação da versão 2.0.0.0 da Microsoft. Windows. SampleAssembly para a versão 2.0.1.0. Isso adiciona uma nova política, chamada 1.1.0.0.Policy, em %systemDrive% \\ windows \\ winsxs \\ policies \\ x86 \_ policy.2.0.Microsoft.Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-ww \_ < *hashvalue>.*

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="1.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

Instalar o arquivo de configuração do editor a seguir para o mesmo assembly redireciona a associação da versão 2.0.0.0 da Microsoft. Windows. SampleAssembly para a versão 2.0.3.0. Isso adiciona outra política, chamada 2.1.0.0.Policy, em %systemDrive% \\ windows \\ winsxs \\ policies \\ x86 \_ policy.2.0.Microsoft.Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-ww \_ < *hashvalue>.*

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="2.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.3.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

 

 



