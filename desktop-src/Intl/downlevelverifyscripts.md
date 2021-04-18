---
description: Compara duas listas enumeradas de scripts.
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: Função DownlevelVerifyScripts (idndl. h)
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
ms.openlocfilehash: 62e029576d53109e3c57faf4ec913472f8aea65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756916"
---
# <a name="downlevelverifyscripts-function"></a>Função DownlevelVerifyScripts

Compara duas listas enumeradas de scripts.

> [!Note]  
> Essa função é usada somente por aplicativos que são executados em sistemas operacionais anteriores ao Windows Vista. Seu uso requer o pacote de download. Os aplicativos que só são executados no Windows Vista e posterior devem chamar [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).

 

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

*dwFlags* \[ no\]
</dt> <dd>

Sinalizadores que especificam opções de verificação de script.



| Valor                                                                                                                                                             | Significado                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <dt>**VS \_ permitir \_ latino**</dt> </dl> | Permitir "Latn" (script latino) na lista de testes, mesmo se não estiver na lista de localidade.<br/> |



 

</dd> <dt>

*lpLocaleScripts* \[ no\]
</dt> <dd>

Aponta para a lista de localidade, a lista enumerada de scripts para uma determinada localidade. Normalmente, essa lista é preenchida chamando [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md).

</dd> <dt>

*cchLocaleScripts* \[ no\]
</dt> <dd>

Tamanho, em caracteres, da cadeia de caracteres indicada por *lpLocaleScripts*. O aplicativo definirá esse parâmetro como-1 se a cadeia de caracteres for terminada em nulo. Se esse parâmetro for definido como 0, a função falhará.

</dd> <dt>

*lpTestScripts* \[ no\]
</dt> <dd>

Ponteiro para a lista de testes, uma segunda lista enumerada de scripts. Normalmente, essa lista é preenchida chamando [**DownlevelGetStringScripts**](downlevelgetstringscripts.md).

</dd> <dt>

*cchTestScripts* \[ no\]
</dt> <dd>

Tamanho, em caracteres, da cadeia de caracteres indicada por *lpTestScripts*. O aplicativo definirá esse parâmetro como-1 se a cadeia de caracteres for terminada em nulo. Se esse parâmetro for definido como 0, a função falhará.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se a lista de testes não estiver vazia e todos os itens da lista também estiverem incluídos na lista de localidade. Caso contrário, a função retornará **false**.

Um valor de retorno **false** pode indicar que a lista de testes contém um item que não está na lista de localidade ou pode indicar um erro. Para distinguir entre esses dois casos, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). Se **DownlevelVerifyScripts** tiver determinado com êxito que há um item na lista de testes que não está na lista de localidade, **GetLastError** retornará o êxito do erro \_ . Caso contrário, **GetLastError** pode retornar um dos seguintes códigos de erro:

-   ERROS de \_ Sinalizadores inválidos \_ . Os valores fornecidos para sinalizadores não eram válidos.
-   \_parâmetro inválido de erro \_ . Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

Essa função compara Cadeias de caracteres, como "Latn; Cyrl; ", que consiste em uma série de nomes de script de 4 caracteres, com cada nome de script seguido por um ponto-e-vírgula. Ele também tem um caso especial para considerar o fato de que o script Latin é geralmente usado em linguagens e localidades para as quais não é nativo.

Essa função é útil como parte de uma estratégia para atenuar problemas de segurança relacionados a [IDNs (nomes de domínio internacionalizados)](handling-internationalized-domain-names--idns.md).

Veja a seguir exemplos do retorno dessa função e uma chamada subsequente para [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) em vários cenários. Os dois últimos exemplos ilustram, respectivamente, um caso em que a lista de testes não tem um ponto-e-vírgula de terminação (cadeia de caracteres malformada) e um caso em que a lista de testes está vazia.



| Cadeia de caracteres "locale" | Cadeia de caracteres de "teste" | *dwFlags*        | Retornar valor | Retorno de GetLastError       |
|-----------------|---------------|------------------|--------------|---------------------------|
| Hani; Hira; Kana | Hani;         | N/D              | **TRUE**     | N/D                       |
| Hani; Hira; Kana | Hani; Latn    | 0                | **FALSE**    | êxito do erro \_            |
| Hani; Hira; Kana | Hani; Latn    | VS \_ permitir \_ latino | **TRUE**     | N/D                       |
| Hani; Hira; Kana | Cyrl;         | N/D              | **FALSE**    | êxito do erro \_            |
| Hani; Hira; Kana | Cyrl;         | N/D              | **FALSE**    | \_parâmetro inválido de erro \_ |
| Hani; Hira; Kana |               | N/D              | **FALSE**    | êxito do erro \_            |



 

O arquivo de cabeçalho e a DLL necessários fazem parte do download ["APIs de mitigação do IDN (Microsoft Internacionalizated Domain Name)"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , disponível no [centro de download do MSDN](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                                                                  |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                                                         |
| Redistribuível<br/>          | APIs de mitigação do IDN (nome de domínio internacionalizado) da Microsoft no Windows XP com SP2, Windows Server 2003 com SP1, orWindows vista<br/> |
| parâmetro<br/>                   | <dl> <dt>Idndl. h</dt> </dl>                                                           |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao idioma nacional](national-language-support.md)
</dt> <dt>

[Funções de suporte ao idioma nacional](national-language-support-functions.md)
</dt> <dt>

[Tratando IDNs (nomes de domínio internacionalizados)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)
</dt> <dt>

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 
