---
description: No Windows 8.1 e no Windows 10, as funções GetVersion e GetVersionEx foram preteridas.
ms.assetid: E7A1A16A-95B3-4B45-81AD-A19E33F15AE4
title: Direcionando seu aplicativo para Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0bd280451e5a1dd6a5162dd7b9ccb34495d22be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297340"
---
# <a name="targeting-your-application-for-windows"></a>Direcionando seu aplicativo para Windows

No Windows 8.1 e no Windows 10, as funções [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) e [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) foram preteridas. No Windows 10, a função [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) também foi preterida. Embora você ainda possa chamar as funções preteridas, se seu aplicativo não direcionar especificamente Windows 8.1 ou Windows 10, as funções retornarão a versão do Windows 8 (6,2).

> [!Note]  
> As funções [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion), [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa), [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)e [auxiliar de versão](version-helper-apis.md) são apenas para aplicativos de área de trabalho. Os aplicativos universais do Windows podem usar a propriedade [**AnalyticsInfo. VERSIONINFO**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) para logs de telemetria e diagnóstico.

Para que seu aplicativo seja direcionado Windows 8.1 ou Windows 10, você precisará incluir um [manifesto de aplicativo (executável)](/windows/compatibility/application-executable-manifest) para o executável do aplicativo. Em seguida, na [seção **&lt; compatibilidade &gt;**](../SbsCs/application-manifests.md#compatibility) do manifesto, você precisará adicionar um elemento **&lt; supportedOS &gt;** para cada versão do Windows que você deseja declarar para o suporte do seu aplicativo.

O exemplo a seguir mostra um arquivo de manifesto de aplicativo para um aplicativo que dá suporte a todas as versões do Windows do Windows Vista para o Windows 10:

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

A declaração de suporte para Windows 8.1 ou Windows 10 em seu manifesto de aplicativo não terá nenhum efeito ao executar seu aplicativo em sistemas operacionais anteriores.

O manifesto do aplicativo acima também inclui uma [seção **&lt; &gt; TrustInfo**](/previous-versions/bb756929(v=msdn.10)), que especifica como o sistema deve tratá-lo em relação ao [UAC (controle de conta de usuário)](/windows/security/identity-protection/user-account-control/how-user-account-control-works). Adicionar **TrustInfo** não é essencial, mas é altamente recomendável, mesmo quando seu aplicativo não precisa de nenhum comportamento específico relacionado ao UAC. Em particular, se você não adicionar **TrustInfo** , as versões x86 de 32 bits do seu aplicativo estarão sujeitas à [virtualização de arquivos do UAC](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), o que permite que as gravações em pastas com privilégios de administrador, como as pastas de sistema do Windows, tenham êxito quando elas falharem, mas as redireciona para uma pasta "VirtualStore" específica do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Obtendo a versão do sistema](getting-the-system-version.md)
</dt> <dt>

[Funções auxiliares de versão](version-helper-apis.md)
</dt> <dt>

[OSVERSIONINFO](/windows/desktop/api/winnt/ns-winnt-osversioninfoa)
</dt> <dt>

[OSVERSIONINFOEX](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)
</dt> </dl>
