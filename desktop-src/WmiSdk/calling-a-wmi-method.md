---
title: Como chamar um método WMI
description: A principal finalidade do WMI é fornecer acesso a classes e instâncias que representam objetos em sua rede.
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d1de14f06388454228528d5a419b551ae2ed0d72c82e3b78c9e04855db6619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051044"
---
# <a name="how-to-call-a-wmi-method"></a>Como chamar um método WMI

A principal finalidade do WMI é fornecer acesso a classes e instâncias que representam objetos em sua rede. Essas classes e instâncias têm suporte dos provedores. Por exemplo, todas as instâncias que representam dispositivos de hardware padrão em sua empresa, como [**Win32 \_ PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) ou [**Win32 \_ Printer,**](/windows/desktop/CIMWin32Prov/win32-printer)têm suporte do provedor Win32. Da mesma forma, você pode acessar o log de eventos por meio do provedor de Log de Eventos e do Registro por meio do provedor do Registro.

Os métodos que o WMI implementa em interfaces como [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) ou objetos de script, como [**SWbemServices**](swbemservices.md), são principalmente para obter e manipular genericamente os dados fornecidos por qualquer provedor. Por exemplo, use [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) para obter todas as instâncias do [**Processo Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) em um subconjunto de computadores empresariais. Em seguida, você pode chamar o método de provedor [**Win32 GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) em cada **objeto win32 \_ Process.**

No exemplo a seguir, o [**método GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) é chamado como um método de automação no objeto Process. Um método WMI, como o [**método \_ Path**](swbemobject-path-.md) definido para [**SWbemObject,**](swbemobject.md) também pode ser chamado no **objeto** Process.


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



O processo real de usar os métodos WMI é idêntico ao uso de qualquer outro Windows com ou interface de automação. Para obter mais informações, [consulte COM](../cossdk/component-services-portal.md) e Criando um [aplicativo WMI ou script](creating-a-wmi-application-or-script.md). Para obter mais informações sobre as interfaces compatíveis com o WMI, consulte [API COM para WMI](com-api-for-wmi.md) e [API de Script para WMI](scripting-api-for-wmi.md).

Para obter mais informações, consulte [Manipulando informações de classe e instância](manipulating-class-and-instance-information.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chamando um método](calling-a-method.md)
</dt> </dl>

 

 
