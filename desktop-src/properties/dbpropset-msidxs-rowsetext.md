---
description: Estende as propriedades definidas para as APIs de conjuntos de linhas.
ms.assetid: C1A2DF19-C68D-42CC-9CB2-190F22CB4158
title: DBPROPSET_MSIDXS_ROWSETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8c647d4b1ecbf9e5cc88ccae4af649c27093472456377e478ff80f7a76f3a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776406"
---
# <a name="dbpropset_msidxs_rowsetext"></a>DBPROPSET \_ MSIDXS \_ ROWSETEXT

Estende as propriedades definidas para as APIs de conjuntos de linhas.

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

O conjunto de propriedades DBPROPSET \_ MSIDXS \_ ROWSETEXT contém as seguintes constantes de propriedade:

<dl> <dt>

<span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP \_ ROWSETQUERYSTATUS
</dt> <dd>

ID da propriedade 2. Status da consulta para o conjuntos de linhas. As constantes STAT \_ \* indicam o status de execução e confiabilidade.

</dd> <dt>

<span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>CADEIA DE CARACTERES DE LOCALIDADE DE COMANDO MSIDXSPROP \_ \_ \_
</dt> <dd>

ID da propriedade 3. Cadeia de caracteres de localidade que representa a configuração de idioma e localidade a ser usada para esse conjuntos de linhas.

</dd> <dt>

<span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>RESTRIÇÃO DE CONSULTA MSIDXSPROP \_ \_
</dt> <dd>

ID da propriedade 4. A cadeia de caracteres de consulta associada a este rowset.

</dd> <dt>

<span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>ÁRVORE DE ANÁLISE MSIDXSPROP \_ \_
</dt> <dd>

ID da propriedade 5.

</dd> <dt>

<span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>MSIDXSPROP \_ MAX \_ RANK 
</dt> <dd>

ID da propriedade 6.

</dd> <dt>

<span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>RESULTADOS DE MSIDXSPROP \_ \_ ENCONTRADOS
</dt> <dd>

ID da propriedade 7.

</dd> <dt>

<span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP \_ WHEREID
</dt> <dd>

ID da propriedade 8.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>VERSÃO DO SERVIDOR MSIDXSPROP \_ \_ 
</dt> <dd>

Novo para Windows 7. ID da propriedade 9. A versão do servidor.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP \_ SERVER \_ WINVER \_ MAJOR
</dt> <dd>

ID da propriedade 10.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP \_ SERVER \_ WINVER \_ MINOR
</dt> <dd>

ID da propriedade 11.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>MSIDXSPROP \_ SERVER \_ NLSVERSION
</dt> <dd>

ID da propriedade 12.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>MSIDXSPROP \_ SERVER \_ NLSVER \_ DEFINIDO 
</dt> <dd>

ID da propriedade 13.

</dd> <dt>

<span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP \_ MESMO \_ SORTORDER \_ USADO 
</dt> <dd>

ID da propriedade 14.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para consultar MSIDXSPROP SERVER VERSION, é necessário emitir a consulta fiada para o servidor, como \_ o exemplo a \_ seguir.

`SELECT top 1 workid from servername.systemindex`

Depois que o conjuntos de linhas for retornado, chame [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para os recursos do conjuntos de linhas e, em seguida, chame [IRowsetInfo::GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) para a nova propriedade (MSIDXSPROP \_ SERVER \_ VERSION). A propriedade tem um tipo de **VT \_ I4** e pode ser um dos seguintes valores:

\#definir CI \_ VERSION \_ WDS30 0x102 // 258

\#definir CI \_ VERSION \_ WDS40 0x109 // 265

\#definir CI \_ VERSION \_ WIN70 0x700 // 1792

Depois que o valor for conhecido, o cliente poderá formar uma consulta com suporte pelo servidor e emitir uma consulta real.

DBPROPSET \_ MSIDXS \_ ROWSETEXT é declarado em ntquery.h.

 

 
