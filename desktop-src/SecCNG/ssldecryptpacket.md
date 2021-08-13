---
description: Descriptografa um único protocolo SSL protocolo SSL.
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: Função SslDecryptPacket (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 0b058fbb01183ccf0582c0fa196bec71bfaffa2e8a44739c1ea5fb01a8148174
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906698"
---
# <a name="ssldecryptpacket-function"></a>Função SslDecryptPacket

A **função SslDecryptPacket** descriptografa um [*único*](/windows/desktop/SecGloss/s-gly) pacote SSL (protocolo protocolo SSL protocolo SSL).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslDecryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ Em\]
</dt> <dd>

O handle da instância do provedor de protocolo SSL.

</dd> <dt>

*hKey* \[ in, out\]
</dt> <dd>

O handle para a chave usada para descriptografar o pacote.

</dd> <dt>

*pbInput* \[ Em\]
</dt> <dd>

Um ponteiro para o buffer que contém o pacote a ser descriptografado.

</dd> <dt>

*cbInput* \[ Em\]
</dt> <dd>

O comprimento, em bytes, do *buffer pbInput.*

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Um ponteiro para um buffer para conter o pacote descriptografado.

</dd> <dt>

*cbOutput* \[ Em\]
</dt> <dd>

O comprimento, bytes, do buffer *pbOutput.*

</dd> <dt>

*pcbResult* \[ out\]
</dt> <dd>

O número de bytes gravados no buffer *pbOutput.*

</dd> <dt>

*SequenceNumber* \[ Em\]
</dt> <dd>

O número de sequência que corresponde a este pacote.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferentes de zero.

Os possíveis códigos de retorno incluem, mas não estão limitados a, o seguinte.



| Valor/código de retorno                                                                                                                                                    | Descrição                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ INVÁLIDO**</dt> <dt>0x80090026L</dt> </dl> | Um dos alças fornecidos não é válido.<br/> |



 

## <a name="remarks"></a>Comentários

O comprimento do pacote pode ser zero, como quando uma mensagem "HelloRequest" é descriptografada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

