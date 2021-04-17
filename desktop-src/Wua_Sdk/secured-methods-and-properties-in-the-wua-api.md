---
description: Quando o WUA detecta que um chamador não tem permissão para acessar uma interface, um método ou uma propriedade, o HRESULT E \_ ACCESSDENIED é retornado.
ms.assetid: 4535ce8d-c329-4335-8b0a-8f63c22f111d
title: Protegendo interfaces, métodos e propriedades na API do WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6680f616e1ca0596aba04edf4f7ddf7615e0c7f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811494"
---
# <a name="securing-interfaces-methods-and-properties-in-the-wua-api"></a>Protegendo interfaces, métodos e propriedades na API do WUA

Algumas interfaces, métodos e propriedades do WUA (Windows Update Agent) são acessíveis somente a chamadores que pertencem aos seguintes grupos de segurança do Windows:

-   Administrador
-   Usuário
-   Usuário avançado

Quando o WUA detecta que um chamador não tem permissão para acessar uma interface, um método ou uma propriedade, o **HRESULT** E \_ ACCESSDENIED é retornado.

As seguintes interfaces estão disponíveis para os grupos de segurança administrador, usuário e usuário avançado:

-   [**IAutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)
-   [**IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings2)
-   [**ISystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)
-   [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) e [ **IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)

> [!Note]  
> Se as seguintes condições forem verdadeiras, uma pesquisa falhará:
>
> -   Um usuário que não é um administrador define a [**Propriedade UserLocale da interface IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) como uma localidade que corresponde a um idioma que não está instalado no computador.
> -   A pesquisa usa um objeto UpdateSearch criado a partir do objeto UpdateSession.

 

As seguintes interfaces e métodos de download estão disponíveis para os grupos de usuários avançados e de administrador:

-   [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)
-   [**IUpdate::CopyFromCache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [**IAutomaticUpdatesSettings2::CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)
    > [!Note]  
    > Administradores, usuários e usuários avançados podem chamar [**IAutomaticUpdatesSettings2:: CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).

     

As seguintes interfaces, métodos e propriedades de instalação estão disponíveis para os grupos de administradores:

-   [**IAutomaticUpdates::P ause**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [**IAutomaticUpdates:: retomar**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [**IAutomaticUpdates::EnableService**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)
-   [**Propriedade IsHidden de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)
    > [!Note]  
    > Administradores, usuários e usuários avançados podem recuperar os valores da [**Propriedade IsHidden de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden). No entanto, somente administradores e usuários avançados podem definir os valores.

     

-   [**IUpdate:: AcceptEula**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
    > [!Note]  
    > Os administradores e os usuários avançados podem chamar o [**método AcceptEula de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).

     

-   [**IAutomaticUpdatesSettings:: salvar**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)
-   [**Propriedade NotificationLevel de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)
    > [!Note]  
    > Administradores, usuários e usuários avançados podem recuperar os valores da [**Propriedade notificationLevel de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel). No entanto, somente os administradores podem definir os valores.

     

-   [**Propriedade ScheduledInstallationDay de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)
    > [!Note]  
    > Administradores, usuários e usuários avançados podem recuperar os valores da [**Propriedade ScheduledInstallationDay de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday). No entanto, somente os administradores podem definir os valores.

     

-   [**Propriedade ScheduledInstallationTime de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)
    > [!Note]  
    > Administradores, usuários e usuários avançados podem recuperar os valores da [**Propriedade ScheduledInstallationTime de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime). No entanto, somente os administradores podem definir os valores.

     

-   [**Propriedade IncludeRecommendedUpdates de IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)
    > [!Note]  
    > Administradores, usuários e usuários avançados podem recuperar os valores da [**Propriedade IncludeRecommendedUpdates de IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates). No entanto, somente os administradores podem definir os valores.

     

 

 



