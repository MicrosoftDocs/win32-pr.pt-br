---
description: Carrega o arquivo do hive do registro especificado na memória e valida o hive.
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: Função OROpenHive (Offreg. h)
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
ms.openlocfilehash: ba6531e7a2ab2b0b148065d9f4666812e75f2968
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749409"
---
# <a name="oropenhive-function"></a>Função OROpenHive

Carrega o arquivo do hive do registro especificado na memória e valida o hive.

## <a name="syntax"></a>Sintaxe


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpHivePath* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode que especifica o nome do arquivo do hive do registro a ser carregado na memória. Pode ser um arquivo de Hive que foi salvo com a função [**ORSaveHive**](orsavehive.md) ou criado com a função [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) ou [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) . O arquivo deve ter menos de 4 GB de tamanho e o chamador deve ter acesso de \_ dados de leitura de arquivo \_ ao arquivo. Para obter mais informações, consulte [segurança de arquivos e direitos de acesso](../fileio/file-security-and-access-rights.md).

</dd> <dt>

*phkResult* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe um identificador para a chave raiz do hive do registro offline carregado. Se o arquivo do hive do registro não puder ser aberto ou a validação falhar, a função definirá esse parâmetro como **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h. Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro. Os códigos de erro possíveis incluem o seguinte:

-   Se o arquivo estiver vazio ou tiver mais de 4 GB de tamanho, a função retornará o erro \_ BADDB.
-   Se o chamador não tiver os direitos de acesso necessários para abrir o arquivo, a função retornará o \_ acesso ao erro \_ negado.
-   Se o hive do registro falhar na validação, a função retornará um erro \_ não \_ arquivo de registro \_ .

## <a name="remarks"></a>Comentários

A função **OROpenHive** é a única função de registro offline que valida um hive do registro. Se a validação falhar, nenhuma tentativa será feita para reparar o hive.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Biblioteca de registro offline do Windows versão 1,0 ou posterior<br/>                      |
| parâmetro<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
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

 

 
