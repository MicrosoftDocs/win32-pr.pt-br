---
description: Abre um alça para uma chave privada.
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: Função SslOpenPrivateKey (Sslprovider.h)
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
ms.openlocfilehash: bab1451ada84576ee33623dfdaa7d8dcad189e6d4ef8050b0b79fafaba11b49c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905645"
---
# <a name="sslopenprivatekey-function"></a>Função SslOpenPrivateKey

A **função SslOpenPrivateKey** abre um handle para uma [*chave privada*](/windows/desktop/SecGloss/p-gly).

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

*hSslProvider* \[ Em\]
</dt> <dd>

O handle para a [*instância do provedor protocolo SSL protocolo*](/windows/desktop/SecGloss/s-gly) SSL.

</dd> <dt>

*phPrivateKey* \[ out\]
</dt> <dd>

O endereço de um buffer no qual gravar o handle na chave privada.

Quando terminar de usar a chave, você deverá liberar *phPrivateKey* chamando a [**função SslFreeObject.**](sslfreeobject.md)

</dd> <dt>

*pCertContext* \[ Em\]
</dt> <dd>

O endereço do certificado do qual obter a chave privada.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferentes de zero.

Os possíveis códigos de retorno incluem, mas não estão limitados a, o seguinte.



| Valor/código de retorno                                                                                                                                                       | Descrição                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Não há memória suficiente disponível para alocar buffers necessários.<br/> |
| <dl> <dt>**NTE \_ HANDLE \_ INVÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | O *alça hSslProvider* não é válido.<br/>                       |
| <dl> <dt>**NTE \_ PARÂMETRO \_ INVÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | O *parâmetro phPrivateKey* ou *pCertContext* é **NULL.**<br/>   |



 

## <a name="remarks"></a>Comentários

A chave privada obtida faz parte de um par [*de chaves pública/privada*](/windows/desktop/SecGloss/p-gly) dentro de um [*certificado*](/windows/desktop/SecGloss/c-gly). Essa função simplesmente extrai a chave privada do certificado especificado pelo *parâmetro pCertContext.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

