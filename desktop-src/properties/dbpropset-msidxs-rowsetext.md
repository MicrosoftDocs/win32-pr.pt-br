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
# <a name="dbpropset_msidxs_rowsetext"></a>DBPROPSET \_ MSIDXS \_ ROWSETEXT

Estende as propriedades definidas para as APIs do conjunto de linhas.

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

O \_ conjunto de propriedades DBPROPSET MSIDXS \_ ROWSETEXT contém as seguintes constantes de propriedade:

<dl> <dt>

<span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP \_ ROWSETQUERYSTATUS
</dt> <dd>

ID da propriedade 2. Status da consulta para o conjunto de linhas. As \_ \* constantes stat indicam o status de execução e de confiabilidade.

</dd> <dt>

<span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>\_cadeia de \_ caracteres de localidade do comando MSIDXSPROP \_
</dt> <dd>

ID da propriedade 3. Cadeia de caracteres de localidade que representa a configuração de idioma e localidade a ser usada para este conjunto de linhas.

</dd> <dt>

<span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>\_restrição de consulta MSIDXSPROP \_
</dt> <dd>

ID da propriedade 4. A cadeia de caracteres de consulta associada a este conjunto de linhas.

</dd> <dt>

<span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>\_árvore de análise do MSIDXSPROP \_
</dt> <dd>

ID da propriedade 5.

</dd> <dt>

<span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>\_classificação máxima de MSIDXSPROP \_ 
</dt> <dd>

ID da propriedade 6.

</dd> <dt>

<span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>resultados de MSIDXSPROP \_ \_ encontrados
</dt> <dd>

ID da propriedade 7.

</dd> <dt>

<span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP \_ whereid
</dt> <dd>

ID da propriedade 8.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>\_versão do servidor MSIDXSPROP \_ 
</dt> <dd>

Novo no Windows 7. ID da propriedade 9. A versão do servidor.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP \_ do servidor de \_ winver \_ principal
</dt> <dd>

ID de propriedade 10.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP \_ de \_ winver do servidor \_ secundário
</dt> <dd>

ID da propriedade 11.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>\_NLSVERSION do MSIDXSPROP Server \_
</dt> <dd>

ID da propriedade 12.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>\_NLSVER do servidor MSIDXSPROP \_ \_ definido 
</dt> <dd>

ID da propriedade 13.

</dd> <dt>

<span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP \_ mesma \_ SortOrder \_ usada 
</dt> <dd>

ID da propriedade 14.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para consultar a \_ versão do MSIDXSPROP Server \_ , é necessário emitir a consulta fictícia para o servidor, como o exemplo a seguir.

`SELECT top 1 workid from servername.systemindex`

Depois que o conjunto de linhas tiver sido retornado, chame [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para os recursos do conjunto de linhas e, em seguida, chame [IRowsetInfo:: GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) para a nova propriedade ( \_ versão do servidor MSIDXSPROP \_ ). A propriedade tem um tipo de **VT \_ i4** e pode ser um dos seguintes valores:

\#definir CI \_ versão \_ WDS30 0x102//258

\#definir CI \_ versão \_ WDS40 0x109//265

\#definir CI \_ versão \_ WIN70 0x700//1792

Depois que o valor é conhecido, o cliente pode formar uma consulta que é suportada pelo servidor e emitir uma consulta real.

DBPROPSET \_ MSIDXS \_ ROWSETEXT é declarado em ntquery. h.

 

 
