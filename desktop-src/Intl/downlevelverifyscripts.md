---
description: Compara duas listas enumeradas de scripts.
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: Função DownlevelVerifyScripts (Idndl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelVerifyScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: df0bdb1e8968d6bb044a3f270eb9200adf1ecaa54137fe3cface0e0898a9b5be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068236"
---
# <a name="downlevelverifyscripts-function"></a>Função DownlevelVerifyScripts

Compara duas listas enumeradas de scripts.

> [!Note]  
> Essa função é usada somente por aplicativos que são executados em sistemas operacionais Windows Vista pré-executados. Seu uso requer o pacote de download. Os aplicativos que são executados somente Windows Vista e posterior devem chamar [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL DownlevelVerifyScripts(
  _In_ DWORD   dwFlags,
  _In_ LPCWSTR lpLocaleScripts,
  _In_ int     cchLocaleScripts,
  _In_ LPCWSTR lpTestScripts,
  _In_ int     cchTestScripts
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Sinalizadores que especificam opções de verificação de script.



| Valor                                                                                                                                                             | Significado                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <dt>**VS \_ ALLOW \_ LATIN**</dt> </dl> | Permita "Latn" (script latino) na lista de testes, mesmo que não seja na lista de localidades.<br/> |



 

</dd> <dt>

*lpLocaleScripts* \[ Em\]
</dt> <dd>

Ponteiro para a lista de localidades, a lista enumerada de scripts para uma determinada localidade. Normalmente, essa lista é preenchida chamando [**DownlevelGetLocaleScripts.**](downlevelgetlocalescripts.md)

</dd> <dt>

*cchLocaleScripts* \[ Em\]
</dt> <dd>

Tamanho, em caracteres, da cadeia de caracteres indicada por *lpLocaleScripts.* O aplicativo define esse parâmetro como -1 se a cadeia de caracteres for terminada em nulo. Se esse parâmetro for definido como 0, a função falhará.

</dd> <dt>

*lpTestScripts* \[ Em\]
</dt> <dd>

Ponteiro para a lista de testes, uma segunda lista enumerada de scripts. Normalmente, essa lista é preenchida chamando [**DownlevelGetStringScripts.**](downlevelgetstringscripts.md)

</dd> <dt>

*cchTestScripts* \[ Em\]
</dt> <dd>

Tamanho, em caracteres, da cadeia de caracteres indicada por *lpTestScripts.* O aplicativo define esse parâmetro como -1 se a cadeia de caracteres for terminada em nulo. Se esse parâmetro for definido como 0, a função falhará.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se a lista de teste não estiver vazia e todos os itens na lista também serão incluídos na lista de localidades. Caso contrário, a função **retornará FALSE.**

Um valor de retorno **FALSE** pode indicar que a lista de testes contém um item que não está na lista de localidades ou pode indicar um erro. Para distinguir entre esses dois casos, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). Se **DownlevelVerifyScripts** tiver determinado com êxito que há um item na lista de testes que não está na lista de localidades, **GetLastError** retornará ERROR \_ SUCCESS. Caso contrário, **GetLastError** poderá retornar um dos seguintes códigos de erro:

-   ERRO \_ \_ SINALIZADORES INVÁLIDOS. Os valores fornecidos para sinalizadores não eram válidos.
-   ERRO \_ PARÂMETRO \_ INVÁLIDO. Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

Essa função compara cadeias de caracteres, como "Latn; Cyrl;", que consiste em uma série de nomes de script de 4 caracteres, com cada nome de script seguido por um ponto e vírgula. Ele também tem um caso especial para levar em conta o fato de que o script latino geralmente é usado em idiomas e localidades para os quais ele não é nativo.

Essa função é útil como parte de uma estratégia para atenuar problemas de segurança relacionados a [IDNs (nomes de domínio internacionalizados).](handling-internationalized-domain-names--idns.md)

A seguir estão exemplos do retorno dessa função e uma chamada subsequente para [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) em vários cenários. Os dois últimos exemplos ilustram, respectivamente, um caso em que a lista de testes não tem um ponto e vírgula de terminação (cadeia de caracteres malformada) e um caso em que a lista de testes está vazia.



| Cadeia de caracteres "Localidade" | Cadeia de caracteres "Test" | *dwFlags*        | Valor retornado | Retorno de GetLastError       |
|-----------------|---------------|------------------|--------------|---------------------------|
| Hani; Hira; Kana; | Hani;         | N/D              | **TRUE**     | N/D                       |
| Hani; Hira; Kana; | Hani; Latn;    | 0                | **FALSE**    | ÊXITO \_ DO ERRO            |
| Hani; Hira; Kana; | Hani; Latn;    | VS \_ ALLOW \_ LATIN | **TRUE**     | N/D                       |
| Hani; Hira; Kana; | Cyrl;         | N/D              | **FALSE**    | ÊXITO \_ DO ERRO            |
| Hani; Hira; Kana; | Cyrl;         | N/D              | **FALSE**    | ERRO \_ PARÂMETRO \_ INVÁLIDO |
| Hani; Hira; Kana; |               | N/D              | **FALSE**    | ÊXITO \_ DO ERRO            |



 

O arquivo de header necessário e a DLL fazem parte do download das APIs de Mitigação de ["IDN (Nome](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) de Domínio Internacionalizado) da Microsoft", disponível no Centro de Download do [MSDN.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                                                         |
| Redistribuível<br/>          | APIs de mitigação de IDN (Nome de Domínio Internacionalizado) da Microsoft noWindows XP com SP2,Windows Server 2003 com SP1 ouWindows Vista<br/> |
| Cabeçalho<br/>                   | <dl> <dt>Idndl.h</dt> </dl>                                                           |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte a idiomas nacionais](national-language-support.md)
</dt> <dt>

[Funções de suporte a idiomas nacionais](national-language-support-functions.md)
</dt> <dt>

[Manipulando IDNs (nomes de domínio internacionalizados)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)
</dt> <dt>

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 
