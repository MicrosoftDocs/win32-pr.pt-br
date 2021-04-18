---
description: Recupera uma cópia do descritor de segurança protegendo a chave do registro aberta especificada em um hive do registro offline.
ms.assetid: 676d5be5-d9d8-48c6-848a-917d1a0474c6
title: Função ORGetKeySecurity (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 13594493af2e7992471d13dce30f0a848501c4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750131"
---
# <a name="orgetkeysecurity-function"></a>Função ORGetKeySecurity

Recupera uma cópia do descritor de segurança protegendo a chave do registro aberta especificada em um hive do registro offline.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ORGetKeySecurity(
  _In_      ORHKEY               Handle,
  _In_      SECURITY_INFORMATION SecurityInformation,
  _Out_opt_ PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Inout_   PDWORD               lpcbSecurityDescriptor
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

Um valor de [ \_ informações de segurança](../secauthz/security-information.md) que indica as informações de segurança solicitadas.

</dd> <dt>

*pSecurityDescriptor* \[ out, opcional\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma cópia do descritor de segurança solicitado. Este parâmetro pode ser **NULL**.

</dd> <dt>

*lpcbSecurityDescriptor* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma variável que especifica o tamanho, em bytes, do buffer apontado pelo parâmetro *pSecurityDescriptor* . Quando a função retorna, a variável contém o número de bytes gravados no buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, a função retornará êxito de erro \_ .

Se a função falhar, ela retornará um código de erro diferente de zero definido em Winerror. h. Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.

Se o buffer especificado pelo parâmetro *pSecurityDescriptor* for muito pequeno, a função retornará um \_ buffer insuficiente de erro \_ e o parâmetro *lpcbSecurityDescriptor* conterá o número de bytes necessários para o descritor de segurança solicitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Biblioteca de registro offline do Windows versão 1,0 ou posterior<br/>                      |
| parâmetro<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORSetKeySecurity**](orsetkeysecurity.md)
</dt> <dt>

[informações de segurança \_](../secauthz/security-information.md)
</dt> </dl>

 

 
