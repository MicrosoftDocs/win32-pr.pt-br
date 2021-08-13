---
description: Se você estiver usando a API COM para WMI para recuperar ou armazenar informações de classe localizadas, especifique a localidade no parâmetro strLocale para a interface IWbemLocator::ConnectServer.
ms.assetid: 940a7bd9-c2ea-4deb-b5d8-207a0ce7a616
ms.tgt_platform: multiple
title: Recuperando classes corrigidas usando a API COM para WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3752be42a7111e677e7cd60e0bfe9996350f9ae19e7bd0e168d1fa5da82fe42a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554020"
---
# <a name="retrieving-amended-classes-using-the-com-api-for-wmi"></a>Recuperando classes corrigidas usando a API COM para WMI

Se você estiver usando a API COM para WMI para recuperar ou armazenar informações de classe localizadas, especifique a localidade no parâmetro *strLocale* para a interface [**IWbemLocator::ConnectServer.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) Ao ler ou escrever classes corrigidas, indique que você deseja usar definições de classe localizadas especificando WBEM FLAG USE QUALIFICADORES CORRIGIDOS como um sinalizador para o parâmetro \_ \_ \_ \_ *iFlags.*

A tabela a seguir lista as versões síncronas e assíncronas dos métodos que usam o sinalizador WBEM \_ \_ USE \_ \_ QUALIFICADORES CORRIGIDOS.



| Método síncrono                                                            | Método assíncrono                                                                     |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IWbemServices::CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)       | [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)       |
| [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) | [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) |
| [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)                   | [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   |
| [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)                   | [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   |
| [**IWbemServices::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)                     | [**IWbemServices::P utClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)                     |
| [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)               | [**IWbemServices::P utInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               |



 

 

 



