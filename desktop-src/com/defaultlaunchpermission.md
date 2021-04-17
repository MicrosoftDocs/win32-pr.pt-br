---
title: DefaultLaunchPermission
description: Define a ACL (lista de controle de acesso) das entidades de segurança que podem iniciar classes que não especificam sua própria ACL por meio do valor do registro LaunchPermission.
ms.assetid: 23ca87fc-7829-46a9-9fc3-2cd7f677bbff
keywords:
- COM valor do registro DefaultLaunchPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599a0993a4a1238e57e357f428f7046331412cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811659"
---
# <a name="defaultlaunchpermission"></a>DefaultLaunchPermission

Define a ACL (lista de controle de acesso) das entidades de segurança que podem iniciar classes que não especificam sua própria ACL por meio do valor do registro [**LaunchPermission**](launchpermission.md) .

> [!Caution]  
> Não é recomendável que você altere esse valor, pois isso afetará todos os aplicativos de servidor COM que não definem sua própria segurança de todo o processo e pode impedi-los de funcionar corretamente. Se você estiver alterando esse valor para afetar as configurações de segurança para um aplicativo COM específico, em vez disso, deverá alterar as configurações de segurança de todo o processo para esse aplicativo COM específico. Para obter mais informações sobre como definir a segurança de todo o processo, consulte [definindo a segurança de todo o processo](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultLaunchPermission = ACL
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ binário reg** .

As permissões de acesso padrão são as seguintes:

-   Administradores: permitir inicialização
-   SISTEMA: permitir inicialização
-   INTERATIVO: permitir inicialização

Se o valor de [**LaunchPermission**](launchpermission.md) for definido para um servidor, ele terá precedência sobre o valor de **DefaultLaunchPermission** . Ao receber uma solicitação local ou remota para iniciar um servidor cuja chave [**AppID**](appid-key.md) não tem nenhum valor **LaunchPermission** próprio, a ACL descrita por esse valor é verificada ao representar o cliente e seu sucesso permite ou não a inicialização do código de classe.

Esse valor fornece um nível simples de administração centralizada do acesso de inicialização padrão a classes não administradas de outra forma em um computador. Por exemplo, um administrador pode usar a ferramenta DCOMCNFG para configurar o sistema para permitir o acesso somente leitura para usuários avançados. Portanto, o OLE restringiria as solicitações para iniciar o código de classe para membros do grupo usuários avançados. Um administrador pode, subsequentemente, configurar permissões de inicialização para classes individuais para conceder a capacidade de iniciar o código de classe para outros grupos ou usuários individuais, conforme necessário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**LaunchPermission**](launchpermission.md)
</dt> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> <dt>

[Definindo a segurança de todo o processo](setting-processwide-security.md)
</dt> </dl>

 

 




