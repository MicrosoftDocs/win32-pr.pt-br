---
title: LaunchPermission
description: Descreve a lista de controle de acesso (ACL) das entidades de segurança que podem iniciar novos servidores para essa classe. Esse valor pode ser adicionado sob qualquer chave AppID para limitar a ativação por clientes remotos de classes específicas.
ms.assetid: 7b8c1ae4-fbbd-489f-b1b5-60ae5a04f906
keywords:
- COM valor do registro LaunchPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e4c50568cae791f08b47fc44e10cc0d35fef07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006169"
---
# <a name="launchpermission"></a>LaunchPermission

Descreve a lista de controle de acesso (ACL) das entidades de segurança que podem iniciar novos servidores para essa classe. Esse valor pode ser adicionado sob qualquer chave [**AppID**](appid-key.md) para limitar a ativação por clientes remotos de classes específicas.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LaunchPermission = ACL
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ binário reg** . Após o recebimento de uma solicitação local ou remota para iniciar o servidor dessa classe, a ACL descrita por esse valor é verificada ao representar o cliente e seu sucesso permite ou não a inicialização do servidor. Se esse valor não existir, o valor de [**DefaultLaunchPermission**](defaultlaunchpermission.md) será verificado da mesma maneira para determinar se o código de classe pode ser iniciado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 




