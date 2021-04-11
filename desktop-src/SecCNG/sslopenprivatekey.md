---
description: Abre um identificador para uma chave privada.
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: Função SslOpenPrivateKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenPrivateKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 6fd5c10ce6385e377c72d21f4557d27d2345737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090198"
---
# <a name="sslopenprivatekey-function"></a>Função SslOpenPrivateKey

A função **SslOpenPrivateKey** abre um identificador para uma [*chave privada*](/windows/desktop/SecGloss/p-gly).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslOpenPrivateKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phPrivateKey,
  _In_  PCCERT_CONTEXT     pCertContext,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ no\]
</dt> <dd>

O identificador para a instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*phPrivateKey* \[ fora\]
</dt> <dd>

O endereço de um buffer no qual gravar o identificador para a chave privada.

Quando terminar de usar a chave, você deverá liberar *phPrivateKey* chamando a função [**SslFreeObject**](sslfreeobject.md) .

</dd> <dt>

*pCertContext* \[ no\]
</dt> <dd>

O endereço do certificado do qual obter a chave privada.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                       | Descrição                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória </dl>         | Não há memória suficiente disponível para alocar os buffers necessários.<br/> |
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl>    | O identificador *hSslProvider* não é válido.<br/>                       |
| <dl> <dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt> </dl> | O parâmetro *phPrivateKey* ou *pCertContext* é **nulo**.<br/>   |



 

## <a name="remarks"></a>Comentários

A chave privada obtida faz parte de um [*par de chaves pública/privada*](/windows/desktop/SecGloss/p-gly) dentro de um [*certificado*](/windows/desktop/SecGloss/c-gly). Essa função simplesmente extrai a chave privada do certificado especificado pelo parâmetro *pCertContext* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

