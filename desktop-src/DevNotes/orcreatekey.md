---
description: Cria a chave do Registro especificada em um hive do Registro offline. Se a chave já existir, a função a abrirá.
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: Função ORCreateKey (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b7ea5a365a9c5bdcb478ce47443a713ed5bc091666b54de880dc478708e4c36c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749685"
---
# <a name="orcreatekey-function"></a>Função ORCreateKey

Cria a chave do Registro especificada em um hive do Registro offline. Se a chave já existir, a função a abrirá.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ORCreateKey(
  _In_      ORHKEY               Handle,
  _In_      PCWSTR               lpSubKey,
  _In_opt_  PWSTR                lpClass,
  _In_opt_  DWORD                dwOptions,
  _In_opt_  PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Out_     PORHKEY              phkResult,
  _Out_opt_ PDWORD               pdwDisposition
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Manipular* \[ Em\]
</dt> <dd>

Um handle para uma chave aberta do Registro em um hive de registro offline.

</dd> <dt>

*lpSubKey* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode que contém o nome de uma sub-chave que essa função abre ou cria. O *parâmetro lpSubKey* deve especificar uma sub-chave da chave identificada pelo *parâmetro Handle;* ele pode ter até 32 níveis de profundidade na árvore do Registro. Para obter mais informações sobre nomes de chave, [consulte Estrutura do Registro](../sysinfo/structure-of-the-registry.md).

Esse parâmetro não pode ser **NULL.**

Os nomes de chave não são sensíveis a minúsculas.

</dd> <dt>

*lpClass* \[ in, opcional\]
</dt> <dd>

A classe (tipo de objeto) dessa chave. Esse parâmetro pode ser ignorado. Este parâmetro pode ser **NULL**.

</dd> <dt>

*dwOptions* \[ in, opcional\]
</dt> <dd>

Esse parâmetro pode ser 0 ou um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <dt>**REG \_ OPTION \_ CREATE \_ LINK**</dt> <dt>0x00000002L</dt> </dl>    | A chave é um link simbólico. O caminho de destino é atribuído ao valor L"SymbolicLinkValue" da chave. O caminho de destino deve ser um caminho absoluto do Registro. Se essa opção for definida, **REG \_ OPTION NON \_ \_ VOLATILE** também deverá ser definido. <br/> Se o *parâmetro lpSubKey* especificar uma chave existente, ele deverá ter sido criado com **REG OPTION CREATE \_ \_ \_ LINK**.<br/> Os links simbólicos do Registro devem ser usados somente quando absolutamente necessários para a compatibilidade do aplicativo. <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <dt>**REG \_ OPTION \_ NON \_ VOLATILE**</dt> <dt>0x0000000L</dt> </dl> | A chave não é volátil; esse é o padrão. As informações são armazenadas em um arquivo e preservadas quando o sistema é reiniciado. A [**função ORSaveHive**](orsavehive.md) salva chaves que não são voláteis.<br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pSecurityDescriptor* \[ in, opcional\]
</dt> <dd>

Um ponteiro para uma [estrutura \_ SECURITY DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor) que contém um descritor de segurança para a nova chave. Se *pSecurityDescriptor* for **NULL,** a chave obtém um descritor de segurança padrão. As ACLs em um descritor de segurança padrão para uma chave são herdadas de sua chave pai direta.

</dd> <dt>

*phkResult* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe um ponteiro para a chave aberta ou criada. Use a [**função ORCloseKey**](orclosekey.md) para fechar a chave depois de terminar de usar o handle.

</dd> <dt>

*pdwDisposition* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que recebe um dos valores de disposição a seguir.



| Valor                                                                                                                                                                                                                                                          | Significado                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <dt>**REG \_ CRIADO \_ NOVA \_ CHAVE**</dt> <dt>0x00000001L</dt> </dl>             | A chave não existia e foi criada.<br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <dt>**REG \_ CHAVE \_ EXISTENTE \_ ABERTA**</dt> <dt>0x00000002L</dt> </dl> | A chave existia e foi simplesmente aberta sem ser alterada.<br/> |



 

Se *pdwDisposition* for **NULL,** nenhuma informação de disposição será retornada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS.

Se a função falhar, o valor de retorno será um código de erro não zero definido em Winerror.h. Você pode usar a [função FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com o sinalizador FORMAT MESSAGE FROM SYSTEM para obter \_ uma \_ \_ descrição genérica do erro.

Se o parâmetro *dwOptions* for definido com **REG OPTION CREATE \_ \_ \_ LINK,** mas **REG OPTION NON \_ \_ \_ VOLATILE** estiver claro ou se o handle a ser retornado for um alçador para a chave raiz do hive, a função retornará ERROR \_ INVALID \_ PARAMETER.

## <a name="remarks"></a>Comentários

A chave que a **função ORCreateKey** cria não tem valores. Um aplicativo pode usar a [**função ORSetValue**](orsetvalue.md) para definir valores de chave.

A **função ORCreateKey** não pode ser usada para criar a chave raiz em um hive do Registro offline. Use a [**função ORCreateHive**](orcreatehive.md) para criar a chave raiz e obter um handle para a chave.

O registro offline não dá suporte ao salvar chaves individuais. Use a [**função ORSaveHive**](orsavehive.md) para salvar uma chave e suas sub-chaves em um hive.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Windows Biblioteca de Registro offline versão 1.0 ou posterior<br/>                      |
| Cabeçalho<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORCreateHive**](orcreatehive.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[DESCRITOR \_ DE SEGURANÇA](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 
