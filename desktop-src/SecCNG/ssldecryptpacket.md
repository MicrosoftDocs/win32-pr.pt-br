---
description: Descriptografa um único pacote de protocolo SSL (Single protocolo SSL Protocol).
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: Função SslDecryptPacket (Sslprovider. h)
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
ms.openlocfilehash: cd568596b7e780242c0ff8d9c522a9e1758c60b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921410"
---
# <a name="ssldecryptpacket-function"></a>Função SslDecryptPacket

a função **SslDecryptPacket** descriptografa um único pacote de protocolo SSL (Single [*protocolo SSL Protocol*](/windows/desktop/SecGloss/s-gly) ).

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

*hSslProvider* \[ no\]
</dt> <dd>

O identificador da instância do provedor de protocolo SSL.

</dd> <dt>

*HKEY* \[ entrada, saída\]
</dt> <dd>

O identificador para a chave que é usada para descriptografar o pacote.

</dd> <dt>

*pbInput* \[ no\]
</dt> <dd>

Um ponteiro para o buffer que contém o pacote a ser descriptografado.

</dd> <dt>

*cbInput* \[ no\]
</dt> <dd>

O comprimento, em bytes, do buffer *pbInput* .

</dd> <dt>

*pbOutput* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que contém o pacote descriptografado.

</dd> <dt>

*cbOutput* \[ no\]
</dt> <dd>

O comprimento, bytes, do buffer *pbOutput* .

</dd> <dt>

*pcbResult* \[ fora\]
</dt> <dd>

O número de bytes gravados no buffer *pbOutput* .

</dd> <dt>

*SequenceNumber* \[ no\]
</dt> <dd>

O número de sequência que corresponde a este pacote.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                    | Descrição                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl> | Um dos identificadores fornecidos não é válido.<br/> |



 

## <a name="remarks"></a>Comentários

O comprimento do pacote pode ser zero, como quando uma mensagem "HelloRequest" é descriptografada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

