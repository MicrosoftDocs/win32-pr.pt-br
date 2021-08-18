---
title: Função TLSKeyPackEnumEnd
description: Continua de uma chamada anterior para a função TLSKeyPackEnumBegin e encerra a enumeração .
ms.assetid: 3434e18d-54c9-46ed-b6a5-bc174b63a152
ms.tgt_platform: multiple
keywords:
- Função TLSKeyPackEnumEnd Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TLSKeyPackEnumEnd
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 176c5d6b03fabe2e085b2582043233cd5fdc2681ef04ef07723ba5435a465863
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986916"
---
# <a name="tlskeypackenumend-function"></a>Função TLSKeyPackEnumEnd

Continua de uma chamada anterior para a [**função TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) e encerra a enumeração .

> [!Note]  
> Essa função não tem nenhum arquivo de header associado ou biblioteca de importação. Para chamar essa função, você deve criar um arquivo de título definido pelo usuário e usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI TLSKeyPackEnumEnd(
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

[**LSKeyPack**](lskeypack.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> </dl>

 

