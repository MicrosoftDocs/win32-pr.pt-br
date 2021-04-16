---
description: Criptografa um pacote de protocolo SSL (Single protocolo SSL Protocol).
ms.assetid: 1002158b-1a4f-4461-978f-b221ef6332e0
title: Função SslEncryptPacket (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEncryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e839b37e839fd09d5df5f9902474b7ce7c4c74a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750501"
---
# <a name="sslencryptpacket-function"></a>Função SslEncryptPacket

A função **SslEncryptPacket** criptografa um único pacote de protocolo SSL (Single [*protocolo SSL Protocol*](/windows/desktop/SecGloss/s-gly) ).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslEncryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwContentType,
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

O identificador para a chave que é usada para criptografar o pacote.

</dd> <dt>

*pbInput* \[ no\]
</dt> <dd>

Um ponteiro para o buffer que contém o pacote a ser criptografado.

</dd> <dt>

*cbInput* \[ no\]
</dt> <dd>

O comprimento, em bytes, do buffer *pbInput* .

</dd> <dt>

*pbOutput* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer para receber o pacote criptografado.

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

*dwContentType* \[ no\]
</dt> <dd>

O tipo de conteúdo que corresponde a esse pacote, que especifica o protocolo de nível superior usado para processar o pacote incluído.



| Valor                                                                                                                                                                                                                                           | Significado                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="CT_CHANGE_CIPHER_SPEC"></span><span id="ct_change_cipher_spec"></span><dl> <dt>**CT \_ ALTERAR \_ \_ especificação de codificação**</dt> <dt>20</dt> </dl> | Indica uma alteração na estratégia de codificação.<br/>                         |
| <span id="CT_ALERT"></span><span id="ct_alert"></span><dl> <dt>**CT \_ ALERTA**</dt> <dt>21</dt> </dl>                                          | Indica que o pacote incluído contém um alerta.<br/>                 |
| <span id="CT_HANDSHAKE"></span><span id="ct_handshake"></span><dl> <dt>**CT \_ HANDSHAKE**</dt> <dt>22</dt> </dl>                              | Indica que o pacote incluído faz parte do protocolo de handshake.<br/> |
| <span id="CT_APPLICATIONDATA"></span><span id="ct_applicationdata"></span><dl> <dt>**CT \_ APPLICATIONDATA**</dt> <dt>23</dt> </dl>            | Indica que o pacote contém dados de aplicativo.<br/>                  |



 

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



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

