---
description: Um arquivo de configuração do Publicador redireciona globalmente os aplicativos e assemblies com uma dependência em uma versão de um assembly lado a lado para usar outra versão do mesmo assembly.
ms.assetid: 9146c81e-8f43-4854-bbc4-1daaeb5fdda8
title: Configuração do Publicador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50ceb5263830cb1778aaaede673974cd7faca75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171281"
---
# <a name="publisher-configuration"></a>Configuração do Publicador

Um [arquivo de configuração do Publicador](publisher-configuration-files.md) redireciona globalmente os aplicativos e assemblies com uma dependência em uma versão de um assembly lado a lado para usar outra versão do mesmo assembly. Isso permite que os aplicativos e assemblies usem o assembly atualizado sem precisar recompilar todos os aplicativos afetados.

Os [arquivos de configuração do Publicador](publisher-configuration-files.md) podem ser fornecidos pelo editor de um assembly ao emitir uma nova versão do assembly com correções de bugs ou atualizações de segurança compatíveis. A versão atualizada deve ser totalmente compatível com versões anteriores. Um arquivo de configuração do Publicador nunca deve ser usado para adicionar novos recursos, a menos que a atualização seja totalmente compatível com versões anteriores. Os arquivos de configuração do Publicador nunca devem ser usados para incrementar a versão principal ou secundária de um assembly. Por exemplo, não redirecione a versão do assembly 6.0.0.0 para 7.0.0.0 ou para 6.1.0.0.

Os arquivos de configuração do Publicador só devem ser emitidos pelo Publicador do assembly. Os desenvolvedores de assembly devem assinar assemblies lado a lado e arquivos de configuração do Publicador. Use a mesma chave para assinar o assembly e os arquivos de configuração do Publicador associados. Os arquivos de configuração do Publicador devem ser assinados usando as mesmas ferramentas usadas para assemblies, consulte [exemplo de assinatura de assembly](assembly-signing-example.md) e [criando arquivos e catálogos assinados](creating-signed-files-and-catalogs.md).

Normalmente, a nova versão de um assembly e o arquivo de configuração do Publicador associado serão instalados em uma atualização service pack. Os arquivos de configuração do Publicador nunca devem ser fornecidos com aplicativos como um redistribuível porque a instalação de um arquivo de configuração do Publicador redireciona globalmente os assemblies no sistema. Se o assembly que está sendo atualizado for fornecido como um redistribuível, o Publicador deverá fornecer os dois procedimentos a seguir.

-   Um pacote Windows Installer (arquivo. msi) que inclui a nova versão do assembly com a configuração do Publicador. Isso pode ser instalado como um service pack ou um QFE porque, nesse caso, o cliente optou por atualizar globalmente o sistema. Essa versão do pacote nunca deve ser instalada por aplicativos.
-   Um módulo de mesclagem Windows Installer (arquivo. msm) que inclui apenas a nova versão do assembly. Essa versão pode ser incluída em aplicativos.

Aplicativos que exigem uma versão mínima do assembly devem declarar sua dependência na versão mínima, se a versão mínima não estiver disponível em um sistema, o aplicativo não será iniciado. Se ele estiver disponível como um redistribuível, ele deverá ser incluído na instalação do aplicativo.

Por exemplo, a instalação do seguinte [arquivo de configuração do Publicador](publisher-configuration-files.md) redireciona a associação da versão 2.0.0.0 do Microsoft. Windows. SampleAssembly para a versão 2.0.1.0. Isso adiciona uma nova política, chamada 1.1.0.0. Policy, em% systemDrive% \\ Windows \\ winsxs \\ Policies \\ \_ Policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-WW \_ < *HashValue*>.

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

A instalação do arquivo de configuração do Publicador a seguir para o mesmo assembly redireciona a associação da versão 2.0.0.0 do Microsoft. Windows. SampleAssembly para a versão 2.0.3.0. Isso adiciona outra política, chamada 2.1.0.0. Policy, em% systemDrive% \\ Windows \\ winsxs \\ Policies \\ \_ Policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-WW \_ < *HashValue*>.

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

 

 



