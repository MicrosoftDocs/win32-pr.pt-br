---
description: Recupera o valor de uma propriedade nomeada para um objeto de chave do provedor de protocolo SSL (protocolo SSL).
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: Função SslGetKeyProperty (Sslprovider. h)
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
ms.openlocfilehash: 42952b76bfb46eeeb31b9f76b1f677e7b3b8e3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753412"
---
# <a name="sslgetkeyproperty-function"></a>Função SslGetKeyProperty

A função **SslGetKeyProperty** recupera o valor de uma propriedade nomeada para um objeto de chave do provedor de protocolo SSL ( [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) ).

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

*HKEY* \[ no\]
</dt> <dd>

O identificador do provedor SSL.

</dd> <dt>

*pszProperty* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o nome da propriedade a ser recuperada. Pode ser um dos [**identificadores de propriedade de armazenamento de chave**](key-storage-property-identifiers.md) predefinidos ou um identificador de propriedade personalizada.

</dd> <dt>

*ppbOutput* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe o valor da propriedade. O chamador da função deve liberar esse buffer chamando a função [**SslFreeBuffer**](sslfreebuffer.md) .

</dd> <dt>

*pcbOutput* \[ fora\]
</dt> <dd>

O tamanho, em bytes, do buffer *pbOutput* .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                       | Descrição                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl>    | Um dos identificadores fornecidos não é válido.<br/>    |
| <dl> <dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt> </dl> | Um dos parâmetros fornecidos não é válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

