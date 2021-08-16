---
description: Compara duas cadeias de caracteres Unicode, usando uma localidade especificada.
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: Função CompareStringWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 9fe05c354aaa901d87c77ba04eecd5dc4efd925d77bdeaf5387a137d85b27348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861507"
---
# <a name="comparestringwrapw-function"></a>Função CompareStringWrapW

\[o **CompareStringWrapW** está disponível para uso no Windows XP. Ele não estará disponível nas versões subsequentes. Você deve usar [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) em seu lugar.\]

Compara duas cadeias de caracteres Unicode, usando uma localidade especificada.

> [!Note]  
> **CompareStringWrapW** é um wrapper para a função **CompareStringW** . Consulte a página [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) para ver mais observações de uso.

 

## <a name="syntax"></a>Sintaxe


```C++
int CompareStringWrapW(
  _In_ LCID    Locale,
  _In_ DWORD   dwCmpFlags,
  _In_ LPCWSTR lpString1,
  _In_ int     cchCount1,
  _In_ LPCWSTR lpString2,
  _In_ int     cchCount2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Localidade* \[ do no\]
</dt> <dd>

Tipo: **LCID**

Um identificador de localidade usado para a comparação. Esse parâmetro pode ser um dos seguintes identificadores de localidade predefinidos ou um identificador de localidade criado pela macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) .

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**\_padrão do sistema de localidade \_**


</dt> <dd>

A localidade padrão do sistema.

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_padrão de usuário de localidade \_**


</dt> <dd>

A localidade padrão do usuário atual.

</dd> </dl> </dd> <dt>

*dwCmpFlags* \[ no\]
</dt> <dd>

Tipo: **DWORD**

Os sinalizadores que indicam como a função compara as duas cadeias de caracteres. Por padrão, esses sinalizadores não são definidos. Defina como zero para obter o comportamento padrão ou para qualquer combinação dos valores a seguir.

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**IGNORECASE de normal \_**


</dt> <dd>

Ignorar maiúsculas e minúsculas.

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**\_IGNOREKANATYPE normal**


</dt> <dd>

Não diferenciar entre caracteres hiragana e Katakana. Os caracteres hiragana e katakana correspondentes são comparados como iguais.

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**\_IGNORENONSPACE normal**


</dt> <dd>

Ignorar caracteres de não espaçamento.

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**\_IGNORESYMBOLS normal**


</dt> <dd>

Ignorar símbolos.

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**\_IGNOREWIDTH normal**


</dt> <dd>

Não Diferencie entre um caractere de byte único e o mesmo caractere como um caractere de byte duplo.

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**CLASSIFICAR \_ STRINGSORT**


</dt> <dd>

Trate a pontuação da mesma forma que os símbolos.

</dd> </dl> </dd> <dt>

*lpString1* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para a primeira cadeia de caracteres Unicode a ser comparada.

</dd> <dt>

*cchCount1* \[ no\]
</dt> <dd>

Tipo: **int**

O número de caracteres na cadeia de caracteres apontada pelo parâmetro *lpString1* . A contagem não inclui o caractere nulo de terminação. Se esse parâmetro for um valor negativo, a cadeia de caracteres será considerada como terminada em nulo e o comprimento será calculado automaticamente.

</dd> <dt>

*lpString2* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para a segunda cadeia de caracteres Unicode a ser comparada.

</dd> <dt>

*cchCount2* \[ no\]
</dt> <dd>

Tipo: **int**

O número de caracteres na cadeia de caracteres apontada pelo parâmetro *lpString2* . A contagem não inclui o caractere nulo de terminação. Se esse parâmetro for um valor negativo, a cadeia de caracteres será considerada como terminada em nulo e o comprimento será calculado automaticamente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **int**

Se a função falhar, o valor retornado será zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** pode retornar um dos seguintes códigos de erro.

-   \_Sinalizadores inválidos de erro \_
-   \_parâmetro inválido de erro \_

Se a função for realizada com sucesso, o valor de retorno será um dos valores a seguir. 

| Requisito | Valor |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| CSTR \_ menor \_ que    | A cadeia de caracteres apontada pelo parâmetro *lpString1* é menos no valor léxico do que a cadeia de caracteres apontada pelo parâmetro *lpString2* . |
| CSTR \_ igual         | A cadeia de caracteres apontada por *lpString1* é igual no valor léxico à cadeia de caracteres apontada por *lpString2*.                              |
| CSTR \_ maior \_ que | A cadeia de caracteres apontada por *lpString1* é maior no valor léxico do que a cadeia de caracteres apontada por *lpString2*                           |



 

## <a name="remarks"></a>Comentários

**Aviso de segurança:** Usar essa função incorretamente pode comprometer a segurança do seu aplicativo. As cadeias de caracteres que não são comparadas corretamente podem produzir entradas inválidas. Testar cadeias de caracteres para certificar-se de que elas são válidas antes de usá-las e fornecer manipuladores de erro. Para obter mais informações, consulte [considerações de segurança: recursos internacionais](../intl/security-considerations--international-features.md)

O método preferencial é usar [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) em conjunto com a camada Microsoft para Unicode (MSLU).

**CompareStringWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 45.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Nenhum</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 
