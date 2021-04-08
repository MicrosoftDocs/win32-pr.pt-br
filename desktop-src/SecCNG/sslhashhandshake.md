---
description: Retorna um identificador para o hash de handshake.
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: Função SslHashHandshake (Sslprovider. h)
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
ms.openlocfilehash: 1dbfdbceb4242d389669a3eebf14260a3bb396fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922450"
---
# <a name="sslhashhandshake-function"></a>Função SslHashHandshake

A função **SslHashHandshake** retorna um identificador para o hash de handshake.

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

*hSslProvider* \[ no\]
</dt> <dd>

O identificador para a instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hHandshakeHash* \[ entrada, saída\]
</dt> <dd>

O identificador para o objeto de hash.

</dd> <dt>

*pbInput* \[ fora\]
</dt> <dd>

O endereço de um buffer que contém os dados a serem armazenados em hash.

</dd> <dt>

*cbInput* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer *pbInput* .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

## <a name="remarks"></a>Comentários

A função **SslHashHandshake** é uma das três funções usadas para gerar um hash a ser usado durante o HANDSHAKE de SSL.

1.  A função [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) é chamada para obter um identificador de hash.
2.  A função **SslHashHandshake** é chamada qualquer número de vezes com o identificador de hash para adicionar dados ao hash.
3.  A função [**SslComputeFinishedHash**](sslcomputefinishedhash.md) é chamada com o identificador de hash para obter o resumo dos dados com hash.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

