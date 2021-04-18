---
description: A chave do registro do EUDC contém uma ou mais subchaves contendo valores que definem as fontes associadas aos caracteres definidos pelo usuário final (EUDCs) para uma determinada página de código.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781f7c28460c2e56f4bcdb393277f509f88a0383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766889"
---
# <a name="eudc"></a>EUDC

A chave do registro do EUDC contém uma ou mais subchaves contendo valores que definem as fontes associadas aos [caracteres definidos pelo usuário final (EUDCs)](end-user-defined-characters.md) para uma determinada página de código. Ele tem o seguinte local de registro:

HKEY \_ Current \_ user \\ EUDC

O formato é:

EUDC SystemDefaultEUDCFont = TrueTypeEUDCFontFileName TrueTypeFontTypeface = TrueTypeEUDCFontFileName

onde:



|                          |                                                                                                                                          |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| SystemDefaultEUDCFont    | Nome predefinido usado para definir a fonte padrão do sistema. Não há nenhuma fonte EUDC padrão do sistema, a menos que essa entrada seja explicitamente especificada.     |
| TrueTypeFontTypeface     | Nome definido pelo usuário associado a uma fonte TrueType não EUDC.                                                                              |
| TrueTypeEUDCFontFileName | Cadeia de caracteres que consiste no nome do arquivo de um arquivo de fonte EUDC separado. Esse arquivo identifica uma fonte a ser associada ao TrueTypeFontTypeface. |



 

O exemplo a seguir mostra a chave EUDC para a página de código 932.


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



O exemplo a seguir define a fonte EUDC padrão do sistema como Eudc. ttf e associa as fontes EUDC separadas Mineudc. ttf e Goteudc. ttf com os nomes de fonte MS Mincho e MS Gothic, respectivamente.


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



Quando a página de código do Windows (ACP do sistema) associada ao idioma para programas não-Unicode corresponde à subchave, o subsistema GDI procura os pares de valor de subchave para obter informações de exibição sobre o caractere. Primeiro, ele procura um nome correspondente à fonte atual. Se não houver nenhum, ele examinará o valor SystemDefaultEUDCFont. Se nenhum valor for definido, o GDI tratará o caractere como indefinido.

Observe que o texto em si não precisa estar na página de código do Windows. Por exemplo, suponha que a página de código tenha o identificador 1252, a página de código padrão do Windows para inglês. Um aplicativo passa o ponto de código Unicode único U + E000, na área de uso privado Unicode (PUA), para [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). Nesse caso, o GDI examina os valores de registro em 1252 para obter as informações de fonte das propriedades de exibição de caractere.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Entradas do registro EUDC](eudc-registry-entries.md)
</dt> <dt>

[EUDCCodeRange](eudccoderange.md)
</dt> </dl>

 

 
