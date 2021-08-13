---
description: Recupera o valor de uma propriedade nomeada para um objeto de chave protocolo SSL protocolo SSL.
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: Função SslGetKeyProperty (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetKeyProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: b86f8a2e76573122bcfcf809d5301bc6bf70690467527f4dc69a5ec12419f56b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906114"
---
# <a name="sslgetkeyproperty-function"></a>Função SslGetKeyProperty

A **função SslGetKeyProperty** recupera o valor de uma propriedade nomeada para um objeto de chave de provedor SSL [*(protocolo*](/windows/desktop/SecGloss/s-gly) protocolo SSL).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslGetKeyProperty(
  _In_  NCRYPT_KEY_HANDLE hKey,
  _In_  LPCWSTR           pszProperty,
  _Out_ PBYTE             ppbOutput,
  _Out_ DWORD             *pcbOutput,
  _In_  DWORD             dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hKey* \[ Em\]
</dt> <dd>

O handle do provedor SSL.

</dd> <dt>

*pszProperty* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o nome da propriedade a ser recuperada. Esse pode ser um dos Identificadores de Propriedade Armazenamento [**Chave**](key-storage-property-identifiers.md) predefinidos ou um identificador de propriedade personalizado.

</dd> <dt>

*ppbOutput* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe o valor da propriedade. O chamador da função deve liberar esse buffer chamando a [**função SslFreeBuffer.**](sslfreebuffer.md)

</dd> <dt>

*pcbOutput* \[ out\]
</dt> <dd>

O tamanho, em bytes, do buffer *pbOutput.*

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferentes de zero.

Os possíveis códigos de retorno incluem, mas não estão limitados a, o seguinte.



| Valor/código de retorno                                                                                                                                                       | Descrição                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ INVÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | Um dos alças fornecidos não é válido.<br/>    |
| <dl> <dt>**NTE \_ PARÂMETRO \_ INVÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | Um dos parâmetros fornecidos não é válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

