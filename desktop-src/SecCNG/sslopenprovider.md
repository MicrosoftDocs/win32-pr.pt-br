---
description: Abre um identificador para o provedor de protocolo do protocolo de protocolo SSL especificado (SSL).
ms.assetid: 0d5c4da3-12d6-4a53-a4d0-f0f174a4c8d8
title: Função SslOpenProvider (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenProvider
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8a9ea6c97662d94fffef0c87a227d5e2ae052606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164394"
---
# <a name="sslopenprovider-function"></a>Função SslOpenProvider

A função **SslOpenProvider** abre um identificador para o provedor de protocolo do [*protocolo de protocolo SSL*](/windows/desktop/SecGloss/s-gly) especificado (SSL).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslOpenProvider(
  _Out_ NCRYPT_PROV_HANDLE *phSslProvider,
  _In_  LPCWSTR            pszProviderName,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phSslProvider* \[ fora\]
</dt> <dd>

O endereço de um **\_ \_ identificador de Prov de NCRYPT** no qual gravar o identificador do provedor.

Quando terminar de usar o identificador, você deverá liberá-lo chamando a função [**SslFreeObject**](sslfreeobject.md) .

</dd> <dt>

*pszProviderName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode que contém o nome do provedor. Se o valor desse parâmetro for **NULL**, um identificador para o **provedor do \_ MS \_ Schannel** será retornado.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro e deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                       | Descrição                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl>    | Um dos identificadores fornecidos não é válido.<br/>                      |
| <dl> <dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt> </dl> | O parâmetro *phSslProvider* ou *ppProviderList* é **nulo**.<br/> |
| <dl> <dt>**Status \_ do SEM \_**</dt> <dt>0xC0000017L</dt> de memória </dl>      | Não há memória suficiente disponível para alocar os buffers necessários.<br/>  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

