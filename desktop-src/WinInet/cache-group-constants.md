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
ms.openlocfilehash: 3a08efa37ad78fa3351d12fa43491c7b62ee64af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780654"
---
# <a name="cache-group-constants"></a><span data-ttu-id="42daf-103">Constantes do grupo de cache</span><span class="sxs-lookup"><span data-stu-id="42daf-103">Cache Group Constants</span></span>

<span data-ttu-id="42daf-104">A lista a seguir contém as constantes usadas pelas funções do grupo de cache.</span><span class="sxs-lookup"><span data-stu-id="42daf-104">The following list contains the constants used by the cache group functions.</span></span>

<dl> <dt>

<span data-ttu-id="42daf-105"><span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**atributo do FileCache \_ \_ básico**</span><span class="sxs-lookup"><span data-stu-id="42daf-105"><span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**CACHEGROUP\_ATTRIBUTE\_BASIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42daf-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="42daf-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="42daf-107">Recupera os atributos de cota, tipo e sinalizadores de disco do grupo de cache.</span><span class="sxs-lookup"><span data-stu-id="42daf-107">Retrieves the flags, type, and disk quota attributes of the cache group.</span></span> <span data-ttu-id="42daf-108">Isso é usado pela função [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="42daf-108">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42daf-109"><span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**sinalizador de atributo do FileCache \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42daf-109"><span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**CACHEGROUP\_ATTRIBUTE\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42daf-110">0x00000002</span><span class="sxs-lookup"><span data-stu-id="42daf-110">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="42daf-111">Define ou recupera os sinalizadores associados ao grupo de cache.</span><span class="sxs-lookup"><span data-stu-id="42daf-111">Sets or retrieves the flags associated with the cache group.</span></span> <span data-ttu-id="42daf-112">Isso é usado pelas funções [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="42daf-112">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42daf-113"><span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**\_ \_ obter \_ todos os atributos do FileCache**</span><span class="sxs-lookup"><span data-stu-id="42daf-113"><span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**CACHEGROUP\_ATTRIBUTE\_GET\_ALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42daf-114">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="42daf-114">0xffffffff</span></span>
</dt> <dt>



<span data-ttu-id="42daf-115">Recupera todos os atributos do grupo de cache.</span><span class="sxs-lookup"><span data-stu-id="42daf-115">Retrieves all the attributes of the cache group.</span></span> <span data-ttu-id="42daf-116">Isso é usado pela função [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="42daf-116">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42daf-117"><span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**\_atributo GroupName do FILEcache \_**</span><span class="sxs-lookup"><span data-stu-id="42daf-117"><span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**CACHEGROUP\_ATTRIBUTE\_GROUPNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42daf-118">0x000000010</span><span class="sxs-lookup"><span data-stu-id="42daf-118">0x000000010</span></span>
</dt> <dt>



<span data-ttu-id="42daf-119">Define ou recupera o nome do grupo de cache.</span><span class="sxs-lookup"><span data-stu-id="42daf-119">Sets or retrieves the group name of the cache group.</span></span> <span data-ttu-id="42daf-120">Isso é usado pelas funções [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="42daf-120">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42daf-121"><span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**cota de atributo do FileCache \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42daf-121"><span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**CACHEGROUP\_ATTRIBUTE\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42daf-122">0x00000008</span><span class="sxs-lookup"><span data-stu-id="42daf-122">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="42daf-123">Define ou recupera a cota de disco associada ao grupo de cache.</span><span class="sxs-lookup"><span data-stu-id="42daf-123">Sets or retrieves the disk quota associated with the cache group.</span></span> <span data-ttu-id="42daf-124">Isso é usado pelas funções [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="42daf-124">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42daf-125"><span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**armazenamento de atributos do FileCache \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42daf-125"><span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**CACHEGROUP\_ATTRIBUTE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42daf-126">0x00000020</span><span class="sxs-lookup"><span data-stu-id="42daf-126">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="42daf-127">Define ou recupera o armazenamento de proprietário do grupo associado ao grupo de cache.</span><span class="sxs-lookup"><span data-stu-id="42daf-127">Sets or retrieves the group owner storage associated with the cache group.</span></span> <span data-ttu-id="42daf-128">Isso é usado pelas funções [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="42daf-128">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42daf-129"><span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**tipo de \_ atributo de cache \_**</span><span class="sxs-lookup"><span data-stu-id="42daf-129"><span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**CACHEGROUP\_ATTRIBUTE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42daf-130">0x00000004</span><span class="sxs-lookup"><span data-stu-id="42daf-130">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="42daf-131">Define ou recupera o tipo de grupo de cache.</span><span class="sxs-lookup"><span data-stu-id="42daf-131">Sets or retrieves the cache group type.</span></span> <span data-ttu-id="42daf-132">Isso é usado pelas funções [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="42daf-132">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42daf-133"><span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**sinalizador de \_ cache \_ FLUSHURL \_ OnDelete**</span><span class="sxs-lookup"><span data-stu-id="42daf-133"><span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**CACHEGROUP\_FLAG\_FLUSHURL\_ONDELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42daf-134">0x00000002</span><span class="sxs-lookup"><span data-stu-id="42daf-134">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="42daf-135">Indica que todas as entradas de cache associadas ao grupo de cache devem ser excluídas, a menos que a entrada pertença a outro grupo de cache.</span><span class="sxs-lookup"><span data-stu-id="42daf-135">Indicates that all the cache entries associated with the cache group should be deleted, unless the entry belongs to another cache group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42daf-136"><span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**sinalizador de \_ GIDONLY de cache \_**</span><span class="sxs-lookup"><span data-stu-id="42daf-136"><span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**CACHEGROUP\_FLAG\_GIDONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42daf-137">0x00000004</span><span class="sxs-lookup"><span data-stu-id="42daf-137">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="42daf-138">Indica que a função deve criar apenas um GROUPid exclusivo para o grupo de cache e não criar o grupo real.</span><span class="sxs-lookup"><span data-stu-id="42daf-138">Indicates that the function should only create a unique GROUPID for the cache group and not create the actual group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42daf-139"><span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**sinalizador de FileCache não \_ \_ eliminável**</span><span class="sxs-lookup"><span data-stu-id="42daf-139"><span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**CACHEGROUP\_FLAG\_NONPURGEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42daf-140">0x00000001</span><span class="sxs-lookup"><span data-stu-id="42daf-140">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="42daf-141">Indica que o grupo de cache não pode ser limpo.</span><span class="sxs-lookup"><span data-stu-id="42daf-141">Indicates that the cache group cannot be purged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42daf-142"><span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**máscara ReadWrite do FileCache \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42daf-142"><span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**CACHEGROUP\_READWRITE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42daf-143">0x0000003c</span><span class="sxs-lookup"><span data-stu-id="42daf-143">0x0000003c</span></span>
</dt> <dt>



<span data-ttu-id="42daf-144">Define o tipo, a cota de disco, o nome do grupo e os atributos de armazenamento do proprietário do grupo de cache.</span><span class="sxs-lookup"><span data-stu-id="42daf-144">Sets the type, disk quota, group name, and owner storage attributes of the cache group.</span></span> <span data-ttu-id="42daf-145">Isso é usado pela função [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="42daf-145">This is used by the [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42daf-146"><span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**\_Pesquisar tudo no FILEcache \_**</span><span class="sxs-lookup"><span data-stu-id="42daf-146"><span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**CACHEGROUP\_SEARCH\_ALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42daf-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42daf-147">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="42daf-148">Indica que todos os grupos de cache no sistema do usuário devem ser enumerados.</span><span class="sxs-lookup"><span data-stu-id="42daf-148">Indicates that all of the cache groups in the user's system should be enumerated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42daf-149"><span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**BYURL de pesquisa do FileCache \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42daf-149"><span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**CACHEGROUP\_SEARCH\_BYURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42daf-150">0x00000001</span><span class="sxs-lookup"><span data-stu-id="42daf-150">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="42daf-151">Não implementado atualmente.</span><span class="sxs-lookup"><span data-stu-id="42daf-151">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42daf-152"><span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**tipo de FileCache \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="42daf-152"><span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**CACHEGROUP\_TYPE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42daf-153">0x00000001</span><span class="sxs-lookup"><span data-stu-id="42daf-153">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="42daf-154">Indica que o tipo de grupo de cache é inválido.</span><span class="sxs-lookup"><span data-stu-id="42daf-154">Indicates that the cache group type is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42daf-155"><span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**\_tamanho do \_ armazenamento do proprietário do grupo \_**</span><span class="sxs-lookup"><span data-stu-id="42daf-155"><span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**GROUP\_OWNER\_STORAGE\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42daf-156">0x00000004</span><span class="sxs-lookup"><span data-stu-id="42daf-156">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="42daf-157">Comprimento da matriz de armazenamento do proprietário do grupo.</span><span class="sxs-lookup"><span data-stu-id="42daf-157">Length of the group owner storage array.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42daf-158"><span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**\_comprimento máximo de GroupName \_**</span><span class="sxs-lookup"><span data-stu-id="42daf-158"><span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**GROUPNAME\_MAX\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42daf-159">0x00000078</span><span class="sxs-lookup"><span data-stu-id="42daf-159">0x00000078</span></span>
</dt> <dt>



<span data-ttu-id="42daf-160">Número máximo de caracteres permitidos para um nome de grupo de cache.</span><span class="sxs-lookup"><span data-stu-id="42daf-160">Maximum number of characters allowed for a cache group name.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42daf-161">Comentários</span><span class="sxs-lookup"><span data-stu-id="42daf-161">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="42daf-162">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="42daf-162">WinINet does not support server implementations.</span></span> <span data-ttu-id="42daf-163">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="42daf-163">In addition, it should not be used from a service.</span></span> <span data-ttu-id="42daf-164">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="42daf-164">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="42daf-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42daf-165">Requirements</span></span>



| <span data-ttu-id="42daf-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="42daf-166">Requirement</span></span> | <span data-ttu-id="42daf-167">Valor</span><span class="sxs-lookup"><span data-stu-id="42daf-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="42daf-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42daf-168">Minimum supported client</span></span><br/> | <span data-ttu-id="42daf-169">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="42daf-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="42daf-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42daf-170">Minimum supported server</span></span><br/> | <span data-ttu-id="42daf-171">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="42daf-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="42daf-172">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="42daf-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="42daf-173"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="42daf-173"><dt>Wininet.h</dt></span></span> </dl> |



 

