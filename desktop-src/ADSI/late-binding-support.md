---
title: Suporte à ligação tardia
description: Quando o suporte à associação tardia está em vigor, cada chamada de função deve passar pela interface do ADSI IDispatch, antes de ser redirecionada para a extensão apropriada.
ms.assetid: fbdc6234-9381-4d64-bf02-05e393b3e0bd
ms.tgt_platform: multiple
keywords:
- ADSI de extensões, suporte à associação tardia
- adsi adsi, exemplo de código Visual Basic, suporte de associação tardia
- Associação de anúncio, suporte de associação tardia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff8a66764e49e912e7d4db61356c997516b8d2192046912e673640e9567e415
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821316"
---
# <a name="late-binding-support"></a>Suporte à ligação tardia

Quando o suporte à associação tardia está em vigor, cada chamada de função deve passar pela interface do ADSI [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , antes de ser redirecionada para a extensão apropriada.

Considere o exemplo de código a seguir.


```C++
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
 
x.MyNewMethod( "\\srv\public")
x.MyProperty = "Hello World"
 
x.OtherMethod()
x.OtherProperty = 4362
 
Debug.Print x.LastName
```



Não há chamadas explícitas para o método **QueryInterface** para obter as extensões. As extensões devem redirecionar suas chamadas [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para a interface ADSI **IDispatch** . A ADSI toma a decisão e resolve todos os conflitos que ocorrem e, em seguida, reencaminha para a extensão apropriada usando uma interface chamada [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension). Portanto, qualquer extensão que dê suporte à ligação tardia deve implementar **IADsExtension**.

 

 