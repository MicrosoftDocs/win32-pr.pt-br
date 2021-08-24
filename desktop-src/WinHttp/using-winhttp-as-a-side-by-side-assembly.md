---
description: no Windows Server 2003, o WinHTTP é implementado como um assembly lado a lado e deve ser vinculado a tal como tal. observe que isso não se aplica ao Windows Vista e posterior.
ms.assetid: 524d926d-4d8a-4576-96fd-c533517ba28e
title: Usando o WinHTTP como um assembly lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c8c6312fb57f210e0324c1ae89bb785fd5b51bcb2b1ea4ba1a4959a3d0fd540
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614086"
---
# <a name="using-winhttp-as-a-side-by-side-assembly"></a>Usando o WinHTTP como um assembly lado a lado

no Windows Server 2003, o WinHTTP é implementado como um assembly lado a lado e deve ser vinculado a tal como tal. observe que isso não se aplica ao Windows Vista e posterior.

## <a name="side-by-side-assemblies"></a>Assemblies lado a lado

a partir do Microsoft Windows XP, um mecanismo de assemblies lado a lado foi fornecido para controlar a vinculação de tempo de execução para evitar conflitos de controle de versão da DLL (biblioteca de vínculo dinâmico). Para obter informações sobre assemblies lado a lado, consulte [sobre aplicativos isolados e assemblies](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies)lado a lado.

para usar esse mecanismo para vincular o winhttp versão 5,1 no Windows Server 2003, um aplicativo deve incorporar um manifesto que especifica o WinHTTP como um assembly dependente. Consulte [usando assemblies lado a lado](/windows/desktop/SbsCs/using-side-by-side-assemblies) para obter mais informações sobre como fazer isso.

## <a name="a-sample-winhttp-application-manifest"></a>Um manifesto de aplicativo do WinHTTP de exemplo

O manifesto de exemplo a seguir ilustra um manifesto de aplicativo que pode ser usado para vincular ao WinHTTP.

Todos os atributos, exceto "Type" de " <assembly> <assemblyIdentity> ", devem ser modificados conforme apropriado para seu aplicativo específico. O mesmo vale para o conteúdo do elemento " &lt; Description &gt; ".

Além disso, certifique-se de que o atributo "processorArchitecture" de " <dependentAssembly> <assemblyIdentity> " corresponda ao atributo "processorArchitecture" de " <assembly> <assemblyIdentity> ". Abaixo, por exemplo, ambos estão definidos como "x86".

Todos os valores não específicos do seu aplicativo devem seguir os formulários mostrados abaixo.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity
                    version="1.0.0.0"
                    processorArchitecture="x86"
                    name="Microsoft.Windows.Sample"
                    type="win32" />
  <description>Sample WinHttp Application</description>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity 
                    type="win32" 
                    name="Microsoft.Windows.WinHTTP" 
                    version="5.1.0.0"
                    processorArchitecture="x86" 
                    publicKeyToken="6595b64144ccf1df"
                    language="*" />
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
