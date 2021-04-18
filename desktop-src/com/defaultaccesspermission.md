---
title: DefaultAccessPermission
description: Define a ACL (lista de controle de acesso) das entidades de segurança que podem acessar classes para as quais não há nenhuma configuração AccessPermission.
ms.assetid: 02675d0e-a96c-476e-820e-e6ff3c2d1be1
keywords:
- COM valor do registro DefaultAccessPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c132096807b8c234259071758ebd361421f8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105796144"
---
# <a name="defaultaccesspermission"></a>DefaultAccessPermission

Define a ACL (lista de controle de acesso) das entidades de segurança que podem acessar classes para as quais não há nenhuma configuração [**AccessPermission**](accesspermission.md) . Essa ACL é usada somente por aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e não têm um valor **AccessPermission** sob sua chave [**AppID**](appid-key.md) .

> [!Caution]  
> Não é recomendável que você altere esse valor, pois isso afetará todos os aplicativos de servidor COM que não definem sua própria segurança de todo o processo e pode impedi-los de funcionar corretamente. Se você estiver alterando esse valor para afetar as configurações de segurança para um aplicativo COM específico, em vez disso, deverá alterar as configurações de segurança de todo o processo para esse aplicativo COM específico. Para obter mais informações sobre como definir a segurança de todo o processo, consulte [definindo a segurança de todo o processo](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultAccessPermission = ACL
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ binário reg** .

O tempo de execução COM no servidor verifica a ACL descrita por esse valor ao representar o chamador que está tentando se conectar ao objeto e seu sucesso determina se o acesso é permitido ou não. Se a verificação de acesso falhar, a conexão com o objeto não será permitida. Se esse valor nomeado não existir, somente a entidade de segurança do servidor e o sistema local terão permissão para chamar o servidor.

Por padrão, esse valor não tem entradas nele. Somente a entidade de segurança do servidor e o sistema têm permissão para chamar o servidor.

Esse valor fornece um nível simples de administração centralizada do acesso de conexão padrão à execução de objetos em um computador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**AccessPermission**](accesspermission.md)
</dt> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> <dt>

[Definindo a segurança de todo o processo](setting-processwide-security.md)
</dt> </dl>

 

 




