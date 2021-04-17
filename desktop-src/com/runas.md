---
title: RunAs
description: Configura uma classe para ser executada em uma conta de usuário específica quando ativada por um cliente remoto sem ser escrita como um aplicativo de serviço.
ms.assetid: 2325a7da-8acd-41f4-a658-36a02532505a
keywords:
- Valor do registro RunAs COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3139d12864eb92cc153b919dc4b9b9a4059379d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105812151"
---
# <a name="runas"></a>RunAs

Configura uma classe para ser executada em uma conta de usuário específica quando ativada por um cliente remoto sem ser escrita como um aplicativo de serviço.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RunAs = value
```

## <a name="remarks"></a>Comentários

O valor especifica o nome de usuário e deve ser um dos formulários *username*, *Domain ***\\*** username* ou da cadeia de caracteres "Interactive User". Você também pode especificar as cadeias de caracteres "NT Authority \\ LocalService" (para o serviço local) e "NT Authority \\ NetworkService" (para serviço de rede). Você também pode especificar a cadeia de caracteres "NT Authority \\ System" quando {*AppID \_ GUID*} se refere a um servidor com que já foi iniciado ou que tem uma entrada na tabela de classes. No entanto, não é possível usar "NT Authority \\ System" com um servidor com que ainda não tenha sido iniciado. A senha padrão para "NT Authority \\ LocalService", "NT Authority \\ NetworkService" e "NT Authority \\ System" é "" (cadeia de caracteres vazia).

> [!Note]  
> A partir do Windows Vista, uma senha vazia não é mais necessária para configurar as configurações de runas "NT Authority \\ LocalService", "NT Authority \\ NetworkService" e "NT Authority \\ System". 

 

As classes configuradas para execução como um usuário específico não podem ser registradas em nenhuma outra identidade, portanto, as chamadas para [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) com esse CLSID falham, a menos que o processo tenha sido iniciado pelo com em nome de uma solicitação de ativação real.

O nome de usuário é obtido do valor **runas** na chave **AppID** da classe. Se o nome de usuário for "usuário interativo", o servidor será executado na identidade do usuário conectado no momento e conectado à área de trabalho interativa.

Caso contrário, a senha será recuperada de uma parte do registro que está disponível somente para os administradores do computador e para o sistema. O nome de usuário e a senha são usados para criar uma sessão de logon na qual o servidor é executado. Quando iniciada dessa forma, o usuário é executado com sua própria área de trabalho e estação de janela e não compartilha identificadores de janela, área de transferência ou outros elementos de interface do usuário com usuários interativos ou outros usuários em execução em outras contas de usuário.

Para estabelecer uma senha para uma classe **runas** , você deve usar a ferramenta administrativa DCOMCNFG instalada no diretório do sistema.

Para identidades **runas** usadas pelos servidores DCOM, a conta de usuário especificada no valor deve ter os direitos de fazer logon como um trabalho em lotes. Esse direito pode ser adicionado usando a ferramenta administrativa política de segurança local. Vá para **políticas locais** e abra **atribuição de direitos de usuário**. Selecione **fazer logon como um trabalho em lotes** e adicione a conta de usuário.

O valor **runas** não é usado para servidores configurados para serem executados como serviços. Os serviços COM que precisam ser executados com uma identidade diferente do LocalSystem devem definir o nome de usuário e a senha apropriados usando o miniaplicativo serviços do painel de controle ou as funções do controlador de serviço. (Para obter mais informações sobre essas funções, consulte [Serviços](/windows/desktop/Services/services).)

> [!Note]  
> A partir do Microsoft Windows Server 2003, a classe AppID é lida explicitamente a partir do **HKEY \_ local \_ Machine \\ software \\ classes \\ AppID**, que, ao contrário da maioria das chaves do registro, não é intercambiável com a **\_ \_ \\ AppID raiz das classes hKey**.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> </dl>

 

 