---
title: Função TLSGetServerCertificate
description: Retorna o certificado do servidor de licença Área de Trabalho Remota.
ms.assetid: 7a31e7f9-f6d6-4030-b7db-43be118bb158
ms.tgt_platform: multiple
keywords:
- Função TLSGetServerCertificate Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TLSGetServerCertificate
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3144245863ee4a4316bbce8333f03ca3901cb499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755152"
---
# <a name="tlsgetservercertificate-function"></a>Função TLSGetServerCertificate

Retorna o certificado do servidor de licença Área de Trabalho Remota.

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI TLSGetServerCertificate(
  _In_  TLS_HANDLE hHandle,
  _In_  BOOL       bSignCert,
  _Out_ LPBYTE     *ppbCertBlob,
  _Out_ LPDWORD    lpdwCertBlobLen,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hHandle* \[ no\]
</dt> <dd>

Identificador para um Área de Trabalho Remota servidor de licença que é aberto por uma chamada para a função [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

</dd> <dt>

*bSignCert* \[ no\]
</dt> <dd>

**Verdadeiro** se o certificado de assinatura, **falso** , se o certificado do Exchange.

</dd> <dt>

*ppbCertBlob* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recebe um ponteiro para um buffer que contém o certificado.

</dd> <dt>

*lpdwCertBlobLen* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recebe o tamanho do certificado retornado.

</dd> <dt>

*pdwErrCode* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recebe o código de erro.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S com \_ êxito** (0)


</dt> <dd>

A chamada foi bem-sucedida.

</dd> <dt>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS \_ \_ \_ Certificado W SELFSIGN** (4007)


</dt> <dd>

O certificado retornado é um certificado autoassinado.

</dd> <dt>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS \_ \_Certificado de \_ SELFSIGN \_ temporário W** (4009)


</dt> <dd>

O certificado retornado é temporário.

</dd> <dt>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS \_ E \_ acesso \_ negado** (5003)


</dt> <dd>

Acesso negado.

</dd> <dt>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS \_ \_ \_ Identificador E alocado** (5007)


</dt> <dd>

O servidor está muito ocupado para processar a solicitação.

</dd> <dt>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS \_ E \_ nenhum \_ certificado** (5022)


</dt> <dd>

Não é possível recuperar um certificado.

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

O argumento era inválido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> </dl>

 

