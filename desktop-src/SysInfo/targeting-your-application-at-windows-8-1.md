---
description: No Windows 8.1 e Windows 10, as funções GetVersion e GetVersionEx foram preterida.
ms.assetid: E7A1A16A-95B3-4B45-81AD-A19E33F15AE4
title: Direcionando seu aplicativo para Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e045dff2f46501c4715e2ffebe484dfeadb3aa9f276d79c7e7c1afdbec6ba7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763107"
---
# <a name="targeting-your-application-for-windows"></a>Direcionando seu aplicativo para Windows

No Windows 8.1 e Windows 10, as funções [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) e [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) foram preterida. No Windows 10, a [**função VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) também foi preterida. Embora você ainda possa chamar as funções preterida, se o aplicativo não for especificamente destinado a Windows 8.1 ou Windows 10, as funções retornarão a versão Windows 8 (6.2).

> [!Note]  
> [**As funções GetVersion,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) [**GetVersionEx,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)e [Version Helper](version-helper-apis.md) são apenas para aplicativos da área de trabalho. Aplicativos Windows universal podem usar a propriedade [**AnalyticsInfo.VersionInfo**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) para telemetria e logs de diagnóstico.

Para que seu aplicativo seja Windows 8.1 ou Windows 10, você precisará incluir um manifesto do aplicativo [(executável)](/windows/compatibility/application-executable-manifest) para o executável do aplicativo. Em seguida, [ **&lt; &gt;**](../SbsCs/application-manifests.md#compatibility) na seção de compatibilidade do manifesto, você precisará adicionar um elemento **&lt; supportedOS &gt;** para cada versão Windows que você deseja declarar que seu aplicativo dá suporte.

O exemplo a seguir mostra um arquivo de manifesto do aplicativo para um aplicativo que dá suporte a todas as versões do Windows do Windows Vista para Windows 10:

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
            <!-- Windows 10 -->
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/>
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
        <security>
            <requestedPrivileges>
                <!--
                  UAC settings:
                  - app should run at same integrity level as calling process
                  - app does not need to manipulate windows belonging to
                    higher-integrity-level processes
                  -->
                <requestedExecutionLevel
                    level="asInvoker"
                    uiAccess="false"
                />   
            </requestedPrivileges>
        </security>
    </trustInfo>
</assembly>
```

Declarar suporte para Windows 8.1 ou Windows 10 no manifesto do aplicativo não terá nenhum efeito ao executar seu aplicativo em sistemas operacionais anteriores.

O manifesto do aplicativo acima também inclui uma [ **&lt; seção trustInfo &gt;**](/previous-versions/bb756929(v=msdn.10)), que especifica como o sistema deve tratá-lo em relação ao [UAC (Controle](/windows/security/identity-protection/user-account-control/how-user-account-control-works)de Conta de Usuário). Adicionar **trustInfo** não é essencial, mas é altamente recomendável, mesmo quando seu aplicativo não precisa de nenhum comportamento específico relacionado ao UAC. Em particular, se você não adicionar **trustInfo,** as versões x86 de 32 bits do seu aplicativo estarão sujeitas à virtualização de arquivo [UAC,](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization)que permite que as gravações em pastas com privilégios de administrador, como as pastas do sistema Windows, sejam bem-sucedidas quando falharem de outra forma, mas as redireciona para uma pasta "VirtualStore" específica do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Obter a versão do sistema](getting-the-system-version.md)
</dt> <dt>

[Funções auxiliares de versão](version-helper-apis.md)
</dt> <dt>

[Osversioninfo](/windows/desktop/api/winnt/ns-winnt-osversioninfoa)
</dt> <dt>

[OSVERSIONINFOEX](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)
</dt> </dl>
