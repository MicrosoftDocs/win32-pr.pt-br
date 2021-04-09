---
description: A partir do Windows XP, você pode criar um assembly privado e torná-lo disponível para um aplicativo específico.
ms.assetid: 08cebffc-6856-4dac-8600-5e7fecb5c69b
title: Corrigir um aplicativo existente usando um assembly privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095c3eefc5f166ad09643a363ec4308d190e6586
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010432"
---
# <a name="fixing-an-existing-application-using-a-private-assembly"></a>Corrigindo um aplicativo existente usando um assembly privado

A partir do Windows XP, você pode criar um assembly privado e torná-lo disponível para um aplicativo específico. Esse recurso pode ser usado para corrigir um aplicativo que se torna incompatível com uma atualização. Um exemplo seria um aplicativo que se torna incompatível com a versão mais recente do MSVCRT.DLL após a atualização do sistema operacional. Nesse caso, você não tem a opção de substituir a versão do sistema porque MSVCRT.DLL é um arquivo protegido do Windows. Em vez de ter que reescrever o aplicativo para funcionar com a nova versão do MSVCRT, você pode criar um assembly privado para o MSVCRT e instalá-lo na pasta do aplicativo. Observe que nem todo componente compartilhado é um candidato adequado para um assembly lado a lado privado, e alguns componentes têm restrições de licenciamento sobre onde seus componentes podem ser instalados. O componente precisa atender aos critérios para um componente lado a lado. Pergunte ao editor do componente se ele pode fornecer um assembly adequado.

O manifesto do assembly privado e o manifesto do aplicativo devem ser instalados na mesma pasta que o executável do aplicativo. Quando o aplicativo é executado, ele consulta o manifesto do aplicativo e carrega a versão do MSVCRT que é privada para o aplicativo.

Para este exemplo, o assembly privado incluiria MSVCRT.DLL e MSVCIRT.DLL como no seguinte manifesto do assembly:

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32"
      name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
version="6.0.0.0" 
processorArchitecture="x86"/>
    <file name="msvcrt.dll"/>
    <file name="msvcirt.dll"/>
</assembly>
```

Veja a seguir um exemplo de um possível manifesto do aplicativo.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<assemblyIdentity 
    version="1.0.0.0" 
    processorArchitecture="x86" 
    name="APPLICATION" 
    type="win32" 
/> 
<description>Description of Application</description> 
<dependency> 
    <dependentAssembly> 
       <assemblyIdentity 
           type="win32"
           name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
           version="6.0.0.0" 
           processorArchitecture="x86"/> 
    </dependentAssembly> 
</dependency> 
</assembly>
```

 

 



