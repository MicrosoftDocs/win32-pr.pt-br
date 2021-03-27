---
description: Essa classe é a classe pai para eventos de e/s de disco. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 630fb6c6-b505-4384-ab7b-ee898d95bd41
title: Classe DiskIo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 97f9907e4da51675bb1a5f562931e471ee0e133e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920736"
---
# <a name="diskio-class"></a>Classe DiskIo

Essa classe é a classe pai para eventos de e/s de disco.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c}")]
class DiskIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A classe **DiskIo** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar eventos I/0 de disco em uma sessão de log de kernel NT, especifique o sinalizador de **\_ \_ \_ \_ e/s do disco do sinalizador de rastreamento de eventos** no membro **EnableFlags** de uma estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . Você também pode especificar um ou mais dos seguintes sinalizadores:

-   **sinalizador de rastreamento de eventos \_ \_ \_ inicialização de \_ e/s de disco \_**
-   **\_Driver de \_ sinalizador de rastreamento de eventos \_**

Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de e/s de disco chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**DiskIoGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* . Use os seguintes tipos de evento para identificar o evento de e/s de disco real ao consumir eventos.



| Tipo de evento                                                                      | Descrição                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de \_Leitura de \_ e \_ /s do tipo de rastreamento**(o valor do tipo de evento é 10)<br/>             | Ler evento. A classe [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) MOF define os dados do evento para esse evento.                                              |
| **Evento \_ de \_Gravação de \_ e \_ /s do tipo de rastreamento**(o valor do tipo de evento é 11)<br/>            | Evento de gravação. A classe [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) MOF define os dados do evento para esse evento.                                             |
| **Evento \_ de Tipo de rastreamento \_ \_ e/s \_ leitura \_ init**(o valor do tipo de evento é 12)<br/>       | Inicializar evento de leitura. A classe [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) MOF define os dados do evento para esse evento.                                   |
| **Evento \_ de Tipo de rastreamento \_ \_ Io \_ Write \_ init**(o valor do tipo de evento é 13)<br/>      | Inicializar evento de gravação. A classe [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) MOF define os dados do evento para esse evento.                                  |
| **Evento \_ de Tipo de rastreamento \_ \_ e \_ liberação de e/s**(o valor do tipo de evento é 14)<br/>            | Inicializar evento de gravação. A classe [**DiskIo \_ TypeGroup3**](diskio-typegroup3.md) MOF define os dados do evento para esse evento.                                  |
| **Evento \_ de Tipo de rastreamento \_ \_ Io \_ flush \_ init**(o valor do tipo de evento é 15)<br/>      | Inicializar evento de liberação. A classe [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) MOF define os dados do evento para esse evento.                                  |
| **Evento \_ de Tipo de rastreamento \_ \_ e/s \_ \_ inicialização redirecionada**(o valor do tipo de evento é 16)<br/> | Inicializar evento Redirecionado. Os eventos de e/s redirecionados são usados para mapear o IOs de disco para um formato WIM (Windows Imaging) para o nome de arquivo dentro do WIM.                  |
| O valor do tipo de evento é 52<br/>                                               | Evento de solicitação de conclusão de driver. A classe MOF [**DriverCompleteRequest**](drivercompleterequest.md) define os dados do evento para esse evento.                    |
| O valor do tipo de evento é 53<br/>                                               | Evento de retorno de solicitação de conclusão de driver. A classe MOF [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) define os dados do evento para esse evento. |
| O valor do tipo de evento é 37<br/>                                               | Evento de rotina de conclusão do driver. A classe MOF [**DriverCompletionRoutine**](drivercompletionroutine.md) define os dados do evento para esse evento.              |
| O valor do tipo de evento é 34<br/>                                               | Evento de chamada de função principal do driver. A classe MOF [**DriverMajorFunctionCall**](drivermajorfunctioncall.md) define os dados do evento para esse evento.             |
| O valor do tipo de evento é 35<br/>                                               | Evento de retorno de chamada de função principal do driver. A classe MOF [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) define os dados do evento para esse evento.  |



 

O provedor I/0 de disco não pode identificar qual arquivo é lido ou gravado durante um evento de e/s de disco. Para recuperar o nome do arquivo associado ao evento de e/s de disco, habilite o provedor de eventos arquivo I/0.

Os eventos de e/s de disco são registrados no tempo de conclusão de e/s. Para determinar quando a operação de e/s foi iniciada, use os eventos de inicialização, por exemplo, o tipo de rastreamento de evento \_ \_ \_ Io \_ Read \_ init.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DiskIo \_ TypeGroup1**](diskio-typegroup1.md)
</dt> <dt>

[**DiskIo \_ TypeGroup2**](diskio-typegroup2.md)
</dt> <dt>

[**DiskIo \_ TypeGroup3**](diskio-typegroup3.md)
</dt> <dt>

[**DriverCompleteRequest**](drivercompleterequest.md)
</dt> <dt>

[**DriverCompleteRequestReturn**](drivercompleterequestreturn.md)
</dt> <dt>

[**DriverCompletionRoutine**](drivercompletionroutine.md)
</dt> <dt>

[**DriverMajorFunctionCall**](drivermajorfunctioncall.md)
</dt> <dt>

[**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md)
</dt> </dl>

 

 
