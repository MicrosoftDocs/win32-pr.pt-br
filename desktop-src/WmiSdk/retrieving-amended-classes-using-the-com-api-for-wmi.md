---
description: 'Se você estiver usando a API COM para que o WMI recupere ou armazene informações de classe localizadas, especifique a localidade no parâmetro strLocale para a interface IWbemLocator:: ConnectServer.'
ms.assetid: 940a7bd9-c2ea-4deb-b5d8-207a0ce7a616
ms.tgt_platform: multiple
title: Recuperando classes corrigidas usando a API COM para o WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0178b0b99de2b666e2f497074a02b02c49ba400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663242"
---
# <a name="retrieving-amended-classes-using-the-com-api-for-wmi"></a>Recuperando classes corrigidas usando a API COM para o WMI

Se você estiver usando a API COM para que o WMI recupere ou armazene informações de classe localizadas, especifique a localidade no parâmetro *strLocale* para a interface [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) . Ao ler ou gravar classes corrigidas, indique que você deseja usar definições de classe localizadas \_ especificando \_ o sinalizador WBEM use \_ \_ qualificadores corrigidos como um sinalizador para o parâmetro *iFlags* .

A tabela a seguir lista as versões síncronas e assíncronas dos métodos que usam o sinalizador WBEM \_ \_ usar \_ sinalizador de \_ qualificadores corrigidos.



| Método síncrono                                                            | Método assíncrono                                                                     |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IWbemServices:: CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)       | [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)       |
| [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) | [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) |
| [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)                   | [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   |
| [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)                   | [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   |
| [**IWbemServices::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)                     | [**IWbemServices::P utClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)                     |
| [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)               | [**IWbemServices::P utInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               |



 

 

 



