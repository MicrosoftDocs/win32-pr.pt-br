---
title: HTTP_LOGGING_FLAG_ constantes (Http.h)
description: Defina as opções para configurar o registro em log na API do Servidor HTTP.
ms.assetid: b6afef7a-5426-4ccd-9785-169e83812c07
topic_type:
- apiref
api_name:
- HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER
- HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION
- HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY
- HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae84697d84295d137f929bcf0d65c2e49fc6754aa7c1110d3b341bb471cbcb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981436"
---
# <a name="http_logging_flag_-constants"></a>Constantes \_ DE SINALIZADOR DE LOG \_ HTTP \_

As **constantes \_ DO SINALIZADOR DE \_ LOG HTTP \_** definem as opções para configurar o registro em log na API do Servidor HTTP.

Essas constantes são usadas na estrutura [**HTTP \_ LOGGING \_ INFO.**](/windows/desktop/api/Http/ns-http-http_logging_info)

<dl> <dt>

<span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**ROLLOVER \_ DE HORA LOCAL DO SINALIZADOR DE \_ \_ \_ LOG \_ HTTP**
</dt> <dd> <dl> <dt>



A sobrepondo do arquivo de log é baseada na hora local. Por padrão, as sobrevassões de arquivo de log se baseiam no UTC (tempo universal coordenado).


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**HTTP \_ SINALIZADOR DE \_ LOG \_ USAR \_ CONVERSÃO UTF8 \_**
</dt> <dd> <dl> <dt>



Os campos unicode são convertidos em multibytes UTF8 ao escrever nos arquivos de log. Por padrão, os arquivos de log são gravados com a conversão de página de código local.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**SOMENTE \_ ERROS DE LOG DO SINALIZADOR \_ \_ DE LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Os arquivos de log incluem apenas informações de erro. Por padrão, as respostas de erro e de êxito são registradas. Se nem OS ERROS DE LOG DO **\_ SINALIZADOR DE \_ \_ LOG \_ \_ HTTP** SOMENTE ou o LOG DO SINALIZADOR DE LOG HTTP SOMENTE ÊXITO for definido, as informações de erro e de êxito são registradas. **\_ \_ \_ \_ \_**

Esse sinalizador não poderá ser definido se o **sinalizador LOG LOG SUCCESS \_ \_ \_ \_ \_ ONLY** HTTP também estiver definido. Esses dois sinalizadores são mutuamente exclusivos.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**HTTP \_ LOG LOG \_ FLAG \_ LOG SUCCESS \_ \_ ONLY**
</dt> <dd> <dl> <dt>



Os arquivos de log incluem apenas informações de êxito. Por padrão, os erros e as transações de êxito são registrados. Se nem OS ERROS DE LOG DO **\_ SINALIZADOR DE \_ \_ LOG \_ \_ HTTP** SOMENTE ou o LOG DO SINALIZADOR DE LOG HTTP SOMENTE ÊXITO for definido, as informações de erro e de êxito são registradas. **\_ \_ \_ \_ \_**

Esse sinalizador não poderá ser definido se o sinalizador LOG DE ERROS SOMENTE DO SINALIZADOR DE **\_ \_ \_ LOG \_ \_ HTTP** também estiver definido. Esses dois sinalizadores são mutuamente exclusivos.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Http.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes da API do Servidor HTTP versão 2.0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**INFORMAÇÕES DE \_ LOG \_ HTTP**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





