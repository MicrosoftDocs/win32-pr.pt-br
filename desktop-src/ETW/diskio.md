---
description: Essa classe é a classe pai para eventos de E/S de disco. A sintaxe a seguir é simplificada do código MOF.
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
ms.openlocfilehash: 0e91f5e8b84d77b0938f35da69a84c26fa0f34a4da63bce40330484a29e19b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118395297"
---
# <a name="diskio-class"></a>Classe DiskIo

Essa classe é a classe pai para eventos de E/S de disco.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c}")]
class DiskIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A **classe DiskIo** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar eventos de E/S de disco em uma sessão de registro em log do Kernel NT, especifique o sinalizador **DE \_ \_ \_ \_ E/S** DO SINALIZADOR DE RASTREAMENTO DE EVENTOS no membro **EnableFlags** de uma estrutura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a [**função StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea) Você também pode especificar um ou mais dos seguintes sinalizadores:

-   **EVENT \_ TRACE \_ FLAG \_ DISK \_ IO \_ INIT**
-   **DRIVER DO \_ SINALIZADOR DE RASTREAMENTO DE \_ \_ EVENTOS**

Os consumidores de rastreamento de eventos podem implementar o processamento especial para eventos de E/S de disco chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**DiskIoGuid**](nt-kernel-logger-constants.md) como o *parâmetro pGuid.* Use os seguintes tipos de evento para identificar o evento de E/S de disco real ao consumir eventos.



| Tipo de evento                                                                      | Descrição                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ IO \_ READ**(O valor do tipo de evento é 10)<br/>             | Evento de leitura. A [**classe \_ MOF DiskIo TypeGroup1**](diskio-typegroup1.md) define os dados de evento para esse evento.                                              |
| **EVENTO \_ TRACE \_ TYPE \_ IO \_ WRITE**(o valor do tipo de evento é 11)<br/>            | Gravar evento. A [**classe \_ MOF DiskIo TypeGroup1**](diskio-typegroup1.md) define os dados de evento para esse evento.                                             |
| **EVENTO \_ TRACE \_ TYPE \_ IO READ \_ \_ INIT**(O valor do tipo de evento é 12)<br/>       | Inicializar evento de leitura. A [**classe \_ MOF DiskIo TypeGroup2**](diskio-typegroup2.md) define os dados de evento para esse evento.                                   |
| **EVENTO \_ TRACE \_ TYPE \_ IO WRITE \_ \_ INIT**(O valor do tipo de evento é 13)<br/>      | Inicializar evento de gravação. A [**classe \_ MOF DiskIo TypeGroup2**](diskio-typegroup2.md) define os dados de evento para esse evento.                                  |
| **EVENTO \_ TRACE \_ TYPE \_ IO \_ FLUSH**(o valor do tipo de evento é 14)<br/>            | Inicializar evento de gravação. A [**classe \_ MOF DiskIo TypeGroup3**](diskio-typegroup3.md) define os dados de evento para esse evento.                                  |
| **EVENTO \_ TRACE \_ TYPE \_ IO FLUSH \_ \_ INIT**(o valor do tipo de evento é 15)<br/>      | Inicializar evento de liberação. A [**classe \_ MOF DiskIo TypeGroup2**](diskio-typegroup2.md) define os dados de evento para esse evento.                                  |
| **EVENTO \_ TRACE \_ TYPE \_ IO \_ REDIRECTED \_ INIT**(O valor do tipo de evento é 16)<br/> | Inicializar evento redirecionado. Eventos de E/S redirecionados são usados para mapear E/Ss de disco para um WIM (formato de imagem de Windows) para o nome de arquivo dentro do WIM.                  |
| O valor do tipo de evento é 52<br/>                                               | Evento de solicitação de conclusão do driver. A [**classe MOF DriverCompleteRequest**](drivercompleterequest.md) define os dados de evento para esse evento.                    |
| O valor do tipo de evento é 53<br/>                                               | Evento de retorno de solicitação completa do driver. A [**classe MOF DriverCompleteRequestReturn**](drivercompleterequestreturn.md) define os dados de evento para esse evento. |
| O valor do tipo de evento é 37<br/>                                               | Evento de rotina de conclusão do driver. A [**classe MOF DriverCompletionRoutine**](drivercompletionroutine.md) define os dados de evento para esse evento.              |
| O valor do tipo de evento é 34<br/>                                               | Evento de chamada de função principal do driver. A [**classe MOF DriverMajorFunctionCall**](drivermajorfunctioncall.md) define os dados de evento para esse evento.             |
| O valor do tipo de evento é 35<br/>                                               | Evento de retorno de chamada de função principal do driver. A [**classe MOF DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) define os dados de evento para esse evento.  |



 

O provedor de E/S de disco não pode identificar qual arquivo é lido ou gravado durante um evento de E/S de disco. Para recuperar o nome do arquivo associado ao evento de E/S de disco, habilita o provedor de eventos de E/S do arquivo.

Eventos de E/S de disco são registrados no momento da conclusão de E/S. Para determinar quando a operação de E/S começou, use os eventos de inicialização, por exemplo, EVENT \_ TRACE \_ TYPE \_ IO READ \_ \_ INIT.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |



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

 

 
