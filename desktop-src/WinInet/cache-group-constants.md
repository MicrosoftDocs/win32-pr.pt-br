---
title: Constantes do grupo de cache (Wininet. h)
description: A lista a seguir contém as constantes usadas pelas funções do grupo de cache.
ms.assetid: 9ca2069e-497d-4747-acf4-d5b8020b8ab7
topic_type:
- apiref
api_name:
- CACHEGROUP_ATTRIBUTE_BASIC
- CACHEGROUP_ATTRIBUTE_FLAG
- CACHEGROUP_ATTRIBUTE_GET_ALL
- CACHEGROUP_ATTRIBUTE_GROUPNAME
- CACHEGROUP_ATTRIBUTE_QUOTA
- CACHEGROUP_ATTRIBUTE_STORAGE
- CACHEGROUP_ATTRIBUTE_TYPE
- CACHEGROUP_FLAG_FLUSHURL_ONDELETE
- CACHEGROUP_FLAG_GIDONLY
- CACHEGROUP_FLAG_NONPURGEABLE
- CACHEGROUP_READWRITE_MASK
- CACHEGROUP_SEARCH_ALL
- CACHEGROUP_SEARCH_BYURL
- CACHEGROUP_TYPE_INVALID
- GROUP_OWNER_STORAGE_SIZE
- GROUPNAME_MAX_LENGTH
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb79ae76d743ff4633f6d7f359f96906d2f60cc64c2c35ab2544ae80918721a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955616"
---
# <a name="cache-group-constants"></a>Constantes do grupo de cache

A lista a seguir contém as constantes usadas pelas funções do grupo de cache.

<dl> <dt>

<span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**atributo do FileCache \_ \_ básico**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Recupera os atributos de cota, tipo e sinalizadores de disco do grupo de cache. Isso é usado pela função [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**sinalizador de atributo do FileCache \_ \_**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Define ou recupera os sinalizadores associados ao grupo de cache. Isso é usado pelas funções [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**\_ \_ obter \_ todos os atributos do FileCache**
</dt> <dd> <dl> <dt>

0xffffffff
</dt> <dt>



Recupera todos os atributos do grupo de cache. Isso é usado pela função [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**\_atributo GroupName do FILEcache \_**
</dt> <dd> <dl> <dt>

0x000000010
</dt> <dt>



Define ou recupera o nome do grupo de cache. Isso é usado pelas funções [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**cota de atributo do FileCache \_ \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Define ou recupera a cota de disco associada ao grupo de cache. Isso é usado pelas funções [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**armazenamento de atributos do FileCache \_ \_**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Define ou recupera o armazenamento de proprietário do grupo associado ao grupo de cache. Isso é usado pelas funções [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**tipo de \_ atributo de cache \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Define ou recupera o tipo de grupo de cache. Isso é usado pelas funções [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**sinalizador de \_ cache \_ FLUSHURL \_ OnDelete**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Indica que todas as entradas de cache associadas ao grupo de cache devem ser excluídas, a menos que a entrada pertença a outro grupo de cache.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**sinalizador de \_ GIDONLY de cache \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Indica que a função deve criar apenas um GROUPid exclusivo para o grupo de cache e não criar o grupo real.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**sinalizador de FileCache não \_ \_ eliminável**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indica que o grupo de cache não pode ser limpo.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**máscara ReadWrite do FileCache \_ \_**
</dt> <dd> <dl> <dt>

0x0000003c
</dt> <dt>



Define o tipo, a cota de disco, o nome do grupo e os atributos de armazenamento do proprietário do grupo de cache. Isso é usado pela função [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**\_Pesquisar tudo no FILEcache \_**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Indica que todos os grupos de cache no sistema do usuário devem ser enumerados.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**BYURL de pesquisa do FileCache \_ \_**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Não implementado atualmente.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**tipo de FileCache \_ \_ inválido**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indica que o tipo de grupo de cache é inválido.


</dt> </dl> </dd> <dt>

<span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**\_tamanho do \_ armazenamento do proprietário do grupo \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Comprimento da matriz de armazenamento do proprietário do grupo.


</dt> </dl> </dd> <dt>

<span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**\_comprimento máximo de GroupName \_**
</dt> <dd> <dl> <dt>

0x00000078
</dt> <dt>



Número máximo de caracteres permitidos para um nome de grupo de cache.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. para implementações de servidor ou serviços, use [o Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>WinInet. h</dt> </dl> |



 

