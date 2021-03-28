---
description: Essa classe é a classe pai para eventos de imagem. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: a719a34c-7e32-4758-9031-6ca2b2873e3e
title: Classe Image
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- NA
api_location: ''
ms.openlocfilehash: 47280a81b882f91ad71c6cd91004d1c0885afddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967980"
---
# <a name="image-class"></a>Classe Image

Essa classe é a classe pai para eventos de imagem.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{2cb15d1d-5fc1-11d2-abe1-00a0c911f518}"), EventVersion(2)]
class Image : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A classe **Image** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar eventos de imagem em uma sessão de log de kernel NT, especifique o sinalizador de carregamento de imagem do sinalizador de rastreamento de eventos no membro **EnableFlags** da estrutura [](/windows/win32/api/evntrace/nf-evntrace-starttracea) de [**Propriedades de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função StartTrace. **\_ \_ \_ \_**

Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de carregamento de imagem chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**ImageLoadGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* . Use os seguintes tipos de evento para identificar eventos de carga de imagem ao consumir eventos.



| Tipo de evento                                                          | Descrição                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ de \_ \_ Carga de tipo de rastreamento**(o valor do tipo de evento é 10)<br/>     | Evento de carregamento de imagem. Gerado quando um arquivo DLL ou executável é carregado. O provedor gera apenas um evento pela primeira vez que uma determinada DLL é carregada. A classe MOF de [**\_ carregamento de imagem**](image-load.md) define os dados do evento para esse evento.      |
| **Evento \_ de Tipo de rastreamento \_ \_ end**(o valor do tipo de evento é 2)<br/>       | Evento de descarregamento de imagem. Gerado quando um arquivo DLL ou executável é descarregado. O provedor gera apenas um evento para a última vez em que uma determinada DLL é descarregada. A classe MOF de [**\_ carregamento de imagem**](image-load.md) define os dados do evento para esse evento. |
| **Evento \_ de Tipo de rastreamento \_ \_ DC \_ Iniciar**(o valor do tipo de evento é 3)<br/> | Evento de início de coleta de dados. Enumera todas as imagens carregadas no início do rastreamento. A classe MOF de [**\_ carregamento de imagem**](image-load.md) define os dados do evento para esse evento.                                                                  |
| **Evento \_ de Tipo de rastreamento \_ \_ DC \_ end**(o valor do tipo de evento é 4)<br/>   | Evento de término da coleta de dados. Enumera todas as imagens carregadas no final do rastreamento. A classe MOF de [**\_ carregamento de imagem**](image-load.md) define os dados do evento para esse evento.                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Carregamento de imagem \_**](image-load.md)
</dt> <dt>

[**V0 de imagem \_**](image-v0.md)
</dt> <dt>

[**Imagem \_ v1**](image-v1.md)
</dt> </dl>

 

 
