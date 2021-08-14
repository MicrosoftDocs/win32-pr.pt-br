---
description: Criptografa um único protocolo SSL protocolo SSL.
ms.assetid: 1002158b-1a4f-4461-978f-b221ef6332e0
title: Função SslEncryptPacket (Sslprovider.h)
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
ms.openlocfilehash: 74c489cae777b6ca7ac93020fb80ab198622fae97640c09cbd99544c2dafa4e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906658"
---
# <a name="sslencryptpacket-function"></a>Função SslEncryptPacket

A **função SslEncryptPacket** criptografa um único [*protocolo SSL protocolo*](/windows/desktop/SecGloss/s-gly) SSL.

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

*hSslProvider* \[ Em\]
</dt> <dd>

O handle da instância do provedor de protocolo SSL.

</dd> <dt>

*hKey* \[ in, out\]
</dt> <dd>

O handle para a chave usada para criptografar o pacote.

</dd> <dt>

*pbInput* \[ Em\]
</dt> <dd>

Um ponteiro para o buffer que contém o pacote a ser criptografado.

</dd> <dt>

*cbInput* \[ Em\]
</dt> <dd>

O comprimento, em bytes, do *buffer pbInput.*

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Um ponteiro para um buffer para receber o pacote criptografado.

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

*dwContentType* \[ Em\]
</dt> <dd>

O tipo de conteúdo que corresponde a esse pacote, que especifica o protocolo de nível superior usado para processar o pacote incluído.



| Valor                                                                                                                                                                                                                                           | Significado                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="CT_CHANGE_CIPHER_SPEC"></span><span id="ct_change_cipher_spec"></span><dl> <dt>**CT \_ ALTERAR \_ ESPECIFICAÇÃO \_ DE CODIFICAÇÃO**</dt> <dt>20</dt> </dl> | Indica uma alteração na estratégia de codificação.<br/>                         |
| <span id="CT_ALERT"></span><span id="ct_alert"></span><dl> <dt>**CT \_ ALERTA**</dt> <dt>21</dt> </dl>                                          | Indica que o pacote incluído contém um alerta.<br/>                 |
| <span id="CT_HANDSHAKE"></span><span id="ct_handshake"></span><dl> <dt>**CT \_ HANDSHAKE**</dt> <dt>22</dt> </dl>                              | Indica que o pacote incluído faz parte do protocolo de handshake.<br/> |
| <span id="CT_APPLICATIONDATA"></span><span id="ct_applicationdata"></span><dl> <dt>**CT \_ APPLICATIONDATA**</dt> <dt>23</dt> </dl>            | Indica que o pacote contém dados do aplicativo.<br/>                  |



 

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



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

