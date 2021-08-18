---
description: Verifica a assinatura especificada usando o hash fornecido e a chave pública.
ms.assetid: fa274851-15f2-4be0-9e2f-4cdced36daff
title: Função SslVerifySignature (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslVerifySignature
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: b020f41822185dfc9e4e2513fc9e299bc35d9bbb258aaeddf6f1e1e8ea7b8cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905655"
---
# <a name="sslverifysignature-function"></a>Função SslVerifySignature

A função **SslVerifySignature** verifica a assinatura especificada usando o [*hash*](/windows/desktop/SecGloss/h-gly) fornecido e a [*chave pública*](/windows/desktop/SecGloss/p-gly).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslVerifySignature(
  _In_ NCRYPT_PROV_HANDLE hSslProvider,
  _In_ NCRYPT_KEY_HANDLE  hPublicKey,
  _In_ PBYTE              pbHashValue,
  _In_ DWORD              cbHashValue,
  _In_ PBYTE              pbSignature,
  _In_ DWORD              cbSignature,
  _In_ DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ no\]
</dt> <dd>

O identificador para a instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hPublicKey* \[ no\]
</dt> <dd>

O identificador para a chave pública.

</dd> <dt>

*pbHashValue* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que contém o hash a ser usado para verificar a assinatura.

</dd> <dt>

*cbHashValue* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer *pbHashValue* .

</dd> <dt>

*pbSignature* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que contém a assinatura a ser verificada.

</dd> <dt>

*cbSignature* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer *pbSignature* .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                    | Descrição                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl> | Um dos identificadores fornecidos não é válido.<br/> |



 

## <a name="remarks"></a>Comentários

A função **SslVerifySignature** não é chamada atualmente por Windows. Essa função é uma parte necessária da interface do provedor SSL e deve ser totalmente implementada para garantir a compatibilidade com o futuro.

As implementações atuais do lado do servidor da conexão do [*protocolo*](/windows/desktop/SecGloss/t-gly) TLS chamam a função [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) durante a autenticação do cliente para processar a mensagem de verificação de certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

