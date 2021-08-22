---
description: Carrega o arquivo hive do Registro especificado na memória e valida o hive.
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: Função OROpenHive (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 86ff3d6ff15b030054d40ca7131e521cedb59ebf20c4942951f0e141f27a2840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076010"
---
# <a name="oropenhive-function"></a>Função OROpenHive

Carrega o arquivo hive do Registro especificado na memória e valida o hive.

## <a name="syntax"></a>Sintaxe


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpHivePath* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode que especifica o nome do arquivo hive do Registro a ser carregado na memória. Pode ser um arquivo hive que foi salvo com a [**função ORSaveHive**](orsavehive.md) ou criado com a [função RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) ou [RegSaveKeyEx.](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) O arquivo deve ter menos de 4 GB de tamanho e o chamador deve ter acesso a DADOS DE LEITURA DE ARQUIVO \_ \_ ao arquivo. Para obter mais informações, consulte [Segurança de arquivos e direitos de acesso](../fileio/file-security-and-access-rights.md).

</dd> <dt>

*phkResult* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe um handle para a chave raiz do hive do registro offline carregado. Se o arquivo hive do Registro não puder ser aberto ou a validação falhar, a função define esse parâmetro como **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS.

Se a função falhar, o valor de retorno será um código de erro não zero definido em Winerror.h. Você pode usar a [função FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com o sinalizador FORMAT MESSAGE FROM SYSTEM para obter \_ uma \_ \_ descrição genérica do erro. Os códigos de erro possíveis incluem o seguinte:

-   Se o arquivo estiver vazio ou tiver mais de 4 GB de tamanho, a função retornará ERROR \_ BADDB.
-   Se o chamador não tiver os direitos de acesso necessários para abrir o arquivo, a função retornará ERROR \_ ACCESS \_ DENIED.
-   Se o hive do Registro falhar na validação, a função retornará ERROR \_ NOT \_ REGISTRY \_ FILE.

## <a name="remarks"></a>Comentários

A **função OROpenHive** é a única função de registro offline que valida um hive do Registro. Se a validação falhar, nenhuma tentativa será feita para reparar o hive.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Windows Biblioteca de Registro offline versão 1.0 ou posterior<br/>                      |
| Cabeçalho<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**ORCreateHive**](orcreatehive.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya)
</dt> <dt>

[RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa)
</dt> </dl>

 

 
