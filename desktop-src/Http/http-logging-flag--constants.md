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
# <a name="http_logging_flag_-constants"></a><span data-ttu-id="6a4e6-103">\_Constantes de \_ sinalizador de log http \_</span><span class="sxs-lookup"><span data-stu-id="6a4e6-103">HTTP\_LOGGING\_FLAG\_ Constants</span></span>

<span data-ttu-id="6a4e6-104">As constantes do **\_ \_ sinalizador \_ de log http** definem as opções para configurar o log na API do servidor http.</span><span class="sxs-lookup"><span data-stu-id="6a4e6-104">The **HTTP\_LOGGING\_FLAG\_** constants define the options to configure logging on the HTTP Server API.</span></span>

<span data-ttu-id="6a4e6-105">Essas constantes são usadas na estrutura [**de \_ \_ informações de log http**](/windows/desktop/api/Http/ns-http-http_logging_info) .</span><span class="sxs-lookup"><span data-stu-id="6a4e6-105">These constants are used in the [**HTTP\_LOGGING\_INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="6a4e6-106"><span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**\_substituição do \_ \_ horário local \_ do sinalizador de log http \_**</span><span class="sxs-lookup"><span data-stu-id="6a4e6-106"><span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**HTTP\_LOGGING\_FLAG\_LOCAL\_TIME\_ROLLOVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a4e6-107">A substituição do arquivo de log é baseada na hora local.</span><span class="sxs-lookup"><span data-stu-id="6a4e6-107">The log file rollover is based on local time.</span></span> <span data-ttu-id="6a4e6-108">Por padrão, as sobreposições de arquivo de log baseiam-se no tempo universal coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="6a4e6-108">By default, log file rollovers is based on coordinated universal time (UTC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a4e6-109"><span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**Http \_ Sinalizador de registro em log \_ \_ usar \_ \_ conversão UTF8**</span><span class="sxs-lookup"><span data-stu-id="6a4e6-109"><span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span> **HTTP\_LOGGING\_FLAG\_USE\_UTF8\_CONVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a4e6-110">Os campos Unicode são convertidos em caracteres UTF-bytes ao gravar nos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="6a4e6-110">The unicode fields are converted to UTF8 multibytes when writting to the log files.</span></span> <span data-ttu-id="6a4e6-111">Por padrão, os arquivos de log são gravados com a conversão da página de código local.</span><span class="sxs-lookup"><span data-stu-id="6a4e6-111">By default, the log files are written with the local code page conversion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a4e6-112"><span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**\_ \_ \_ somente erros de log de sinalizador \_ de log http \_**</span><span class="sxs-lookup"><span data-stu-id="6a4e6-112"><span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a4e6-113">Os arquivos de log incluem apenas informações de erro.</span><span class="sxs-lookup"><span data-stu-id="6a4e6-113">The log files include error information only.</span></span> <span data-ttu-id="6a4e6-114">Por padrão, as respostas de erro e êxito são registradas.</span><span class="sxs-lookup"><span data-stu-id="6a4e6-114">By default, both error and success responses are logged.</span></span> <span data-ttu-id="6a4e6-115">Se o sinalizador de log http não tiver **\_ \_ \_ \_ \_ somente erros de log** ou o log de sinalizador de log **http \_ \_ \_ \_ \_ somente com êxito** for definido, as informações de erro e êxito serão registradas.</span><span class="sxs-lookup"><span data-stu-id="6a4e6-115">If neither the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** or the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** is set, both error and success information is logged.</span></span>

<span data-ttu-id="6a4e6-116">Esse sinalizador não pode ser definido se o sinalizador log de sinalizador de log **http \_ \_ \_ \_ \_ somente com êxito** também é definido.</span><span class="sxs-lookup"><span data-stu-id="6a4e6-116">This flag cannot be set if the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** flag is also set.</span></span> <span data-ttu-id="6a4e6-117">Esses dois sinalizadores são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="6a4e6-117">These two flags are mutually exclusive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a4e6-118"><span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**Http \_ log de sinalizador de log \_ \_ \_ \_ somente com êxito**</span><span class="sxs-lookup"><span data-stu-id="6a4e6-118"><span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span> **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a4e6-119">Os arquivos de log incluem apenas informações de êxito.</span><span class="sxs-lookup"><span data-stu-id="6a4e6-119">The log files include success information only.</span></span> <span data-ttu-id="6a4e6-120">Por padrão, os erros e as transações de êxito são registrados.</span><span class="sxs-lookup"><span data-stu-id="6a4e6-120">By default, both errors and success transactions are logged.</span></span> <span data-ttu-id="6a4e6-121">Se o sinalizador de log http não tiver **\_ \_ \_ \_ \_ somente erros de log** ou o log de sinalizador de log **http \_ \_ \_ \_ \_ somente com êxito** for definido, as informações de erro e êxito serão registradas.</span><span class="sxs-lookup"><span data-stu-id="6a4e6-121">If neither the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** or the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** is set, both error and success information is logged.</span></span>

<span data-ttu-id="6a4e6-122">Esse sinalizador não pode ser definido se o sinalizador de log de sinalizador de log **http \_ \_ \_ \_ \_ somente** sinalizar erros também estiver definido.</span><span class="sxs-lookup"><span data-stu-id="6a4e6-122">This flag cannot be set if the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** flag is also set.</span></span> <span data-ttu-id="6a4e6-123">Esses dois sinalizadores são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="6a4e6-123">These two flags are mutually exclusive.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a4e6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a4e6-124">Requirements</span></span>



| <span data-ttu-id="6a4e6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a4e6-125">Requirement</span></span> | <span data-ttu-id="6a4e6-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6a4e6-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6a4e6-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a4e6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6a4e6-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a4e6-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6a4e6-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a4e6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6a4e6-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6a4e6-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6a4e6-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a4e6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a4e6-132"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a4e6-132"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a4e6-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a4e6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a4e6-134">Constantes da API do servidor HTTP versão 2,0</span><span class="sxs-lookup"><span data-stu-id="6a4e6-134">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="6a4e6-135">**\_informações de log http \_**</span><span class="sxs-lookup"><span data-stu-id="6a4e6-135">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[<span data-ttu-id="6a4e6-136">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="6a4e6-136">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="6a4e6-137">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="6a4e6-137">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="6a4e6-138">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="6a4e6-138">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="6a4e6-139">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="6a4e6-139">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





