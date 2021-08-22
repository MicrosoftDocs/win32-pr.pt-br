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
ms.openlocfilehash: a7db8595dd09790d875e502e479d14669a6df90b8de38b71fcf9ed58f2b68b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070106"
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

A **classe Image** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar eventos de imagem em uma sessão de registro em log do Kernel NT, especifique o sinalizador **EVENT \_ TRACE IMAGE \_ \_ \_ LOAD** no membro **EnableFlags** da estrutura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a [**função StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

Os consumidores de rastreamento de eventos podem implementar o processamento especial para eventos de carregamento de imagem chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**ImageLoadGuid**](nt-kernel-logger-constants.md) como o *parâmetro pGuid.* Use os seguintes tipos de evento para identificar eventos de carregamento de imagem ao consumir eventos.



| Tipo de evento                                                          | Descrição                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ LOAD**(o valor do tipo de evento é 10)<br/>     | Evento de carregamento de imagem. Gerado quando uma DLL ou arquivo executável é carregado. O provedor gera apenas um evento pela primeira vez em que uma determinada DLL é carregada. A [**classe MOF \_ de**](image-load.md) Carregamento de Imagem define os dados de evento para esse evento.      |
| **EVENTO \_ TRACE \_ TYPE \_ END**(o valor do tipo de evento é 2)<br/>       | Evento de descarregamento de imagem. Gerado quando uma DLL ou arquivo executável é descarregado. O provedor gera apenas um evento para a última vez que uma determinada DLL é descarregada. A [**classe MOF \_ de**](image-load.md) Carregamento de Imagem define os dados de evento para esse evento. |
| **EVENTO \_ TRACE \_ TYPE \_ DC \_ START**(o valor do tipo de evento é 3)<br/> | Evento de início da coleta de dados. Enumera todas as imagens carregadas no início do rastreamento. A [**classe MOF \_ de**](image-load.md) Carregamento de Imagem define os dados de evento para esse evento.                                                                  |
| **EVENTO \_ TRACE \_ TYPE \_ DC \_ END**(o valor do tipo de evento é 4)<br/>   | Evento final da coleta de dados. Enumera todas as imagens carregadas no final do rastreamento. A [**classe MOF \_ de**](image-load.md) Carregamento de Imagem define os dados de evento para esse evento.                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemTrace do MSNT \_**](msnt-systemtrace.md)
</dt> <dt>

[**Carregamento de \_ imagem**](image-load.md)
</dt> <dt>

[**Imagem \_ V0**](image-v0.md)
</dt> <dt>

[**Imagem \_ V1**](image-v1.md)
</dt> </dl>

 

 
