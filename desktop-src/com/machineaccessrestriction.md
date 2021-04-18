---
title: MachineAccessRestriction
description: Define a política de restrição de todo o computador para acesso ao componente.
ms.assetid: aeb37e49-6425-4058-968e-f9d00acf4fc2
keywords:
- COM valor do registro MachineAccessRestriction COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d99e747b8a38dbb41cb8a6a8adc0935d3f9fa8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788865"
---
# <a name="machineaccessrestriction"></a>MachineAccessRestriction

Define a política de restrição de todo o computador para acesso ao componente.

> [!Caution]  
> A alteração desse valor afetará todos os aplicativos de servidor COM e poderá impedi-lo de funcionar corretamente. Se houver aplicativos de servidor COM que tenham restrições menos rigorosas do que as restrições em todo o computador, reduzir as restrições de computador poderá expor esses aplicativos para acesso indesejado. Por outro lado, se você aumentar as restrições de todo o computador, alguns aplicativos de servidor COM podem não estar mais acessíveis chamando aplicativos.

 

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineAccessRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ binário reg** .

As entidades não dadas as permissões aqui não podem obtê-las mesmo se as permissões forem concedidas pelo valor do registro [DefaultAccessPermission](defaultaccesspermission.md) ou pela função [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) .

Por padrão, os membros do grupo Everyone podem obter permissões de acesso local e remota, e os usuários anônimos podem obter permissões de acesso local.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo a segurança para aplicativos COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




