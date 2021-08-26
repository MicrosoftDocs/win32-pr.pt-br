---
title: Função TLSLicenseEnumEnd
description: Continua de uma chamada anterior para a função TLSLicenseEnumBegin e encerra a enumeração .
ms.assetid: b9cba03c-0f5a-41e8-ae13-bcdd0ac6dd99
ms.tgt_platform: multiple
keywords:
- Função TLSLicenseEnumEnd Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TLSLicenseEnumEnd
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0518b9c27b01484b7fb92dd254ae6f1ccdf01d36ef602541209b9f38abd205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869206"
---
# <a name="tlslicenseenumend-function"></a>Função TLSLicenseEnumEnd

Continua de uma chamada anterior para a [**função TLSLicenseEnumBegin**](tlslicenseenumbegin.md) e encerra a enumeração .

> [!Note]  
> Essa função não tem nenhum arquivo de header associado ou biblioteca de importação. Para chamar essa função, você deve criar um arquivo de título definido pelo usuário e usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI TLSLicenseEnumEnd(
  _In_  TLS_HANDLE hHandle,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hHandle* \[ Em\]
</dt> <dd>

Lidar com um servidor Área de Trabalho Remota licença. Especifique um alça que é aberto pela [**função TLSConnectToLsServer.**](tlsconnecttolsserver.md)

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

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER \_ E \_ HANDLE \_ INVÁLIDO** (5005)


</dt> <dd>

O handle não é válido.

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

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> </dl>

 

