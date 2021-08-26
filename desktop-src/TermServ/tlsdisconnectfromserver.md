---
title: Função TLSDisconnectFromServer
description: Fecha um identificador aberto para um servidor de licença Área de Trabalho Remota.
ms.assetid: b4b001ec-823b-4514-bbec-839a83a9a189
ms.tgt_platform: multiple
keywords:
- Função TLSDisconnectFromServer Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TLSDisconnectFromServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95911536eda4bd87e45fd034626cf83d88f4d9fc768e4837316ee93abfe3c3d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869406"
---
# <a name="tlsdisconnectfromserver-function"></a>Função TLSDisconnectFromServer

Fecha um identificador aberto para um servidor de licença Área de Trabalho Remota.

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI TLSDisconnectFromServer(
  _In_ TLS_HANDLE hHandle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hHandle* \[ no\]
</dt> <dd>

Identificador para um Área de Trabalho Remota servidor de licença que é aberto por uma chamada para a função [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Chame a função **TLSDisconnectFromServer** como parte da rotina de limpeza do programa para fechar todos os identificadores do servidor que são abertos por chamadas para a função [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**identificador de TLS \_**](tls-handle.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> </dl>

 

