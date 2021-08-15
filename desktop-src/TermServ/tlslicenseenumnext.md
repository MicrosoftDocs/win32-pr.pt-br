---
title: Função TLSLicenseEnumNext
description: Continua de uma chamada anterior para a função TLSLicenseEnumBegin e retorna a próxima licença instalada em um servidor de licença Área de Trabalho Remota que corresponde aos critérios de pesquisa.
ms.assetid: 6932289b-b59c-493c-8dbc-03c0662e921e
ms.tgt_platform: multiple
keywords:
- Função TLSLicenseEnumNext Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TLSLicenseEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 945c0afb931770a36049342f32c71613bd8fb1a0a9b16142c1ffbc6a67ccc288
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986796"
---
# <a name="tlslicenseenumnext-function"></a>Função TLSLicenseEnumNext

Continua de uma chamada anterior para a função [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) e retorna a próxima licença instalada em um servidor de licença Área de Trabalho Remota que corresponde aos critérios de pesquisa.

> [!Note]  
> Essa função não tem nenhum arquivo de header associado ou biblioteca de importação. Para chamar essa função, você deve criar um arquivo de título definido pelo usuário e usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI TLSLicenseEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LSLicense  *lpLicense,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hHandle* \[ Em\]
</dt> <dd>

Lidar com um servidor Área de Trabalho Remota licença. Especifique um alça que é aberto pela [**função TLSConnectToLsServer.**](tlsconnecttolsserver.md)

</dd> <dt>

*lpLicense* \[ Em\]
</dt> <dd>

Ponteiro para uma [**estrutura LSLicense**](lslicense.md) que recebe a próxima licença que corresponde aos critérios de pesquisa.

</dd> <dt>

*pdwErrCode* \[ out\]
</dt> <dd>

Ponteiro para uma variável que recebe um dos códigos de erro a seguir no retorno.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S \_ SUCCESS** (0)


</dt> <dd>

A chamada foi bem-sucedida.

</dd> <dt>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER \_ NÃO \_ HÁ \_ MAIS \_ DADOS** (4001)


</dt> <dd>

Não há mais licenças que corresponderem aos critérios de pesquisa.

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ ERRO \_ \_ INTERNO DO E** (5001)


</dt> <dd>

Erro interno no servidor de licença.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ E \_ SEQUÊNCIA \_ INVÁLIDA** (5006)


</dt> <dd>

A sequência de chamada não era válida. Deve chamar a [**função TLSLicenseEnumBegin()**](tlslicenseenumbegin.md) antes disso.

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ E \_ SERVER \_ BUSY** (5007)


</dt> <dd>

O servidor de licença está muito ocupado para processar a solicitação.

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OUTOFMEMORY** (5008)


</dt> <dd>

Não é possível processar a solicitação devido à memória insuficiente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função retorna os seguintes valores de retorno possíveis.

<dl> <dt>

**RPC \_ S \_ OK**
</dt> <dd>

A chamada foi bem-sucedida. Verifique o valor do parâmetro *pdwErrCode* para obter o código de retorno da chamada.

</dd> <dt>

**RPC \_ S \_ \_ ARG INVÁLIDO**
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

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> </dl>

 

