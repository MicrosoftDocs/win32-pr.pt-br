---
description: O instalador executa ações personalizadas com privilégios de usuário por padrão para limitar o acesso de ações personalizadas ao sistema.
ms.assetid: 62a3d103-a786-4727-b757-3a8229c8a53f
title: Segurança de ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0a8011640bea177ec253f555b6ff83302541b640a050ccf861eb345c58ca13f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143306"
---
# <a name="custom-action-security"></a>Segurança de ação personalizada

O instalador executa ações personalizadas com privilégios de usuário por padrão para limitar o acesso de ações personalizadas ao sistema. O instalador pode executar ações personalizadas com privilégios elevados se um aplicativo gerenciado estiver sendo instalado ou se a política do sistema tiver sido especificada para privilégios elevados.

Você deve usar a propriedade [**MsiHiddenProperties**](msihiddenproperties.md) e **msidbCustomActionTypeHideTarget** para impedir o registro em log de informações confidenciais usadas pela ação personalizada. Para obter mais informações  sobre msidbCustomActionTypeHideTarget [, consulte opção de destino oculto de ação personalizada](custom-action-hidden-target-option.md).

Desmarque a propriedade CustomActionData depois de defini-la para garantir que os dados confidenciais não estejam mais disponíveis. O código de exemplo abaixo é um trecho usado por uma ação personalizada de DLL imediata que está configurando dados para uso por uma ação personalizada adiada chamada "MyDeferredCA":


```C++
#include <windows.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall MyImmediateCA(MSIHANDLE hInstall)
{
    // set up information for deferred custom action called MyDeferredCA
    const TCHAR szValue[] = TEXT("data");
    UINT uiStat = ERROR_INSTALL_FAILURE;
    if (ERROR_SUCCESS == MsiSetProperty(hInstall, TEXT("MyDeferredCA"), szValue))
    {
        uiStat = MsiDoAction(hInstall, TEXT("MyDeferredCA"));

        // clear CustomActionData property
        if (ERROR_SUCCESS != MsiSetProperty(hInstall, TEXT("MyDeferredCA"), TEXT("")))
            return ERROR_INSTALL_FAILURE;
    }

    return (uiStat == ERROR_SUCCESS) ? uiStat : ERROR_INSTALL_FAILURE;    
}
```



Observe que apenas [ações personalizadas de execução adiada](deferred-execution-custom-actions.md) podem usar o atributo **msidbCustomActionTypeNoImpersonate** . Para obter mais informações, consulte [ação personalizada In-Script opções de execução](custom-action-in-script-execution-options.md).

Se o bit **msidbCustomActionTypeNoImpersonate** não estiver definido para uma ação personalizada, o instalador executará a ação personalizada com privilégios de nível de usuário. Para obter mais informações, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).

Se o bit **msidbCustomActionTypeNoImpersonate** for definido e um aplicativo gerenciado estiver sendo instalado com a permissão de administrador, o instalador poderá executar a ação personalizada com privilégios elevados. No entanto, se um usuário tentar instalar o aplicativo gerenciado sem permissão de administrador, o instalador executará o aplicativo com privilégios de nível de usuário, independentemente de o **msidbCustomActionTypeNoImpersonate** ser definido.

Observe que uma ação personalizada pode ser executada com privilégios de sistema, mesmo quando o bit **msidbCustomActionTypeNoImpersonate** não está definido. isso ocorrerá se um administrador instalar o aplicativo para todos os usuários em um servidor que executa o serviço de função Terminal Server usando Windows 2000 e a ação não estiver marcada com **msidbCustomActionTypeTSAware**. Uma ação personalizada também pode ser executada com privilégios de sistema se a instalação for chamada quando não houver nenhum contexto de usuário. por exemplo, se não houver um usuário conectado no momento durante uma instalação invocada pela implantação do aplicativo Windows 2000.

Ao criar suas próprias ações personalizadas, você sempre deve criar a ação personalizada usando métodos seguros. Para obter mais informações, consulte [diretrizes para proteger ações personalizadas](guidelines-for-securing-custom-actions.md).

 

 



