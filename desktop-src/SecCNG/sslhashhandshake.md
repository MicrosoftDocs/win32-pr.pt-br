---
description: Retorna um alça para o hash de handshake.
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: Função SslHashHandshake (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslHashHandshake
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 5a21bdb3fd655e5c3b39249937f04a4122c64e6c6176c0d39ae1164e48863edb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906094"
---
# <a name="sslhashhandshake-function"></a>Função SslHashHandshake

A **função SslHashHandshake** retorna um alça para o hash de handshake.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslHashHandshake(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_   PBYTE              pbInput,
  _In_    DWORD              cbInput,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ Em\]
</dt> <dd>

O handle para a [*instância do provedor protocolo SSL protocolo*](/windows/desktop/SecGloss/s-gly) SSL.

</dd> <dt>

*hHandshakeHash* \[ in, out\]
</dt> <dd>

O identificador para o objeto hash.

</dd> <dt>

*pbInput* \[ out\]
</dt> <dd>

O endereço de um buffer que contém os dados a serem armazenados em hashed.

</dd> <dt>

*cbInput* \[ Em\]
</dt> <dd>

O tamanho, em bytes, do buffer *pbInput.*

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará zero.

## <a name="remarks"></a>Comentários

A **função SslHashHandshake** é uma das três funções usadas para gerar um hash a ser usado durante o handshake SSL.

1.  A [**função SslCreateHandshakeHash**](sslcreatehandshakehash.md) é chamada para obter um alça de hash.
2.  A **função SslHashHandshake** é chamada de qualquer número de vezes com o alça de hash para adicionar dados ao hash.
3.  A [**função SslComputeFinishedHash**](sslcomputefinishedhash.md) é chamada com o alça de hash para obter o resumo dos dados com hash.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

