---
title: Alterações de versão do sistema operacional no Windows 8.1 e no Windows Server 2012 R2
description: Alterações de versão do sistema operacional no Windows 8.1 e no Windows Server 2012 R2
ms.assetid: 3040262A-85EB-4F26-BE34-D2BBD5886E9E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0078ba918c675bbc8b9b9bbaf76660388f05bda9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366633"
---
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a>Alterações de versão do sistema operacional no Windows 8.1 e no Windows Server 2012 R2

## <a name="platforms"></a>Plataformas

**Clientes-** Windows 8.1

**Servidores-** Windows Server 2012 R2

## <a name="description"></a>Descrição

Fizemos algumas alterações significativas em como as APIs GetVersion (ex) funcionam em Windows 8.1 devido a comportamentos indesejáveis do cliente, resultando da forma como as APIs GetVersion (ex) foram usadas no passado.

Nas versões anteriores do Windows, chamar as APIs GetVersion (ex) retornaria a versão real do sistema operacional (SO), a menos que o processo tivesse sido mitigado por um Shim de compatibilidade de aplicativo para dar a ele uma versão diferente. Isso foi feito em uma base provisionada e foi relativamente incompleto em termos do número de processos que a Microsoft poderia corrigir razoavelmente em uma versão. Muitos aplicativos passam pelas rachaduras porque não obtiveram corrigido devido a verificações de versão mal projetadas.

O número um motivo para fazer uma verificação de versão é avisar o usuário de que o aplicativo precisa ser executado em uma versão mais recente do sistema operacional. No entanto, devido a verificações ruins, os aplicativos geralmente avisam que eles precisavam ser executados no Windows XP ou posterior, o que é claro que o sistema operacional mais recente é. Com mais frequência do que não, o sistema operacional mais recente executaria o aplicativo sem nenhum problema se não fosse para essas verificações.

## <a name="manifestation"></a>Manifestação

No Windows 8.1, as APIs GetVersion (ex) foram preteridas. Isso significa que, embora você ainda possa chamar essas funções de API, se seu aplicativo não direcionar especificamente Windows 8.1, as funções retornarão a versão do Windows 8 (6,2).

## <a name="solution"></a>Solução

### <a name="adding-an-app-manifest"></a>Adicionando um manifesto de aplicativo

Para que seu aplicativo seja direcionado Windows 8.1, você precisará incluir um [manifesto de aplicativo (executável)](/windows/compatibility/application-executable-manifest) para o executável do aplicativo. Em seguida, na [seção **&lt; compatibilidade &gt;**](../SbsCs/application-manifests.md#compatibility) do manifesto, você precisará adicionar um elemento **&lt; supportedOS &gt;** para cada versão do Windows que você deseja declarar para o suporte do seu aplicativo.

O exemplo a seguir mostra um arquivo de manifesto de aplicativo para um aplicativo que dá suporte a todas as versões do Windows do Windows Vista para Windows 8.1:

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

A declaração de suporte para Windows 8.1 em seu manifesto de aplicativo não terá nenhum efeito ao executar seu aplicativo em sistemas operacionais anteriores.

### <a name="using-versionhelpers-instead-of-getversionex"></a>Usando VersionHelpers em vez de GetVersion (ex)

Windows 8.1 introduz novas funções de API de substituição para GetVersion (ex), conhecidas como VersionHelpers. Eles são extremamente fáceis de usar; Tudo o que você precisa fazer é `#include <VersionHelpers.h>` . As funções embutidas disponíveis no arquivo de cabeçalho VersionHelpers. h permitem que seu código pergunte se o sistema operacional é uma determinada versão do Windows ou posterior.

**Exemplo** Por exemplo, se seu aplicativo exigir o Windows 8 ou posterior, use o teste a seguir:

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

As funções de API do VersionHelper disponíveis são:

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

Eles retornarão TRUE ou FALSE dependendo da pergunta que você está fazendo e você só precisa definir o sistema operacional de nível mínimo ao qual dá suporte.

## <a name="resources"></a>Recursos

-   [Download do kit de ferramentas de compatibilidade de aplicativos](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   [Correções de compatibilidade conhecidas, modos de compatibilidade e mensagens AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [APIs do VersionHelpers](../sysinfo/version-helper-apis.md)