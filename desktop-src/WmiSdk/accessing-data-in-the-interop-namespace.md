---
description: Provedores de associação permitem que clientes Instrumentação de Gerenciamento do Windows (WMI) percorram e recuperem perfis e instâncias de classe associadas de namespaces diferentes.
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: Acessando dados no namespace Interop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a217a7a44651b1a6c94476b53193eedac7f0d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922599"
---
# <a name="accessing-data-in-the-interop-namespace"></a>Acessando dados no namespace Interop

Provedores de associação permitem que clientes Instrumentação de Gerenciamento do Windows (WMI) percorram e recuperem perfis e instâncias de classe associadas de namespaces diferentes.

Provedores de associação e classes residem no \\ \\ \\ namespace de interoperabilidade raiz. Para obter mais informações, consulte [passagem de associação de namespace cruzado](cross-namespace-association-traversal.md) e [gravando um provedor de associação](writing-an-association-provider-for-interop.md).

Provedores de associação expõem perfis padrão, como um perfil de energia. Os exemplos a seguir usam o perfil de energia para ilustrar como descobrir e acessar dados por meio do namespace Interop.

O Windows PowerShell fornece um mecanismo simples para percorrer a associação apropriada, recuperar um perfil de dispositivo e chamar um método.

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a>Enumerando perfis no namespace root/Interop

O seguinte comando do Windows PowerShell enumera os perfis com suporte da[DMTF](https://www.dmtf.org/standards/wsman)(Distributed Management Task Force) em um computador com o Windows 7:


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a>Recuperando instâncias de um perfil de dispositivo específico

O comando do Windows PowerShell a seguir retorna todas as instâncias de um perfil especificado por meio do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)):


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a>Atribuindo o perfil de energia a uma variável

O seguinte comando do Windows PowerShell atribui a instância do perfil de energia a uma variável:


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a>Enumerando os planos de energia em um computador

O seguinte comando do Windows PowerShell enumera os planos de perfil de energia disponíveis:


```PowerShell
$pplan
```



## <a name="calling-a-method"></a>Chamando um método

O comando do Windows PowerShell a seguir chama o método [**Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) para o plano de energia:


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Passagem de associação entre namespaces](cross-namespace-association-traversal.md)
</dt> <dt>

[Escrevendo um provedor de associação](writing-an-association-provider-for-interop.md)
</dt> <dt>

[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**\_PowerPlan Win32**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))
</dt> </dl>

 

 
