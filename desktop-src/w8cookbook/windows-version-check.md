---
title: Verificação de versão do Windows
description: a versão do sistema operacional foi incrementada com a versão do sistema operacional Windows 10.
ms.assetid: 55BB7B44-1AFD-456D-9380-38B4D26E5EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710f59313f05dac95e5953c6013108987dc9bf8ad84d7eb7d8bca67a5391996b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007876"
---
# <a name="windows-version-check"></a>Verificação de versão do Windows

a versão do sistema operacional foi incrementada com a versão do sistema operacional Windows 10. isso significa que o número de versão interno para Windows 10 também foi alterado para 10,0. Como sempre, não medimos esforços para manter a compatibilidade de aplicativos e dispositivos após uma mudança de versão do sistema operacional. Para a maioria das categorias de aplicativo (sem nenhuma dependência de kernel), a alteração não afetará negativamente a funcionalidade do aplicativo e os aplicativos existentes continuarão funcionando bem no Windows 10.

## <a name="manifestations"></a>Manifestações

A manifestação dessa alteração é específica do aplicativo. Isso significa que qualquer aplicativo que verifica especificamente para a versão do sistema operacional obterá um número de versão superior, que pode levar a uma ou mais das seguintes situações:

-   Os instaladores de aplicativos podem não ser capazes de instalar o aplicativo e os aplicativos talvez não consigam iniciar.
-   Os aplicativos podem ficar instáveis ou falhar.
-   Os aplicativos podem gerar mensagens de erro, mas continuar funcionando adequadamente.

Alguns aplicativos realizam uma verificação de versão e simplesmente passam um aviso para os usuários. No entanto, há aplicativos associados rigidamente a uma verificação de versão (nos drivers ou no modo de kernel para evitar a detecção). Nesses casos, o aplicativo falhará se for encontrada uma versão incorreta. Em vez de uma verificação de versão, recomendamos um dos procedimentos a seguir:

-   Se o aplicativo for dependente da funcionalidade de uma API específica, selecione a versão correta da API.
-   O número de versão do NTDDI (NT Device Driver interface) será incrementado somente se a funcionalidade de destino na API for alterada. Certifique-se de detectar a alteração via APISet ou outra API exposta, conforme criado pela equipe de recursos, e não use a versão como um proxy para algum recurso ou correção. Se houver alterações da falha e uma seleção adequada não for exposta, então isso será um bug.
-   Verifique se o aplicativo não verifica a versão de maneiras estranhas, como por meio do registro, versões de arquivo, deslocamentos, modo kernel, drivers ou outros meios. Se o aplicativo precisar verificar a versão, use as APIs GetVersion, que devem retornar o número principal, secundário e de Build.
-   Se você estiver usando a API GetVersion ou outras funções auxiliares de versão, como [VerifyVersionInfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa), lembre-se de que o comportamento dessa API foi alterado a partir de Windows 8.1. Consulte [a documentação da API](../SysInfo/version-helper-apis.md) para obter mais detalhes.
-   se você tiver aplicativos como antimalware ou firewall, deverá trabalhar com os canais de comentários usuais e por meio do programa insider Windows.

## <a name="declaring-windows-10-compatibility-with-an-app-manifest"></a>declarando Windows 10 compatibilidade com um manifesto de aplicativo

se seu aplicativo for compatível com Windows 10, ele poderá declarar esse fato no [manifesto do aplicativo (executável)](/windows/compatibility/application-executable-manifest) para o executável do aplicativo. isso informa ao sistema que seu aplicativo entende o número da versão do sistema de 10,0 do Windows 10 (portanto, a API getversion não retorna uma versão anterior) e também permite que o sistema desative outros comportamentos de compatibilidade aplicados a aplicativos que não declaram Windows 10 compatibilidade.

para declarar Windows 10 compatibilidade em um manifesto de aplicativo, você precisará adicionar uma [seção de **&lt; &gt; compatibilidade**](../SbsCs/application-manifests.md#compatibility) do manifesto, se ainda não existir um, e, em seguida, adicionar elementos **&lt; supportedOS &gt;** para Windows 10 e todas as outras Windows versão que você deseja declarar para as quais seu aplicativo dá suporte.

o exemplo a seguir mostra um arquivo de manifesto de aplicativo para um aplicativo que dá suporte a todas as versões do Windows do Windows Vista para Windows 10:

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
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/> <!-- * ADD THIS LINE * -->
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
</assembly>
```

A linha acima marcada `* ADD THIS LINE *` mostra como direcionar com precisão seu aplicativo para Windows 10.

a declaração de suporte para Windows 10 em seu manifesto de aplicativo não terá nenhum efeito ao executar seu aplicativo em sistemas operacionais anteriores.

## <a name="resources"></a>Recursos

-   [download do Toolkit de compatibilidade de aplicativos: baixe o Windows ADK para Windows 10](https://download.microsoft.com/download/9/A/E/9AE69DD5-BA93-44E0-864E-180F5E700AB4/adk/adksetup.exe)
-   [Correções de compatibilidade conhecidas, modos de compatibilidade e mensagens AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [API de auxiliares de versão](../sysinfo/version-helper-apis.md)