---
description: Estende as propriedades definidas para as APIs do conjunto de linhas.
ms.assetid: C1A2DF19-C68D-42CC-9CB2-190F22CB4158
title: DBPROPSET_MSIDXS_ROWSETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba37466c52f2fa9f83e3aa439ace03c1fba34f44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798370"
---
# <a name="dbpropset_msidxs_rowsetext"></a><span data-ttu-id="df7cf-103">DBPROPSET \_ MSIDXS \_ ROWSETEXT</span><span class="sxs-lookup"><span data-stu-id="df7cf-103">DBPROPSET\_MSIDXS\_ROWSETEXT</span></span>

<span data-ttu-id="df7cf-104">Estende as propriedades definidas para as APIs do conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="df7cf-104">Extends properties defined for the Rowset APIs.</span></span>

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

<span data-ttu-id="df7cf-105">O \_ conjunto de propriedades DBPROPSET MSIDXS \_ ROWSETEXT contém as seguintes constantes de propriedade:</span><span class="sxs-lookup"><span data-stu-id="df7cf-105">The DBPROPSET\_MSIDXS\_ROWSETEXT property set contains the following property constants:</span></span>

<dl> <dt>

<span data-ttu-id="df7cf-106"><span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP \_ ROWSETQUERYSTATUS</span><span class="sxs-lookup"><span data-stu-id="df7cf-106"><span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP\_ROWSETQUERYSTATUS</span></span>
</dt> <dd>

<span data-ttu-id="df7cf-107">ID da propriedade 2.</span><span class="sxs-lookup"><span data-stu-id="df7cf-107">Property ID 2.</span></span> <span data-ttu-id="df7cf-108">Status da consulta para o conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="df7cf-108">Query status for the rowset.</span></span> <span data-ttu-id="df7cf-109">As \_ \* constantes stat indicam o status de execução e de confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="df7cf-109">The STAT\_\* constants indicate the execution and reliability status.</span></span>

</dd> <dt>

<span data-ttu-id="df7cf-110"><span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>\_cadeia de \_ caracteres de localidade do comando MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="df7cf-110"><span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>MSIDXSPROP\_COMMAND\_LOCALE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="df7cf-111">ID da propriedade 3.</span><span class="sxs-lookup"><span data-stu-id="df7cf-111">Property ID 3.</span></span> <span data-ttu-id="df7cf-112">Cadeia de caracteres de localidade que representa a configuração de idioma e localidade a ser usada para este conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="df7cf-112">Locale string that represents the language and locale setting to use for this rowset.</span></span>

</dd> <dt>

<span data-ttu-id="df7cf-113"><span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>\_restrição de consulta MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="df7cf-113"><span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>MSIDXSPROP\_QUERY\_RESTRICTION</span></span>
</dt> <dd>

<span data-ttu-id="df7cf-114">ID da propriedade 4.</span><span class="sxs-lookup"><span data-stu-id="df7cf-114">Property ID 4.</span></span> <span data-ttu-id="df7cf-115">A cadeia de caracteres de consulta associada a este conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="df7cf-115">The query string associated with this rowset.</span></span>

</dd> <dt>

<span data-ttu-id="df7cf-116"><span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>\_árvore de análise do MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="df7cf-116"><span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>MSIDXSPROP\_PARSE\_TREE</span></span>
</dt> <dd>

<span data-ttu-id="df7cf-117">ID da propriedade 5.</span><span class="sxs-lookup"><span data-stu-id="df7cf-117">Property ID 5.</span></span>

</dd> <dt>

<span data-ttu-id="df7cf-118"><span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>\_classificação máxima de MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="df7cf-118"><span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>MSIDXSPROP\_MAX\_RANK</span></span> 
</dt> <dd>

<span data-ttu-id="df7cf-119">ID da propriedade 6.</span><span class="sxs-lookup"><span data-stu-id="df7cf-119">Property ID 6.</span></span>

</dd> <dt>

<span data-ttu-id="df7cf-120"><span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>resultados de MSIDXSPROP \_ \_ encontrados</span><span class="sxs-lookup"><span data-stu-id="df7cf-120"><span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>MSIDXSPROP\_RESULTS\_FOUND</span></span>
</dt> <dd>

<span data-ttu-id="df7cf-121">ID da propriedade 7.</span><span class="sxs-lookup"><span data-stu-id="df7cf-121">Property ID 7.</span></span>

</dd> <dt>

<span data-ttu-id="df7cf-122"><span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP \_ whereid</span><span class="sxs-lookup"><span data-stu-id="df7cf-122"><span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP\_WHEREID</span></span>
</dt> <dd>

<span data-ttu-id="df7cf-123">ID da propriedade 8.</span><span class="sxs-lookup"><span data-stu-id="df7cf-123">Property ID 8.</span></span>

</dd> <dt>

<span data-ttu-id="df7cf-124"><span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>\_versão do servidor MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="df7cf-124"><span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>MSIDXSPROP\_SERVER\_VERSION</span></span> 
</dt> <dd>

<span data-ttu-id="df7cf-125">Novo no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="df7cf-125">New for Windows 7.</span></span> <span data-ttu-id="df7cf-126">ID da propriedade 9.</span><span class="sxs-lookup"><span data-stu-id="df7cf-126">Property ID 9.</span></span> <span data-ttu-id="df7cf-127">A versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="df7cf-127">The server version.</span></span>

</dd> <dt>

<span data-ttu-id="df7cf-128"><span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP \_ do servidor de \_ winver \_ principal</span><span class="sxs-lookup"><span data-stu-id="df7cf-128"><span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP\_SERVER\_WINVER\_MAJOR</span></span>
</dt> <dd>

<span data-ttu-id="df7cf-129">ID de propriedade 10.</span><span class="sxs-lookup"><span data-stu-id="df7cf-129">Property ID 10.</span></span>

</dd> <dt>

<span data-ttu-id="df7cf-130"><span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP \_ de \_ winver do servidor \_ secundário</span><span class="sxs-lookup"><span data-stu-id="df7cf-130"><span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP\_SERVER\_WINVER\_MINOR</span></span>
</dt> <dd>

<span data-ttu-id="df7cf-131">ID da propriedade 11.</span><span class="sxs-lookup"><span data-stu-id="df7cf-131">Property ID 11.</span></span>

</dd> <dt>

<span data-ttu-id="df7cf-132"><span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>\_NLSVERSION do MSIDXSPROP Server \_</span><span class="sxs-lookup"><span data-stu-id="df7cf-132"><span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>MSIDXSPROP\_SERVER\_NLSVERSION</span></span>
</dt> <dd>

<span data-ttu-id="df7cf-133">ID da propriedade 12.</span><span class="sxs-lookup"><span data-stu-id="df7cf-133">Property ID 12.</span></span>

</dd> <dt>

<span data-ttu-id="df7cf-134"><span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>\_NLSVER do servidor MSIDXSPROP \_ \_ definido</span><span class="sxs-lookup"><span data-stu-id="df7cf-134"><span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>MSIDXSPROP\_SERVER\_NLSVER\_DEFINED</span></span> 
</dt> <dd>

<span data-ttu-id="df7cf-135">ID da propriedade 13.</span><span class="sxs-lookup"><span data-stu-id="df7cf-135">Property ID 13.</span></span>

</dd> <dt>

<span data-ttu-id="df7cf-136"><span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP \_ mesma \_ SortOrder \_ usada</span><span class="sxs-lookup"><span data-stu-id="df7cf-136"><span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP\_SAME\_SORTORDER\_USED</span></span> 
</dt> <dd>

<span data-ttu-id="df7cf-137">ID da propriedade 14.</span><span class="sxs-lookup"><span data-stu-id="df7cf-137">Property ID 14.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df7cf-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="df7cf-138">Remarks</span></span>

<span data-ttu-id="df7cf-139">Para consultar a \_ versão do MSIDXSPROP Server \_ , é necessário emitir a consulta fictícia para o servidor, como o exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="df7cf-139">To query MSIDXSPROP\_SERVER\_VERSION, it is necessary to issue the dummy query to server, such as the following example.</span></span>

`SELECT top 1 workid from servername.systemindex`

<span data-ttu-id="df7cf-140">Depois que o conjunto de linhas tiver sido retornado, chame [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para os recursos do conjunto de linhas e, em seguida, chame [IRowsetInfo:: GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) para a nova propriedade ( \_ versão do servidor MSIDXSPROP \_ ).</span><span class="sxs-lookup"><span data-stu-id="df7cf-140">After the rowset has been returned, call [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the capabilities of the rowset and then call [IRowsetInfo::GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) for the new property (MSIDXSPROP\_SERVER\_VERSION).</span></span> <span data-ttu-id="df7cf-141">A propriedade tem um tipo de **VT \_ i4** e pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="df7cf-141">The property has a type of **VT\_I4** and can be one of the following values:</span></span>

<span data-ttu-id="df7cf-142">\#definir CI \_ versão \_ WDS30 0x102//258</span><span class="sxs-lookup"><span data-stu-id="df7cf-142">\#define CI\_VERSION\_WDS30 0x102 // 258</span></span>

<span data-ttu-id="df7cf-143">\#definir CI \_ versão \_ WDS40 0x109//265</span><span class="sxs-lookup"><span data-stu-id="df7cf-143">\#define CI\_VERSION\_WDS40 0x109 // 265</span></span>

<span data-ttu-id="df7cf-144">\#definir CI \_ versão \_ WIN70 0x700//1792</span><span class="sxs-lookup"><span data-stu-id="df7cf-144">\#define CI\_VERSION\_WIN70 0x700 // 1792</span></span>

<span data-ttu-id="df7cf-145">Depois que o valor é conhecido, o cliente pode formar uma consulta que é suportada pelo servidor e emitir uma consulta real.</span><span class="sxs-lookup"><span data-stu-id="df7cf-145">Once the value is known, the client can form a query which is supported by the server and issue a real query.</span></span>

<span data-ttu-id="df7cf-146">DBPROPSET \_ MSIDXS \_ ROWSETEXT é declarado em ntquery. h.</span><span class="sxs-lookup"><span data-stu-id="df7cf-146">DBPROPSET\_MSIDXS\_ROWSETEXT is declared in ntquery.h.</span></span>

 

 
