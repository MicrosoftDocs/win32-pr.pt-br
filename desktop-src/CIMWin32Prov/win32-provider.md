---
description: O Microsoft&\# 160; o provedor Win32 recupera e atualiza dados relevantes para Windows sistemas&\# 8212; dados como as configurações atuais de variáveis de ambiente e os atributos de um disco lógico.
ms.assetid: 71c13736-0504-4d50-b8a4-5d68d4ba9a90
ms.tgt_platform: multiple
title: Provedor Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca4426f849b59dfbfb5f667c32e8e3b9cd47ca7482fd3547d631592a080f968
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118007769"
---
# <a name="win32-provider"></a>Provedor Win32

o provedor do Microsoft Win32 recupera e atualiza os dados relevantes para Windows sistemas — dados como as configurações atuais de variáveis de ambiente e os atributos de um disco lógico. Com o provedor do Win32, os aplicativos de gerenciamento podem usar o WMI para acessar facilmente esses dados. o provedor Win32 recupera suas informações fazendo Windows chamadas de função e consultando o registro do sistema.

o provedor Win32 define as classes usadas para descrever o hardware ou software disponível em sistemas Windows e as relações entre eles.

Como um provedor de instância e método, o provedor Win32 implementa a interface [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) padrão, bem como os seguintes métodos de [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) :

-   [**CreateInstanceEnumAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**DeleteInstanceAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [**ExecMethodAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

A tabela a seguir lista as categorias de classe do provedor do Win32.



| Classes                                                                             | Descrição                                                               |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Classes de hardware do sistema de computador](computer-system-hardware-classes.md)<br/> | Objetos relacionados ao hardware.<br/>                                      |
| [Classes do sistema operacional](operating-system-classes.md)<br/>                 | Objetos relacionados ao sistema operacional.<br/>                              |
| [Classes de contador de desempenho](performance-counter-classes.md)<br/>           | Dados de desempenho brutos e calculados dos contadores de desempenho.<br/> |
| [Classes de gerenciamento de serviço WMI](wmi-service-management-classes.md)<br/>     | Gerenciamento do WMI.<br/>                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Provedor WMI do CIMWin32](cimwin32-wmi-providers.md)
</dt> </dl>

 

 
