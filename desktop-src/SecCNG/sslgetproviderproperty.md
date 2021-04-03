---
description: Recupera o valor de uma propriedade de provedor especificada.
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: Função SslGetProviderProperty (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetProviderProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ced0f32d45531a1220f7aae9fe0e660648e5d1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829663"
---
# <a name="sslgetproviderproperty-function"></a>Função SslGetProviderProperty

A função **SslGetProviderProperty** recupera o valor de uma propriedade de provedor especificada.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslGetProviderProperty(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _In_    LPCWSTR            pszProperty,
  _Out_   PBYTE              ppbOutput,
  _Out_   DWORD              *pcbOutput,
  _Inout_ PVOID              *ppEnumState,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ no\]
</dt> <dd>

O identificador do provedor de [*protocolo de protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL) para o qual recuperar a propriedade.

</dd> <dt>

*pszProperty* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o nome da propriedade a ser recuperada.

</dd> <dt>

*ppbOutput* \[ fora\]
</dt> <dd>

O endereço de um buffer que recebe o valor da propriedade.

O chamador da função deve liberar esse buffer chamando a função [**SslFreeBuffer**](sslfreebuffer.md) .

</dd> <dt>

*pcbOutput* \[ fora\]
</dt> <dd>

O tamanho, em bytes, do buffer *pbOutput* .

</dd> <dt>

*ppEnumState* \[ entrada, saída\]
</dt> <dd>

O endereço de um ponteiro **void** que recebe informações de estado de enumeração que são usadas em chamadas subsequentes para essa função. Essas informações só têm significado para o provedor SSL e são opacas para o chamador. O provedor SSL usa essas informações para determinar qual item está em seguida na enumeração. Se a variável apontada por esse parâmetro contiver **NULL**, a enumeração será iniciada desde o início.

O chamador da função deve liberar essa memória chamando a função [**SslFreeBuffer**](sslfreebuffer.md) .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                       | Description                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória </dl>         | Não há memória suficiente disponível para alocar os buffers necessários.<br/> |
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl>    | O identificador *hSslProvider* não é válido.<br/>                       |
| <dl> <dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt> </dl> | Um dos parâmetros fornecidos não é válido.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

