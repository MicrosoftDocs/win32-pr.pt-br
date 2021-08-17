---
description: Usado para representar entradas de registro que controlam o cache de chave privada por CSPs baseados em software da Microsoft.
ms.assetid: 67909072-72fe-4777-ae52-a7b9047c9dd5
title: chaves privadas Caching constantes (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d4caf6a3973a5113e03cbe24882241609ff83b8be65a20492f8f967abb734f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978557"
---
# <a name="private-key-caching-constants"></a>constantes de Caching de chave privada

As constantes a seguir são usadas para representar entradas de registro que controlam o cache de [*chave privada*](../secgloss/p-gly.md) por CSPs baseados em software da Microsoft.



| Constante/valor                                                                                                                                                                                                                                                                                                                                                                                    | Descrição                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| <span id="szKEY_CRYPTOAPI_PRIVATE_KEY_OPTIONS"></span><span id="szkey_cryptoapi_private_key_options"></span><span id="SZKEY_CRYPTOAPI_PRIVATE_KEY_OPTIONS"></span><dl> <dt>**szKEY \_ \_Opções de \_ chave \_ privada CRYPTOAPI**</dt> <dt>"políticas de software \\ \\ \\ \\ criptografia da Microsoft \\ \\ "</dt> </dl> | O caminho, na raiz **do \_ \_ computador local hKey** , das entradas do registro de cache de chave privada.<br/> |



As constantes a seguir são usadas para identificar valores de registro que controlam o cache de chave privada globalmente para um processo específico por CSPs baseados em software da Microsoft.



| Constante/valor                                                                                                                                                                                                                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="szPRIV_KEY_CACHE_MAX_ITEMS"></span><span id="szpriv_key_cache_max_items"></span><span id="SZPRIV_KEY_CACHE_MAX_ITEMS"></span><dl> <dt>**szPRIV \_ \_Máximo de \_ \_ itens do cache de chaves**</dt> <dt>"PrivKeyCacheMaxItems"</dt> </dl>                                                                  | Um valor **reg \_ DWORD** na chave de registro de **\_ \_ \_ \_ Opções de chave privada szKEY CRYPTOAPI** que especifica o número máximo de chaves privadas que podem ser armazenadas em cache ao mesmo tempo para um único processo. Essa verificação é executada sempre que uma chave privada armazenada é lida. Se o número máximo for excedido, a chave menos usada recentemente será removida do cache.<br/> Se esse valor for zero, nenhuma chave será armazenada em cache. Se esse valor não estiver presente, o **valor \_ \_ \_ padrão máximo de \_ itens \_ do cache de chave cPRIV** será usado como o padrão.<br/> Se uma chave privada que é excluída do cache for atualmente referenciada em um contexto aberto, a chave será lida do armazenamento na próxima vez que for feita uma tentativa de usar a chave.<br/> **Windows Server 2003 e Windows XP com SP1 e versões anteriores:** Não há suporte para esse valor de registro.<br/>                                  |
| <span id="cPRIV_KEY_CACHE_MAX_ITEMS_DEFAULT"></span><span id="cpriv_key_cache_max_items_default"></span><span id="CPRIV_KEY_CACHE_MAX_ITEMS_DEFAULT"></span><dl> <dt>**cPRIV \_ Máximo de itens do cache de chaves \_ \_ \_ \_ padrão**</dt> <dt>20</dt> </dl>                                                         | O valor padrão da entrada de registro **\_ máximo de \_ \_ \_ itens do cache de chave szPRIV** se nenhum valor for especificado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="szPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS"></span><span id="szpriv_key_cache_purge_interval_seconds"></span><span id="SZPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS"></span><dl> <dt>**szPRIV \_ \_Segundos do \_ \_ intervalo \_ de limpeza do cache de chave**</dt> <dt>"PrivKeyCachePurgeIntervalSeconds"</dt> </dl> | Um valor **reg \_ DWORD** na chave de registro de **\_ \_ \_ \_ Opções de chave privada szKEY CRYPTOAPI** que especifica a idade máxima, em segundos, de qualquer chave privada armazenada em cache. Essa verificação é executada sempre que uma chave privada armazenada é usada ou lida. Se esse período de tempo tiver decorrido desde a última limpeza, todas as chaves em cache que não foram referenciadas desde a última limpeza serão removidas do cache.<br/> Se esse valor não estiver presente, o **valor \_ \_ padrão de \_ \_ segundos do \_ \_ intervalo de limpeza do cache de chave cPRIV** será usado como o padrão.<br/> Se uma chave privada que é limpa do cache for atualmente referenciada em um contexto aberto, a chave será lida do armazenamento na próxima vez que for feita uma tentativa de usar a chave.<br/> **Windows Server 2003 e Windows XP com SP1 e versões anteriores:** Não há suporte para esse valor de registro.<br/> |
| <span id="cPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS_DEFAULT"></span><span id="cpriv_key_cache_purge_interval_seconds_default"></span><span id="CPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS_DEFAULT"></span><dl> <dt>**cPRIV \_ Intervalo de limpeza de cache de chave- \_ \_ \_ \_ segundos \_ padrão**</dt> <dt>86400</dt> </dl> | O valor padrão da entrada de registro de **segundos do intervalo de limpeza do \_ cache de chave \_ \_ \_ \_ szPRIV** se nenhum valor for especificado. Esse valor é equivalente a um dia.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



As constantes a seguir são usadas para identificar valores de registro que controlam o cache de chave privada para uma única instância do CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) baseada em software da Microsoft.



| Constante/valor                                                                                                                                                                                                                                                                                          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>"AllowCachePW"</dt> </dl>                                                                                                                                                         | Um valor **reg \_ DWORD** em **HKEY \_ local \_ Machine \\ software \\ Policies The \\ Microsoft \\ Cryptography \\ Protect** registry key, que especifica se o cache de senha está habilitado para chaves protegidas por senha nos CSPs baseados em software da Microsoft. Se esse valor for 0, o cache de senha será disabeld e o usuário será solicitado a fornecer a senha sempre que uma chave protegida por senha for usada. Qualquer outro valor, ou a ausência desse valor, indica que a senha será armazenada em cache. Nesse cenário, o usuário é solicitado apenas uma vez por processo para cada chave. <br/> |
| <span id="szKEY_CACHE_ENABLED"></span><span id="szkey_cache_enabled"></span><span id="SZKEY_CACHE_ENABLED"></span><dl> <dt>**szKEY \_ CACHE \_ habilitado**</dt> <dt>"CachePrivateKeys"</dt> </dl>          | Um valor **reg \_ DWORD** na chave de registro de **\_ \_ \_ \_ Opções de chave privada szKEY CRYPTOAPI** que especifica se o cache de chave privada está habilitado. Se esse valor for 1, o cache de chave privada será habilitado. Qualquer outro valor, ou a ausência desse valor, indica que o cache de chave privada está desabilitado.<br/> **Windows vista com SP1, Windows Vista e Windows XP:** Não há suporte para esse valor de registro.<br/>                                                                                                                                                        |
| <span id="szKEY_CACHE_SECONDS"></span><span id="szkey_cache_seconds"></span><span id="SZKEY_CACHE_SECONDS"></span><dl> <dt>**szKEY \_ \_Segundos de cache**</dt> <dt>"PrivateKeyLifetimeSeconds"</dt> </dl> | Um valor **reg \_ DWORD** na chave de registro de **\_ \_ \_ \_ Opções de chave privada szKEY CRYPTOAPI** que especifica a idade máxima, em segundos, de qualquer chave privada armazenada em cache.<br/> **Windows XP:** Não há suporte para esse valor de registro.<br/>                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Comentários

As diferenças entre os **\_ \_ segundos de cache szKEY** e os valores de intervalo de **\_ limpeza de cache de chave \_ \_ \_ \_ szPRIV** são os seguintes:

 **\_segundos de cache szKEY \_**  

-   Esse valor se aplica somente a um CSP específico. Depois que o CSP é liberado, o cache do CSP é liberado também.  
-   Esse valor só é aplicado quando é feita uma tentativa de usar uma chave privada específica com um identificador de contexto específico.  

**\_segundos do \_ intervalo de limpeza do cache de chave szPRIV \_ \_ \_**  

-   Esse valor se aplica a todos os CSPs em um processo. Mesmo que o CSP seja liberado, esse cache não será liberado.  
-   Esse valor se aplica sempre que qualquer chave privada armazenada é usada ou lida do armazenamento em um único processo.  



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
