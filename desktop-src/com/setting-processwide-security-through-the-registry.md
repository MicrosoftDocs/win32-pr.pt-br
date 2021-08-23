---
title: Definindo Process-Wide segurança por meio do Registro
description: Se você quiser definir a segurança de um processo inteiro, uma solução será definir os níveis de segurança que você deseja no Registro.
ms.assetid: 87f0a64f-f3ec-4ee2-8d65-4f82e8971f0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8ad3a549a78a10b15e965ba2e2a47b9e5e84f1e8790ccfbf90af622051714e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730906"
---
# <a name="setting-process-wide-security-through-the-registry"></a>Definindo Process-Wide segurança por meio do Registro

Se você quiser definir a segurança de um processo inteiro, uma solução será definir os níveis de segurança que você deseja no Registro. Se seu aplicativo não puder chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou se você preferir não usar a segurança programática, essa poderá ser uma boa opção. Se você decidir definir a segurança em todo o processo usando o Registro, deverá estar ciente de que, se você chamar **CoInitializeSecurity** em seu programa COM, usará os valores em **CoInitializeSecurity** e ignorará os valores do Registro.

Há duas maneiras de definir a segurança no Registro para seu aplicativo:

-   Você pode usar Dcomcnfg.exe, que fornece uma interface do usuário simples para modificar valores de segurança. Todos os servidores COM podem ser configurados usando Dcomcnfg.exe. Para obter mais informações, consulte [Configurando Process-Wide segurança usando DCOMCNFG](setting-processwide-security-using-dcomcnfg.md). No entanto, os aplicativos cliente normalmente não aparecem no Dcomcnfg.exe a menos que o cliente crie um GUID e o insira no Registro.
-   Você pode definir valores de segurança na [chave AppID](appid-key.md) para o aplicativo. O restante deste tópico explica como definir a segurança no Registro usando a **chave AppID.**

Uma AppID é um GUID que representa um processo de servidor para uma ou mais classes. Cada classe está associada a exatamente uma AppID, e AppIDs podem ser atribuídos somente a EXEs. As DLLs não têm AppIDs, a menos que sejam executados em um substituto e, em seguida, é o processo substituto que tem a AppID. Se várias DLLs são carregadas em um substituto, cada substituto tem apenas uma AppID.

Para alguns servidores COM, o código de registro gera uma AppID e coloca entradas no Registro que mapeiam o AppID para o nome do executável. Mas alguns servidores COM não fornecem essa funcionalidade. No entanto, se o código de registro do servidor adicionar uma entrada para \\ CLSID do HKCR{ServerCLSID} \\ [LocalServer32](localserver32.md) quando dcomcnfg.exe for executado, ele adicionará automaticamente uma AppID para o CLSID.

Para um cliente COM que não é um servidor, esse mapeamento não é criado porque o cliente nunca é registrado. Portanto, para definir a segurança usando a **chave AppID,** o cliente deve criar [](/windows/desktop/SysInfo/registry-functions) as entradas de Registro necessárias, seja programaticamente usando as funções do Registro ou usando regedit.

Se você decidir definir a segurança em todo o processo no Registro sob a chave **AppID,** esteja ciente de que há dois valores nomeados na chave **AppID** que você pode definir sem ter permissões de administrador:

-   [Accesspermission](accesspermission.md)
-   [Authenticationlevel](authenticationlevel.md)

Os **valores AuthenticationLevel** **e AccessPermission** são definidos independentemente e têm valores padrão separados. Se o **valor AuthenticationLevel** não estiver presente, [o valor LegacyAuthenticationLevel](legacyauthenticationlevel.md) será usado como o padrão. Da mesma forma, se **o valor AccessPermission** não estiver presente, o valor [DefaultAccessPermission](defaultaccesspermission.md) será usado como o padrão. No entanto, **os valores AuthenticationLevel** e **AccessPermission** são inter-relacionados das seguintes maneiras:

-   Se **o AuthenticationLevel** não for nenhum, os valores **AccessPermission** e **DefaultAccessPermission** serão ignorados para esse aplicativo.
-   Se **AuthenticationLevel** não estiver presente e **LegacyAuthenticationLevel** não for nenhum, os valores **AccessPermission** e **DefaultAccessPermission** serão ignorados para esse aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo Process-Wide segurança](setting-processwide-security.md)
</dt> </dl>

 

 