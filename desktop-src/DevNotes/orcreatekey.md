---
description: Cria a chave do Registro especificada em um hive do registro offline. Se a chave já existir, a função a abrirá.
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: Função ORCreateKey (Offreg. h)
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
ms.openlocfilehash: 9a14198cb6f1912612a092e003a68fd9ff49f867
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755276"
---
# <a name="orcreatekey-function"></a>Função ORCreateKey

Cria a chave do Registro especificada em um hive do registro offline. Se a chave já existir, a função a abrirá.

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

*Identificador* \[ do no\]
</dt> <dd>

Um identificador para uma chave do registro aberta em um hive do registro offline.

</dd> <dt>

*lpSubKey* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode que contém o nome de uma subchave que essa função abre ou cria. O parâmetro *lpSubKey* deve especificar uma subchave da chave identificada pelo parâmetro *Handle* ; pode ter até 32 níveis de profundidade na árvore do registro. Para obter mais informações sobre nomes de chave, consulte [estrutura do registro](../sysinfo/structure-of-the-registry.md).

Este parâmetro não pode ser **nulo**.

Os nomes de chave não diferenciam maiúsculas de minúsculas.

</dd> <dt>

*lpClass* \[ em, opcional\]
</dt> <dd>

A classe (tipo de objeto) dessa chave. Esse parâmetro pode ser ignorado. Este parâmetro pode ser **NULL**.

</dd> <dt>

*dwOptions* \[ em, opcional\]
</dt> <dd>

Esse parâmetro pode ser 0 ou um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <dt>**Reg \_ OPÇÃO \_ Create \_ link**</dt> <dt>0x00000002L</dt> </dl>    | A chave é um link simbólico. O caminho de destino é atribuído ao valor de L "SymbolicLinkValue" da chave. O caminho de destino deve ser um caminho de registro absoluto. Se essa opção for definida, **a \_ opção reg \_ não \_ volátil** também deverá ser definida. <br/> Se o parâmetro *lpSubKey* especificar uma chave existente, ele deverá ter sido criado com **a \_ opção reg \_ Create \_ link**.<br/> Os links simbólicos do registro devem ser usados somente quando absolutamente necessário para compatibilidade de aplicativos. <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <dt>**Reg \_ OPÇÃO \_ não \_ volátil**</dt> <dt>0x00000000</dt> </dl> | A chave não é volátil; Esse é o padrão. As informações são armazenadas em um arquivo e são preservadas quando o sistema é reiniciado. A função [**ORSaveHive**](orsavehive.md) salva as chaves que não são voláteis.<br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pSecurityDescriptor* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura de [ \_ descritor de segurança](/windows/win32/api/winnt/ns-winnt-security_descriptor) que contém um descritor de segurança para a nova chave. Se *pSecurityDescriptor* for **NULL**, a chave obterá um descritor de segurança padrão. As ACLs em um descritor de segurança padrão para uma chave são herdadas de sua chave pai direta.

</dd> <dt>

*phkResult* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe um identificador para a chave aberta ou criada. Use a função [**ORCloseKey**](orclosekey.md) para fechar a chave depois de terminar de usar o identificador.

</dd> <dt>

*pdwDisposition* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que recebe um dos seguintes valores de disposição.



| Valor                                                                                                                                                                                                                                                          | Significado                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <dt>**Reg \_ \_Nova \_ chave criada**</dt> em <dt>0x00000001</dt> </dl>             | A chave não existia e foi criada.<br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <dt>**Reg \_ 0x00000002L \_ de \_ chave existente aberta**</dt> <dt></dt> </dl> | A chave existia e foi simplesmente aberta sem ser alterada.<br/> |



 

Se *pdwDisposition* for **NULL**, nenhuma informação de disposição será retornada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h. Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.

Se o parâmetro *dwOptions* for definido com **a \_ opção reg \_ criar \_ link** , mas a **opção reg \_ \_ não \_ volátil** estiver clara, ou se o identificador a ser retornado for um identificador para a chave raiz do hive, a função retornará um parâmetro de erro \_ inválido \_ .

## <a name="remarks"></a>Comentários

A chave que a função **ORCreateKey** cria não tem nenhum valor. Um aplicativo pode usar a função [**ORSetValue**](orsetvalue.md) para definir valores de chave.

A função **ORCreateKey** não pode ser usada para criar a chave raiz em um hive de registro offline. Use a função [**ORCreateHive**](orcreatehive.md) para criar a chave raiz e obter um identificador para a chave.

O registro offline não oferece suporte ao salvamento de chaves individuais. Use a função [**ORSaveHive**](orsavehive.md) para salvar uma chave e suas subchaves em um Hive.

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

[**ORCreateHive**](orcreatehive.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[\_descritor de segurança](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 
