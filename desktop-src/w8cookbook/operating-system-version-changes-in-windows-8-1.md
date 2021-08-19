---
title: Alterações de versão do sistema operacional Windows 8.1 e Windows Server 2012 R2
description: Alterações de versão do sistema operacional Windows 8.1 e Windows Server 2012 R2
ms.assetid: 3040262A-85EB-4F26-BE34-D2BBD5886E9E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e1fe0972a915d0f13ca3c3f8f52e5dd0559ad9c24e1afd2dd005f4a733373c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882686"
---
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a>Alterações de versão do sistema operacional Windows 8.1 e Windows Server 2012 R2

## <a name="platforms"></a>Plataformas

**Clientes – Windows 8.1**

**Servidores – Windows Server 2012** R2

## <a name="description"></a>Descrição

Fizemos algumas alterações significativas em como as APIs GetVersion(Ex) funcionam no Windows 8.1 devido a comportamentos indesejáveis do cliente resultantes de como as APIs GetVersion(Ex) foram usadas no passado.

Nas versões anteriores do Windows, chamar as APIs GetVersion(Ex) retornaria a versão real do sistema operacional ,a menos que o processo tivesse sido mitigado por um shim de compatibilidade de aplicativo para dar a ela uma versão diferente. Isso foi feito em uma base temporária e estava relativamente incompleto em termos do número de processos que a Microsoft poderia razoavelmente fazer shim em uma versão. Muitos aplicativos passam pelas trincas porque não foram aparados devido a verificações de versão mal projetadas.

O principal motivo para fazer uma verificação de versão é avisar o usuário de que o aplicativo precisa ser executado em uma versão mais recente do sistema operacional. No entanto, devido a verificações incorretas, os aplicativos geralmente avisam incorretamente que precisam ser executados no Windows XP ou posterior, que é claro que é o sistema operacional mais recente. Com mais frequência do que não, o sistema operacional mais recente executaria o aplicativo sem problemas se não fosse por essas verificações.

## <a name="manifestation"></a>Manifestação

No Windows 8.1, as APIs GetVersion(Ex) foram preterida. Isso significa que, embora você ainda possa chamar essas funções de API, se seu aplicativo não for especificamente destinado Windows 8.1, as funções retornarão a versão Windows 8 (6.2).

## <a name="solution"></a>Solução

### <a name="adding-an-app-manifest"></a>Adicionando um manifesto do aplicativo

Para que seu aplicativo seja Windows 8.1, você precisará incluir um manifesto do aplicativo [(executável)](/windows/compatibility/application-executable-manifest) para o executável do aplicativo. Em seguida, [ **&lt; &gt;**](../SbsCs/application-manifests.md#compatibility) na seção de compatibilidade do manifesto, você precisará adicionar um elemento **&lt; supportedOS &gt;** para cada versão Windows que você deseja declarar que seu aplicativo dá suporte.

O exemplo a seguir mostra um arquivo de manifesto do aplicativo para um aplicativo que dá suporte a todas as versões do Windows do Windows Vista para Windows 8.1:

```XML
<!-- example.exe.manifest -->
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
    <assemblyIdentity
        type="win32"
        name="Contoso.ExampleApplication.ExampleBinary"
        version="1.2.3.4"
        processorArchitecture="x86"
    />
    <description>Contoso Example Application</description>
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/> <!-- * ADD THIS LINE * -->
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
</assembly>
```

A linha acima marcada `* ADD THIS LINE *` mostra como direcionar com precisão seu aplicativo para Windows 8.1.

Declarar o suporte para Windows 8.1 no manifesto do aplicativo não terá nenhum efeito ao executar seu aplicativo em sistemas operacionais anteriores.

### <a name="using-versionhelpers-instead-of-getversionex"></a>Usando VersionHelpers em vez de GetVersion(Ex)

Windows 8.1 introduz novas funções de API de substituição para GetVersion(Ex), conhecidas como VersionHelpers. Eles são extremamente fáceis de usar; tudo o que você precisa fazer é `#include <VersionHelpers.h>` . As funções em linha disponíveis no arquivo de header VersionHelpers.h permitem que seu código pergunte se o sistema operacional é uma determinada versão do Windows ou posterior.

**Exemplo** Por exemplo, se o aplicativo exigir Windows 8 ou posterior, use o seguinte teste:

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

As funções de API VersionHelper disponíveis são:

```c
#define VERSIONHELPERAPI FORCEINLINE BOOL
VERSIONHELPERAPI IsWindowsXPOrGreater();
VERSIONHELPERAPI IsWindowsXPSP1OrGreater();
VERSIONHELPERAPI IsWindowsXPSP2OrGreater();
VERSIONHELPERAPI IsWindowsXPSP3OrGreater();
VERSIONHELPERAPI IsWindowsVistaOrGreater();
VERSIONHELPERAPI IsWindowsVistaSP1OrGreater();
VERSIONHELPERAPI IsWindowsVistaSP2OrGreater();
VERSIONHELPERAPI IsWindows7OrGreater();
VERSIONHELPERAPI IsWindows7SP1OrGreater();
VERSIONHELPERAPI IsWindows8OrGreater();
VERSIONHELPERAPI IsWindows8Point1OrGreater();
VERSIONHELPERAPI IsWindowsServer();
```

Eles retornarão TRUE ou FALSE dependendo da pergunta que você está fazendo e você só precisa definir o sistema operacional de nível mínimo ao qual você suporta.

## <a name="resources"></a>Recursos

-   [Download de compatibilidade Toolkit aplicativo](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   [Correções de compatibilidade conhecidas, modos de compatibilidade e mensagens AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [VersionHelpers APIs](../sysinfo/version-helper-apis.md)