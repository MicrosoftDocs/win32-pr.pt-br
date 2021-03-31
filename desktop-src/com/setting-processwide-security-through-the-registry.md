---
title: Configurando a segurança do Process-Wide por meio do registro
description: Se você quiser definir a segurança para um processo inteiro, uma solução é definir os níveis de segurança desejados no registro.
ms.assetid: 87f0a64f-f3ec-4ee2-8d65-4f82e8971f0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d303f184229cb20aef1cbf71733956a3b6ce6618
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917713"
---
# <a name="setting-process-wide-security-through-the-registry"></a>Configurando a segurança do Process-Wide por meio do registro

Se você quiser definir a segurança para um processo inteiro, uma solução é definir os níveis de segurança desejados no registro. Se seu aplicativo não puder chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou se você preferir não usar a segurança programática, isso pode ser uma boa opção. Se você decidir definir a segurança de todo o processo usando o registro, deverá estar ciente de que se chamar **CoInitializeSecurity** dentro de seu programa com usará os valores em **CoInitializeSecurity** e ignorará os valores do registro.

Há duas maneiras de definir a segurança no registro para seu aplicativo:

-   Você pode usar Dcomcnfg.exe, que fornece uma interface de usuário simples para modificar os valores de segurança. Todos os servidores COM podem ser configurados usando Dcomcnfg.exe. Para obter mais informações, consulte [definindo Process-Wide segurança usando DCOMCNFG](setting-processwide-security-using-dcomcnfg.md). No entanto, os aplicativos cliente normalmente não aparecem no Dcomcnfg.exe, a menos que o cliente crie um GUID e o insira no registro.
-   Você pode definir valores de segurança na chave [AppID](appid-key.md) para o aplicativo. O restante deste tópico explica como definir a segurança no registro usando a chave **AppID** .

Uma AppID é um GUID que representa um processo de servidor para uma ou mais classes. Cada classe é associada a exatamente uma AppID, e as AppIDs só podem ser atribuídas a EXEs. As DLLs não recebem AppID, a menos que estejam em execução em um substituto e, em seguida, é o processo substituto que tem a AppID. Se várias DLLs forem carregadas em um substituto, cada substituto terá apenas uma AppID.

Para alguns servidores COM, o código de registro gera uma AppID e coloca entradas no registro que mapeiam o AppID para o nome do executável. Mas alguns servidores COM não fornecem essa funcionalidade. No entanto, se o código de registro do servidor adicionar uma entrada para \\ o% ServerCLSID} \\ [LocalServer32](localserver32.md) CLSID quando dcomcnfg.exe for executado, ele adicionará automaticamente uma AppID para o CLSID.

Para um cliente COM que não é um servidor, esse mapeamento não é criado porque o cliente nunca está registrado. Portanto, para definir a segurança usando a chave **AppID** , o cliente deve criar as entradas de Registro necessárias, seja por meio de programação usando as [funções de registro](/windows/desktop/SysInfo/registry-functions) ou usando o regedit.

Se você decidir definir a segurança de todo o processo no registro sob a chave **AppID** , lembre-se de que há dois valores nomeados na chave **AppID** que você pode definir sem ter permissões de administrador:

-   [AccessPermission](accesspermission.md)
-   [AuthenticationLevel](authenticationlevel.md)

Os valores **AuthenticationLevel** e **AccessPermission** são definidos de forma independente e têm valores padrão separados. Se o valor de **AuthenticationLevel** não estiver presente, o valor de [LegacyAuthenticationLevel](legacyauthenticationlevel.md) será usado como o padrão. Da mesma forma, se o valor de **AccessPermission** não estiver presente, o valor de [DefaultAccessPermission](defaultaccesspermission.md) será usado como o padrão. No entanto, os valores **AuthenticationLevel** e **AccessPermission** são inter-relacionados das seguintes maneiras:

-   Se **AuthenticationLevel** for None, os valores **AccessPermission** e **DefaultAccessPermission** serão ignorados para esse aplicativo.
-   Se o **AuthenticationLevel** não estiver presente e **LegacyAuthenticationLevel** for None, os valores **AccessPermission** e **DefaultAccessPermission** serão ignorados para esse aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo Process-Wide segurança](setting-processwide-security.md)
</dt> </dl>

 

 