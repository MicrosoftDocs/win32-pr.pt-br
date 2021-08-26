---
title: Função TLSLicenseEnumBegin
description: Inicia a enumeração de licenças emitidas pelo servidor de licença Área de Trabalho Remota com base nos critérios de pesquisa.
ms.assetid: ec575632-b828-49c0-b326-1ab420381875
ms.tgt_platform: multiple
keywords:
- Função TLSLicenseEnumBegin Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TLSLicenseEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620f6487bb516a76ac5cb7f77da9983178933c24ac03151bd9a4c8455f694ec9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986876"
---
# <a name="tlslicenseenumbegin-function"></a>Função TLSLicenseEnumBegin

Inicia a enumeração de licenças emitidas pelo servidor de licença Área de Trabalho Remota com base nos critérios de pesquisa.

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI TLSLicenseEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSLicense  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hHandle* \[ no\]
</dt> <dd>

Identificador para um servidor de licença Área de Trabalho Remota. Especifique um identificador que é aberto pela função [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

</dd> <dt>

*dwSearchParm* \[ no\]
</dt> <dd>

Especifica os critérios de pesquisa. O parâmetro pode ser um ou uma combinação dos valores descritos na lista a seguir. O parâmetro especifica o tipo de pacote de chaves e o pacote de chaves a ser pesquisado.

<dt>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE \_ \_Licença de pesquisa** (0x00000001)


</dt> <dd>

Pesquisar por ID da licença.

</dd> <dt>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE \_ SEARCH \_ Packid** (0x00000002)


</dt> <dd>

Pesquise por ID do pacote de chaves.

</dd> <dt>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE \_ Pesquisar \_ MachineName** (0x00000008)


</dt> <dd>

Pesquisar por nome do computador.

</dd> <dt>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE \_ \_Nome de usuário da pesquisa** (0x00000010)


</dt> <dd>

Pesquisar por nome de usuário.

</dd> <dt>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE \_ PESQUISA \_ emitida** (0x00000080)


</dt> <dd>

Pesquisar por data de emissão.

</dd> <dt>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE \_ PESQUISA \_ expirada** (0x00000100)


</dt> <dd>

Pesquisar por data de validade.

</dd> <dt>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE \_ Pesquisar \_ NUMLICENSES** (0x00000200)


</dt> <dd>

Pesquisar por número de licenças.

</dd> <dt>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE \_ \_ \_ Status de entrada de pesquisa** (0x20000000)


</dt> <dd>

Pesquisar por status de entrada.

</dd> <dt>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE \_ \_LICENSESTATUS do exsearch** (0x00100000)


</dt> <dd>

Pesquisar por status da licença.

</dd> <dt>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK \_ Pesquisar \_ tudo** (0xFFFFFFFF)


</dt> <dd>

Pesquisar todas as licenças.

</dd> </dl> </dd> <dt>

*bMatchAll* \[ no\]
</dt> <dd>

Especifica se é para corresponder a todos os valores de pesquisa.

</dd> <dt>

*lpSearchParm* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura [**LSLicense**](lslicense.md) que especifica os parâmetros de pesquisa a serem procurados.

</dd> <dt>

*pdwErrCode* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recebe um dos seguintes códigos de erro no retorno.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S com \_ êxito** (0)


</dt> <dd>

A chamada foi bem-sucedida.

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ \_ \_ Erro interno E** (5001)


</dt> <dd>

Erro interno no servidor de licença.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ \_ \_ Sequência inválida E** (5006)


</dt> <dd>

A sequência de chamada não era válida. Provavelmente, uma enumeração anterior não terminou.

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ \_Servidor E \_ ocupado** (5007)


</dt> <dd>

O servidor de licenças está muito ocupado para processar a solicitação.

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OUTOFMEMORY** (5008)


</dt> <dd>

Não é possível processar a solicitação devido à memória insuficiente.

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER \_ E \_ \_ dados inválidos** (5009)


</dt> <dd>

Os dados no parâmetro de pesquisa não são válidos.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função retorna os seguintes valores de retorno possíveis.

<dl> <dt>

**RPC \_ S \_ OK**
</dt> <dd>

A chamada foi bem-sucedida. Verifique o valor do parâmetro *pdwErrCode* para obter o código de retorno para a chamada.

</dd> <dt>

**ARG. de RPC \_ \_ inválido \_**
</dt> <dd>

O argumento não era válido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LSLicense**](lslicense.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> </dl>

 

