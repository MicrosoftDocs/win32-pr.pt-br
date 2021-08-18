---
description: Fornece uma lista de scripts para a localidade especificada.
ms.assetid: 0cedcf6c-bab4-4e0f-ab8f-04aa8e51602f
title: Função DownlevelGetLocaleScripts (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetLocaleScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: 02631a605f67f3c27dfcc29c1e660ca24e56b6072d4490ba8ba090ebdd8b9019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068246"
---
# <a name="downlevelgetlocalescripts-function"></a>Função DownlevelGetLocaleScripts

Fornece uma lista de scripts para a localidade especificada.

> [!Note]  
> essa função é usada somente por aplicativos que são executados em sistemas operacionais anteriores ao Windows Vista. Seu uso requer o pacote de download. os aplicativos que só são executados no Windows Vista e posterior devem chamar [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) com *LCType* definido como [localidade \_ SSCRIPTS](locale-sscripts.md).

 

## <a name="syntax"></a>Sintaxe


```C++
int DownlevelGetLocaleScripts(
  _In_  LPCWSTR lpLocaleName,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpLocaleName* \[ no\]
</dt> <dd>

Ponteiro para um [nome de localidade](locale-names.md)terminada em nulo.

</dd> <dt>

*lpScripts* \[ fora\]
</dt> <dd>

Ponteiro para um buffer no qual essa função recupera uma cadeia de caracteres terminada em nulo que representa uma lista de scripts, usando a notação de 4 caracteres usada no [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html). Cada nome de script consiste em quatro caracteres latinos, e os nomes são recuperados em ordem alfabética. Cada um deles, incluindo o último, é seguido por um ponto-e-vírgula.

Como alternativa, esse parâmetro pode conter **NULL** se *cchScripts* for definido como 0. Nesse caso, a função retorna o tamanho necessário para o buffer de script.

</dd> <dt>

*cchScripts* \[ no\]
</dt> <dd>

Tamanho, em caracteres, para o buffer de script indicado por *lpScripts*.

Como alternativa, o aplicativo pode definir esse parâmetro como 0. Nesse caso, a função recupera **NULL** em *lpScripts* e retorna o tamanho necessário para o buffer de script.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o número de caracteres recuperados no buffer de script, incluindo o caractere nulo de terminação. Se a função for bem sucedido e o valor de *cchScripts* for 0, o valor de retorno será o tamanho necessário, em caracteres, incluindo um caractere nulo de terminação, para o buffer de script.

Essa função retornará 0 se não tiver sucesso. Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:

-   ERRO \_ BADDB. A função não pôde acessar os dados. Essa situação normalmente não deve ocorrer e, normalmente, indica uma instalação inválida, um problema de disco ou assim por diante.
-   ERRO \_ de \_ buffer insuficiente. Um tamanho de buffer fornecido não era grande o suficiente ou foi definido incorretamente como **nulo**.
-   \_parâmetro inválido de erro \_ . Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

Essa função é útil como parte de uma estratégia para atenuar problemas de segurança relacionados a [IDNs (nomes de domínio internacionalizados)](handling-internationalized-domain-names--idns.md).

Aqui estão alguns exemplos de entradas e saídas para essa função, supondo um tamanho de buffer suficiente:



| Local                  | *lpLocaleName* | *lpScripts*     |
|-------------------------|----------------|-----------------|
| Inglês (Estados Unidos) | pt-BR          | Latn           |
| Híndi (Índia)           | hi-IN          | DESVPADPA           |
| Japonês (Japão)        | ja-JP          | Hani; Hira; Kana |



 

A lista não contém o script latino, a menos que seja uma parte essencial do sistema de escrita usado para uma localidade. No entanto, os caracteres latinos são geralmente usados no contexto de localidades para os quais não são nativos, como para um nome comercial estrangeiro. No exemplo acima para Hindi na Índia, o único script recuperado é "DESVPADA" (para o Devanágari), embora os caracteres latinos também possam aparecer em texto em Híndi. A função [**DownlevelVerifyScripts**](downlevelverifyscripts.md) tem um sinalizador especial para resolver esse caso.

O arquivo de cabeçalho e a DLL necessários fazem parte do download ["APIs de mitigação do IDN (Microsoft Internacionalizated Domain Name)"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , disponível no [centro de download do MSDN](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                                                                                                 |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                                                                        |
| Redistribuível<br/>          | APIs de mitigação do IDN (Microsoft internacionalizated Domain Name) no Windows XP (SP2 ou posterior), Windows Server 2003 (SP1 ou posterior) ou Windows Vista<br/> |
| Cabeçalho<br/>                   | <dl> <dt>Idndl. h</dt> </dl>                                                                          |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao idioma nacional](national-language-support.md)
</dt> <dt>

[Funções de suporte ao idioma nacional](national-language-support-functions.md)
</dt> <dt>

[Tratando IDNs (nomes de domínio internacionalizados)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**DownlevelVerifyScripts**](downlevelverifyscripts.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
