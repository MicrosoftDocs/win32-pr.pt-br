---
description: Essa classe é a classe pai para eventos de registro. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 362d7653-1ba0-45b7-80f3-0fccca0badf1
title: Classe de registro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6799756ebfe573fad6a32a191e79c3c2b745f563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090644"
---
# <a name="registry-class"></a>Classe de registro

Essa classe é a classe pai para eventos de registro.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{ae53722e-c863-11d2-8659-00c04fa321a1}"), EventVersion(2)]
class Registry : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A classe de **registro** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar eventos de registro em uma sessão de log de kernel NT, especifique o registro de sinalizador de rastreamento de eventos no membro **EnableFlags** de uma estrutura de [](/windows/win32/api/evntrace/nf-evntrace-starttracea) [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função StartTrace. **\_ \_ \_**

Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de registro chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**RegistryGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* . Use os tipos de evento a seguir para identificar o evento de registro real ao consumir eventos.



| Tipo de evento                                                                       | Descrição                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de Tipo de rastreamento \_ \_ REGCREATE**(o valor do tipo de evento é 10)<br/>             | Criar evento de chave. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento.                                                                                            |
| **Evento \_ de Tipo de rastreamento \_ \_ REGDELETE**(o valor do tipo de evento é 12)<br/>             | Excluir evento de chave. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento.                                                                                            |
| **Evento \_ de Tipo de rastreamento \_ \_ falha em RegDeleteValue**(o valor do tipo de evento é 15)<br/>        | Evento de exclusão de valor. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento.                                                                                          |
| **Evento \_ de Tipo de rastreamento \_ \_ REGENUMERATEKEY**(o valor do tipo de evento é 17)<br/>       | Enumerar evento de chave. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento.                                                                                         |
| **Evento \_ de Tipo de rastreamento \_ \_ REGENUMERATEVALUEKEY**(o valor do tipo de evento é 18)<br/>  | Evento de chave de valor de enumeração. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento.                                                                                   |
| **Evento \_ de Tipo de rastreamento \_ \_ REGFLUSH**(o valor do tipo de evento é 21)<br/>              | Evento de chave de liberação. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento.                                                                                             |
| **Evento \_ de Tipo de rastreamento \_ \_ REGKCBDMP**(o valor do tipo de evento é 22)<br/>             | Criar evento de chave. Gerado quando uma operação de registro usa identificadores em vez de cadeias de caracteres para referenciar subchaves. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento. |
| **Evento \_ de Tipo de rastreamento \_ \_ REGOPEN**(o valor do tipo de evento é 11)<br/>               | Abrir evento de chave. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento.                                                                                              |
| **Evento \_ de Tipo de rastreamento \_ \_ REGQUERY**(o valor do tipo de evento é 13)<br/>              | Evento de chave de consulta. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento.                                                                                             |
| **Evento \_ de Tipo de rastreamento \_ \_ REGQUERYMULTIPLEVALUE**(o valor do tipo de evento é 19)<br/> | Evento consultar vários valores. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento.                                                                                  |
| **Evento \_ de Tipo de rastreamento \_ \_ REGQUERYVALUE**(o valor do tipo de evento é 16)<br/>         | Evento de valor da consulta. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento.                                                                                           |
| **Evento \_ de Tipo de rastreamento \_ \_ REGSETINFORMATION**(o valor do tipo de evento é 20)<br/>     | Definir evento de informações. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento.                                                                                       |
| **Evento \_ de Tipo de rastreamento \_ \_ REGSETVALUE**(o valor do tipo de evento é 14)<br/>           | Definir evento de valor. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento.                                                                                             |
| Valor do tipo de evento, 23                                                             | excluir evento de chave. Gerado quando uma operação de registro usa identificadores em vez de cadeias de caracteres para referenciar subchaves. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento. |
| Valor do tipo de evento, 24                                                             | Enumera as chaves do Registro abertas no início da sessão. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento.                                           |
| Valor do tipo de evento, 25                                                             | Enumera as chaves do Registro abertas no final da sessão. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento.                                                  |
| Valor do tipo de evento, 26                                                             | A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento.                                                                                                              |
| Valor do tipo de evento, 27                                                             | Abrir evento de chave. A classe MOF [**do registro \_ TypeGroup1**](registry-typegroup1.md) define os dados do evento para esse evento.                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**TypeGroup1 do registro \_**](registry-typegroup1.md)
</dt> <dt>

[**V0 do registro \_**](registry-v0.md)
</dt> <dt>

[**Registro \_ v1**](registry-v1.md)
</dt> </dl>

 

 
