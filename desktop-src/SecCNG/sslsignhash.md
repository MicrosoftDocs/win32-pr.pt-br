---
description: Assina um hash usando a chave privada especificada.
ms.assetid: 25e8ebc5-278d-4d1f-977a-c2fab07b790a
title: Função SslSignHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslSignHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 339d0a27cb987557ff90cbd0f489813edb357b77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461036"
---
# <a name="sslsignhash-function"></a>Função SslSignHash

A função **SslSignHash** assina um [*hash*](/windows/desktop/SecGloss/h-gly) usando a [*chave privada*](/windows/desktop/SecGloss/p-gly)especificada. O processo de assinatura é executado no servidor.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslSignHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  PBYTE              pbHashValue,
  _In_  DWORD              cbHashValue,
  _Out_ PBYTE              pbSignature,
  _In_  DWORD              cbSignature,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ no\]
</dt> <dd>

O identificador para a instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hPrivateKey* \[ no\]
</dt> <dd>

O identificador para a chave privada a ser usada para assinar o hash.

</dd> <dt>

*pbHashValue* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que contém o hash a ser assinado.

</dd> <dt>

*cbHashValue* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer *pbHashValue* .

</dd> <dt>

*pbSignature* \[ fora\]
</dt> <dd>

O endereço de um buffer que recebe a assinatura do hash. O parâmetro *cbSignature* contém o tamanho desse buffer. Para determinar o tamanho de dimensionamento necessário do buffer, defina o parâmetro *pbSignature* como **NULL**. O tamanho necessário do buffer será retornado no parâmetro *pcbResult* .

</dd> <dt>

*cbSignature* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer *pbSignature* .

</dd> <dt>

*pcbResult* \[ fora\]
</dt> <dd>

Um ponteiro para um valor que, após a conclusão, contém o número real de bytes gravados no buffer *pbSignature* .

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



 

