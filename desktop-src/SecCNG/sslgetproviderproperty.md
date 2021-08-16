---
description: Recupera o valor de uma propriedade de provedor especificada.
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: Função SslGetProviderProperty (Sslprovider.h)
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
ms.openlocfilehash: bfe65fe4033397fd5885eceb3bf0d2ac9ce9aa9b487a84ab7611cb253d979220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906104"
---
# <a name="sslgetproviderproperty-function"></a>Função SslGetProviderProperty

A **função SslGetProviderProperty** recupera o valor de uma propriedade de provedor especificada.

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

*hSslProvider* \[ Em\]
</dt> <dd>

O handle do provedor [*protocolo SSL protocolo*](/windows/desktop/SecGloss/s-gly) SSL para o qual recuperar a propriedade.

</dd> <dt>

*pszProperty* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o nome da propriedade a ser recuperada.

</dd> <dt>

*ppbOutput* \[ out\]
</dt> <dd>

O endereço de um buffer que recebe o valor da propriedade.

O chamador da função deve liberar esse buffer chamando a [**função SslFreeBuffer.**](sslfreebuffer.md)

</dd> <dt>

*pcbOutput* \[ out\]
</dt> <dd>

O tamanho, em bytes, do buffer *pbOutput.*

</dd> <dt>

*ppEnumState* \[ in, out\]
</dt> <dd>

O endereço de um **ponteiro VOID** que recebe informações de estado de enumeração que são usadas em chamadas subsequentes para essa função. Essas informações só têm significado para o provedor SSL e são opacas para o chamador. O provedor SSL usa essas informações para determinar qual item é o próximo na enumeração. Se a variável apontada por esse parâmetro contiver **NULL,** a enumeração será iniciada desde o início.

O chamador da função deve liberar essa memória chamando a [**função SslFreeBuffer.**](sslfreebuffer.md)

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
| <dl> <dt>**NTE \_ PARÂMETRO \_ INVÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | Um dos parâmetros fornecidos não é válido.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

