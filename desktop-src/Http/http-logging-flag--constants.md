---
title: Constantes de HTTP_LOGGING_FLAG_ (http. h)
description: Defina as opções para configurar o log na API do servidor HTTP.
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
ms.openlocfilehash: c501fc3ab646ab65fa039a5ff5e7d2dc0578002a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644900"
---
# <a name="http_logging_flag_-constants"></a>\_Constantes de \_ sinalizador de log http \_

As constantes do **\_ \_ sinalizador \_ de log http** definem as opções para configurar o log na API do servidor http.

Essas constantes são usadas na estrutura [**de \_ \_ informações de log http**](/windows/desktop/api/Http/ns-http-http_logging_info) .

<dl> <dt>

<span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**\_substituição do \_ \_ horário local \_ do sinalizador de log http \_**
</dt> <dd> <dl> <dt>



A substituição do arquivo de log é baseada na hora local. Por padrão, as sobreposições de arquivo de log baseiam-se no tempo universal coordenado (UTC).


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**Http \_ Sinalizador de registro em log \_ \_ usar \_ \_ conversão UTF8**
</dt> <dd> <dl> <dt>



Os campos Unicode são convertidos em caracteres UTF-bytes ao gravar nos arquivos de log. Por padrão, os arquivos de log são gravados com a conversão da página de código local.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**\_ \_ \_ somente erros de log de sinalizador \_ de log http \_**
</dt> <dd> <dl> <dt>



Os arquivos de log incluem apenas informações de erro. Por padrão, as respostas de erro e êxito são registradas. Se o sinalizador de log http não tiver **\_ \_ \_ \_ \_ somente erros de log** ou o log de sinalizador de log **http \_ \_ \_ \_ \_ somente com êxito** for definido, as informações de erro e êxito serão registradas.

Esse sinalizador não pode ser definido se o sinalizador log de sinalizador de log **http \_ \_ \_ \_ \_ somente com êxito** também é definido. Esses dois sinalizadores são mutuamente exclusivos.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**Http \_ log de sinalizador de log \_ \_ \_ \_ somente com êxito**
</dt> <dd> <dl> <dt>



Os arquivos de log incluem apenas informações de êxito. Por padrão, os erros e as transações de êxito são registrados. Se o sinalizador de log http não tiver **\_ \_ \_ \_ \_ somente erros de log** ou o log de sinalizador de log **http \_ \_ \_ \_ \_ somente com êxito** for definido, as informações de erro e êxito serão registradas.

Esse sinalizador não pode ser definido se o sinalizador de log de sinalizador de log **http \_ \_ \_ \_ \_ somente** sinalizar erros também estiver definido. Esses dois sinalizadores são mutuamente exclusivos.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Constantes da API do servidor HTTP versão 2,0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_informações de log http \_**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





