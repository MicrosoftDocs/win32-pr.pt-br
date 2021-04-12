---
title: Função TLSKeyPackEnumBegin
description: Inicia a enumeração por meio de todos os pacotes de chaves instalados em um servidor de licença Área de Trabalho Remota com base nos critérios de pesquisa.
ms.assetid: 2d847fe4-66ab-42df-8213-651e14257590
ms.tgt_platform: multiple
keywords:
- Função TLSKeyPackEnumBegin Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TLSKeyPackEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db8f61197e3c08f5608be954a9288ea54cad5586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295899"
---
# <a name="tlskeypackenumbegin-function"></a>Função TLSKeyPackEnumBegin

Inicia a enumeração por meio de todos os pacotes de chaves instalados em um servidor de licença Área de Trabalho Remota com base nos critérios de pesquisa.

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI TLSKeyPackEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSKeyPack  *lpSearchParm,
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

Especifica os critérios de pesquisa. Esse parâmetro é reservado para uso futuro e deve conter 0xFFFFFFFF.

</dd> <dt>

*bMatchAll* \[ no\]
</dt> <dd>

Especifica se é para corresponder a todos os valores de pesquisa.

</dd> <dt>

*lpSearchParm* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura [**LSKeyPack**](lskeypack.md) que especifica os parâmetros de pesquisa a serem procurados.

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

## <a name="return-value"></a>Retornar valor

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

[**LSKeyPack**](lskeypack.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> </dl>

 

