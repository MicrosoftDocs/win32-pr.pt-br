---
title: EnableDCOM
description: Controla a ativação global e as políticas de chamada do computador. Somente administradores e o sistema têm acesso total a essa parte do registro. Todos os outros usuários têm acesso somente leitura.
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- COM valor do registro EnableDCOM COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42cc95b24522e87e4b64f6feefc5c6c56ad5341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363844"
---
# <a name="enabledcom"></a>EnableDCOM

Controla a ativação global e as políticas de chamada do computador. Somente administradores e o sistema têm acesso total a essa parte do registro. Todos os outros usuários têm acesso somente leitura.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a>Comentários

Este é um valor de **\_ sz do reg** .



| Valor    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| N (ou n) | Nenhum cliente remoto pode iniciar servidores ou conectar-se a objetos neste computador. Os clientes locais não podem acessar servidores DCOM remotos; todo o tráfego DCOM está bloqueado. A inicialização local do código de classe e a conexão a objetos são permitidas por classe, de acordo com o valor e as permissões de acesso do valor do registro [**LaunchPermission**](launchpermission.md) da classe e o valor do registro global [**DefaultLaunchPermission**](defaultlaunchpermission.md) . |
| Y (ou y) | A inicialização de servidores e a conexão a objetos por clientes remotos é permitida por classe, de acordo com o valor e as permissões de acesso do valor do registro [**LaunchPermission**](launchpermission.md) da classe e o valor do registro global [**DefaultLaunchPermission**](defaultlaunchpermission.md) .                                                                                                                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[**LaunchPermission**](launchpermission.md)
</dt> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 




