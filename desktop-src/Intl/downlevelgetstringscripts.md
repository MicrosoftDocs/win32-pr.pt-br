---
description: Fornece uma lista de scripts usados na cadeia de caracteres Unicode especificada.
ms.assetid: 3ad23613-8d0c-432a-b352-637c373a0980
title: Função DownlevelGetStringScripts (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetStringScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: bc5a9fdaf3beb9e1c401943f923fa48bd9d4b44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105792510"
---
# <a name="downlevelgetstringscripts-function"></a>Função DownlevelGetStringScripts

Fornece uma lista de scripts usados na cadeia de caracteres Unicode especificada.

> [!Note]  
> Essa função é usada somente por aplicativos que são executados em sistemas operacionais anteriores ao Windows Vista. Seu uso requer o pacote de download. Os aplicativos que só são executados no Windows Vista e posterior devem chamar [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).

 

## <a name="syntax"></a>Sintaxe


```C++
int DownlevelGetStringScripts(
  _In_  DWORD   dwFlags,
  _In_  LPCWSTR lpString,
  _In_  int     cchString,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Sinalizadores que especificam opções para recuperação de script.



| Valor                                                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GSS_ALLOW_INHERITED_COMMON"></span><span id="gss_allow_inherited_common"></span><dl> <dt>**GSS \_ permitir \_ herdado \_ comum**</dt> </dl> | Recupere as informações de script "Qaii" (HERDAdo) e "Zyyy" (comum). Esse valor não afeta o processamento de caracteres não atribuídos. Esses caracteres na cadeia de caracteres de entrada sempre fazem com que um "ZZZZ" (script não atribuído) apareça na cadeia de caracteres do script.<br/> |



 

> [!Note]  
> Por padrão, essa função ignora todos os caracteres herdados ou comuns na cadeia de caracteres Unicode de entrada. Se GSS \_ permitir \_ herdado \_ comum não estiver definido, nem "Qaii" nem "Zyyy" aparecerão na cadeia de caracteres de script, mesmo que a cadeia de caracteres de entrada contenha esses caracteres. Se GSS \_ permitir \_ herdado \_ comum estiver definido, e se a cadeia de caracteres de entrada contiver caracteres herdados e/ou comuns, "Qaii" e/ou "Zyyy" aparecerão na cadeia de caracteres do script. Consulte a seção Comentários.

 

</dd> <dt>

*LPSTR* \[ no\]
</dt> <dd>

Ponteiro para a cadeia de caracteres Unicode a ser analisado.

</dd> <dt>

*cchString* \[ no\]
</dt> <dd>

Tamanho, em caracteres, da cadeia de caracteres Unicode indicada por *LPSTR*. O aplicativo definirá esse parâmetro como-1 se a cadeia de caracteres for terminada em nulo. Se o aplicativo definir esse parâmetro como 0, a função recuperará uma cadeia de caracteres Unicode nula (L " \\ 0") em *lpScripts* e retornará 1.

</dd> <dt>

*lpScripts* \[ fora\]
</dt> <dd>

Ponteiro para um buffer no qual essa função recupera uma cadeia de caracteres terminada em nulo que representa uma lista de scripts, usando a notação de 4 caracteres usada no [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html). Cada nome de script consiste em quatro caracteres latinos, e os nomes são recuperados em ordem alfabética. Cada nome, incluindo o último, é seguido por um ponto-e-vírgula.

Como alternativa, esse parâmetro pode conter **NULL** se *cchScripts* definido como 0. Nesse caso, a função retorna o tamanho necessário para o buffer de script.

</dd> <dt>

*cchScripts* \[ no\]
</dt> <dd>

Tamanho, em caracteres, para o buffer de script indicado por *lpScripts*.

Como alternativa, o aplicativo pode definir esse parâmetro como 0. Nesse caso, a função recupera **NULL** em *lpScripts* e retorna o tamanho necessário para o buffer de script.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número de caracteres recuperados no buffer de saída, incluindo um caractere nulo de terminação, se bem-sucedido e *cchScripts* é definido como um valor diferente de zero. A função retorna 1 para indicar que nenhum script foi encontrado, por exemplo, quando a cadeia de caracteres de entrada contém apenas caracteres comuns ou HERDAdos e GSS \_ permitir \_ herdado \_ comum não está definido. Considerando que cada script encontrado adiciona cinco caracteres (quatro caracteres + delimitador), uma operação matemática simples fornece a contagem de script como ( \_ código de retorno-1)/5.

Se a função for bem sucedido e o valor de *cchScripts* for 0, o valor de retorno será o tamanho necessário, em caracteres, incluindo um caractere nulo de terminação, para o buffer de script. A contagem de script é conforme descrito acima.

A função retornará 0 se não tiver sucesso. Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:

-   ERRO \_ BADDB. A função não pôde acessar os dados. Essa situação normalmente não deve ocorrer e, normalmente, indica uma instalação inválida, um problema de disco ou assim por diante.
-   ERRO \_ de \_ buffer insuficiente. Um tamanho de buffer fornecido não era grande o suficiente ou foi definido incorretamente como **nulo**.
-   ERROS de \_ Sinalizadores inválidos \_ . Os valores fornecidos para sinalizadores não eram válidos.
-   \_parâmetro inválido de erro \_ . Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

Essa função é útil como parte de uma estratégia para atenuar problemas de segurança relacionados a [IDNs (nomes de domínio internacionalizados)](handling-internationalized-domain-names--idns.md).

A determinação do script é baseada nos valores de script publicados pelo consórcio Unicode no <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt> , exceto pelo fato de que os caracteres não atribuídos têm o valor "ZZZZ" (não atribuído) em vez de "Zyyy" (comum).

Aqui estão alguns exemplos do comportamento dessa função:



Cadeia de caracteres de entrada

*dwFlags*

*lpScripts*

Scripts

Microsoft.com

0

Latn

Latim

Microsoft.com

GSS \_ permitir \_ herdado \_ comum

Latn Zyyy;

Latino + comum

$ {ROWSPAN2} $Ni ño $ {remover} $  

004E 0069 0241 006F

$ {ROWSPAN2} $GSS \_ permitir \_ herdado \_ $ {Remove} $  

$ {ROWSPAN2} $Latn; $ {remover} $  

$ {ROWSPAN2} $Latin $ {remover} $  

Usa letra latina minúscula N com til

$ {ROWSPAN2} $Ni ño $ {remover} $  

004E 0069 006E 0303 006F

$ {ROWSPAN2} $GSS \_ permitir \_ herdado \_ $ {Remove} $  

$ {ROWSPAN2} $Latn; Qaii; $ {REMOVE} $  

$ {ROWSPAN2} $Latin + herdado $ {REMOVE} $  

Usa til COMBINÁvel

$ {ROWSPAN2} $Sp ооf $ {remover} $  

0053 0070 043e 043e 0066

$ {ROWSPAN2} $0 $ {REMOVER} $  

$ {ROWSPAN2} $Latn; Cyrl; $ {REMOVE} $  

$ {ROWSPAN2} $Latin + cirílico $ {remover} $  

Usa letra CIRÍLICA minúscula O



U + F000

0

Zzzz;

Não atribuído



U + F000

GSS \_ permitir \_ herdado \_ comum

Zzzz;

Não atribuído



 

O arquivo de cabeçalho e a DLL necessários fazem parte do download ["APIs de mitigação do IDN (Microsoft Internacionalizated Domain Name)"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) , disponível no [centro de download do MSDN](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                                                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                                                                        |
| Redistribuível<br/>          | APIs de mitigação do IDN (Microsoft internacionalizated Domain Name) no Windows XP (SP2 ou posterior), Windows Server 2003 (SP1 ou posterior) ou Windows Vista<br/> |
| parâmetro<br/>                   | <dl> <dt>Idndl. h</dt> </dl>                                                                          |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                                        |



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

[**DownlevelVerifyScripts**](downlevelverifyscripts.md)
</dt> <dt>

[**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)
</dt> </dl>

 

 
