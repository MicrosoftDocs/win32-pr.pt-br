---
title: MachineLaunchRestriction
description: Define a política de restrição de todo o computador para inicialização e ativação de componentes.
ms.assetid: 274e3d08-1f38-4179-b7e7-b218d6e184ee
keywords:
- COM valor do registro MachineLaunchRestriction COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5cd235e2dd81e596448f25adfd72ad0b16c13d2da3860eb56fb95f93ef53cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048054"
---
# <a name="machinelaunchrestriction"></a>MachineLaunchRestriction

Define a política de restrição de todo o computador para inicialização e ativação de componentes.

> [!Caution]  
> A alteração desse valor afetará todos os aplicativos de servidor COM e poderá impedi-lo de funcionar corretamente. Se houver aplicativos de servidor COM que tenham restrições menos rigorosas do que as restrições em todo o computador, reduzir as restrições de computador poderá expor esses aplicativos para acesso indesejado. Por outro lado, se você aumentar as restrições de todo o computador, alguns aplicativos de servidor COM podem não estar mais acessíveis chamando aplicativos.

 

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineLaunchRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ binário reg** .

As entidades não dadas as permissões aqui não podem obtê-las mesmo se as permissões forem concedidas pelo valor do registro [DefaultAccessPermission](defaultaccesspermission.md) ou pela função [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) .

Por padrão, os administradores podem obter permissões locais e remotas de inicialização e ativação, e os membros do grupo Everyone podem obter as permissões de ativação local e de inicialização.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo a segurança para aplicativos COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




