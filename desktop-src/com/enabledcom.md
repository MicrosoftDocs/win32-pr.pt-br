---
title: EnableDCOM
description: Controla as políticas de ativação e chamada globais do computador. Somente os administradores e o sistema têm acesso completo a essa parte do Registro. Todos os outros usuários têm acesso somente leitura.
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- Valor do Registro ENABLEDCOM COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74aea79cf600aad4407b96b5c4a10e8f44633a1c928f8b7e376c192b108cb75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793591"
---
# <a name="enabledcom"></a>EnableDCOM

Controla as políticas de ativação e chamada globais do computador. Somente os administradores e o sistema têm acesso completo a essa parte do Registro. Todos os outros usuários têm acesso somente leitura.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ REG SZ.**



| Valor    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| N (ou n) | Nenhum cliente remoto pode iniciar servidores ou se conectar a objetos neste computador. Os clientes locais não podem acessar servidores DCOM remotos; todo o tráfego DCOM está bloqueado. A abertura local do código de classe e a conexão com objetos são permitidas por classe de acordo com o valor e as permissões de acesso do valor do registro [**LaunchPermission**](launchpermission.md) da classe e o valor global do registro [**DefaultLaunchPermission.**](defaultlaunchpermission.md) |
| Y (ou y) | A abertura de servidores e a conexão a objetos por clientes remotos são permitidas por classe de acordo com o valor e as permissões de acesso do valor do registro [**LaunchPermission**](launchpermission.md) da classe e o valor global do registro [**DefaultLaunchPermission.**](defaultlaunchpermission.md)                                                                                                                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[**Launchpermission**](launchpermission.md)
</dt> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 




