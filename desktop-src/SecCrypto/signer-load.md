---
description: Carrega um certificado de autenticação de um arquivo. pfx especificado.
ms.assetid: 98963354-c237-40d0-9235-8318728e2c8e
title: Método signatário. Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9a817a95ca825b67b54a41fc674db10bf81b5740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769270"
---
# <a name="signerload-method"></a>Método signatário. Load

\[O método **Load** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O método **Load** carrega um certificado de autenticação de um arquivo. pfx especificado.

## <a name="syntax"></a>Sintaxe


```VB
Signer.Load( _
  ByVal FileName, _
  [ ByVal Password ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FileName* 
</dt> <dd>

Nome do arquivo. pfx que contém o certificado de autenticação.

</dd> <dt>

*Senha* \[ do adicional\]
</dt> <dd>

Cadeia de caracteres que contém a senha de texto não criptografado usada para abrir o arquivo. Até 32 caracteres Unicode, incluindo um caractere nulo de terminação, podem ser usados para a senha. O valor padrão é uma cadeia de caracteres vazia (""). Para obter informações sobre como proteger a senha, consulte [manipulando senhas](../secbp/handling-passwords.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método carrega o primeiro certificado no arquivo. pfx que tem uma chave privada associada a ele.

Esse método gera CAPICOM \_ E \_ não \_ são permitidos quando são inseridos em script de um aplicativo baseado na Web.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Signatário**](signer.md)
</dt> </dl>

 

 
