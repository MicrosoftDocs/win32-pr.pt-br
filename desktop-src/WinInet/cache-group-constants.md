---
title: Constantes do Grupo de Cache (Wininet.h)
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
# <a name="cache-group-constants"></a>Constantes do Grupo de Cache

A lista a seguir contém as constantes usadas pelas funções do grupo de cache.

<dl> <dt>

<span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**ATRIBUTO CACHEGROUP \_ \_ BÁSICO**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Recupera os sinalizadores, o tipo e os atributos de cota de disco do grupo de cache. Isso é usado pela [**função GetUrlCacheGroupAttribute.**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**SINALIZADOR DE ATRIBUTO \_ CACHEGROUP \_**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Define ou recupera os sinalizadores associados ao grupo de cache. Isso é usado pelas [**funções GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) [**e SetUrlCacheGroupAttribute.**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**ATRIBUTO CACHEGROUP \_ \_ GET \_ ALL**
</dt> <dd> <dl> <dt>

0xffffffff
</dt> <dt>



Recupera todos os atributos do grupo de cache. Isso é usado pela [**função GetUrlCacheGroupAttribute.**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**CACHEGROUP \_ ATTRIBUTE \_ GROUPNAME**
</dt> <dd> <dl> <dt>

0x000000010
</dt> <dt>



Define ou recupera o nome do grupo de cache. Isso é usado pelas [**funções GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) [**e SetUrlCacheGroupAttribute.**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**COTA DE ATRIBUTO \_ CACHEGROUP \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Define ou recupera a cota de disco associada ao grupo de cache. Isso é usado pelas [**funções GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) [**e SetUrlCacheGroupAttribute.**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**ARMAZENAMENTO DE ATRIBUTOS \_ DO GRUPO DE \_ CACHE**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Define ou recupera o armazenamento do proprietário do grupo associado ao grupo de cache. Isso é usado pelas [**funções GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) [**e SetUrlCacheGroupAttribute.**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**TIPO DE ATRIBUTO CACHEGROUP \_ \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Define ou recupera o tipo de grupo de cache. Isso é usado pelas [**funções GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) [**e SetUrlCacheGroupAttribute.**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**SINALIZADOR CACHEGROUP \_ \_ FLUSHURL \_ ONDELETE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Indica que todas as entradas de cache associadas ao grupo de cache devem ser excluídas, a menos que a entrada pertentrada a outro grupo de cache.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**SINALIZADOR CACHEGROUP \_ \_ GIDONLY**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Indica que a função deve criar apenas um GROUPID exclusivo para o grupo de cache e não criar o grupo real.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**SINALIZADOR CACHEGROUP \_ \_ NÃO ACESSÍVEL**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indica que o grupo de cache não pode ser limpo.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**CACHEGROUP \_ READWRITE \_ MASK**
</dt> <dd> <dl> <dt>

0x0000003c
</dt> <dt>



Define o tipo, a cota de disco, o nome do grupo e os atributos de armazenamento do proprietário do grupo de cache. Isso é usado pela [**função SetUrlCacheGroupAttribute.**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**PESQUISA DE GRUPO \_ DE CACHE \_ TUDO**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Indica que todos os grupos de cache no sistema do usuário devem ser enumerados.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**CACHEGROUP \_ SEARCH \_ BYURL**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Não implementado atualmente.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**TIPO CACHEGROUP \_ \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indica que o tipo de grupo de cache é inválido.


</dt> </dl> </dd> <dt>

<span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**TAMANHO DE \_ ARMAZENAMENTO DO PROPRIETÁRIO DO \_ \_ GRUPO**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Comprimento da matriz de armazenamento do proprietário do grupo.


</dt> </dl> </dd> <dt>

<span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**GROUPNAME \_ MAX \_ LENGTH**
</dt> <dd> <dl> <dt>

0x00000078
</dt> <dt>



Número máximo de caracteres permitidos para um nome de grupo de cache.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> O WinINet não dá suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o WinHTTP (Microsoft Windows HTTP Services).](/windows/desktop/WinHttp/winhttp-start-page)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Wininet.h</dt> </dl> |



 

