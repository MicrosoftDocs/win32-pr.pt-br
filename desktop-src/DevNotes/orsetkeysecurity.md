---
description: Define a segurança de uma chave do registro aberta em um hive do registro offline.
ms.assetid: 002866bb-1532-41ad-a4db-a32d6e1c0a6a
title: Função ORSetKeySecurity (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ff63a7d896964f486b5fcb168c08513f8d5703be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769137"
---
# <a name="orsetkeysecurity-function"></a>Função ORSetKeySecurity

Define a segurança de uma chave do registro aberta em um hive do registro offline.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ORSetKeySecurity(
  _In_ ORHKEY               Handle,
  _In_ SECURITY_INFORMATION SecurityInformation,
  _In_ PSECURITY_DESCRIPTOR pSecurityDescriptor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Identificador* \[ do no\]
</dt> <dd>

Um identificador para uma chave do registro aberta em um hive do registro offline.

</dd> <dt>

*SecurityInformation* \[ no\]
</dt> <dd>

Sinalizadores de bits que indicam o tipo de informações de segurança a serem definidas. Esse parâmetro pode ser uma combinação dos sinalizadores de bit de [ \_ informações de segurança](../secauthz/security-information.md) .

</dd> <dt>

*pSecurityDescriptor* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [ \_ descritor de segurança](/windows/win32/api/winnt/ns-winnt-security_descriptor) que especifica os atributos de segurança a serem definidos para a chave especificada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, a função retornará êxito de erro \_ .

Se a função falhar, ela retornará um código de erro diferente de zero definido em Winerror. h. Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Biblioteca de registro offline do Windows versão 1,0 ou posterior<br/>                      |
| parâmetro<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORGetKeySecurity**](orgetkeysecurity.md)
</dt> <dt>

[\_descritor de segurança](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[informações de segurança \_](../secauthz/security-information.md)
</dt> </dl>

 

 
