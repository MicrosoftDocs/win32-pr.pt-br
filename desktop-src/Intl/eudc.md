---
description: A chave do Registro EUDC contém uma ou mais sub-chaves que contêm valores que definem as fontes associadas aos EUDCs (caracteres definidos pelo usuário final) para uma determinada página de código.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: Eudc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b583c7a0bfaa67684901e8d0a4a95ac5e45658
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120701"
---
# <a name="eudc"></a>Eudc

A chave do Registro EUDC contém uma ou mais sub-chaves que contêm valores que definem as fontes associadas aos [EUDCs (caracteres](end-user-defined-characters.md) definidos pelo usuário final) para uma determinada página de código. Ele tem o seguinte local do Registro:

\_ \_ EUDC DO USUÁRIO ATUAL \\ DO HKEY

O formato é:

EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName

em que:



| Valor                         | Descrição                                                                                                                                         |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| SystemDefaultEUDCFont    | Nome predefinido usado para definir a fonte padrão do sistema. Não há nenhuma fonte EUDC padrão do sistema, a menos que essa entrada seja especificada explicitamente.     |
| TrueTypeFontTypeface     | Nome definido pelo usuário associado a uma fonte TrueType não EUDC.                                                                              |
| TrueTypeEUDCFontFileName | Cadeia de caracteres que consiste no nome do arquivo de um arquivo de fonte EUDC separado. Esse arquivo identifica uma fonte a ser associada a TrueTypeFontTypeface. |



 

O exemplo a seguir mostra a chave EUDC para a página de código 932.


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



O exemplo a seguir define a fonte EUDC padrão do sistema como Eudc.ttf e associa as fontes EUDC separadas Mineudc.ttf e Goteudc.ttf aos nomes de fonte MS Mincho e MS Ques, respectivamente.


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



Quando a página de código do Windows (sistema ACP) associada à linguagem para programas não Unicode corresponde à sub-chave , o subsistema GDI procura os pares de valores de sub-chave para obter informações de exibição sobre o caractere. Primeiro, ele procura um nome que corresponde à fonte atual. Se não houver nenhum, ele examinará o valor SystemDefaultEUDCFont. Se nenhum valor for definido, a GDI tratará o caractere como indefinido.

Observe que o texto em si não precisa estar na página de código do Windows. Por exemplo, suponha que a página de código tenha o identificador 1252, a página de código padrão do Windows para inglês. Um aplicativo passa o único ponto de código Unicode U+E000, na PUA (área de uso privado Unicode), para [**DrawText.**](/windows/win32/api/winuser/nf-winuser-drawtext) Nesse caso, a GDI analisa os valores do Registro em 1252 para obter as informações de fonte para as propriedades de exibição de caracteres.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Entradas do Registro EUDC](eudc-registry-entries.md)
</dt> <dt>

[EUDCCodeRange](eudccoderange.md)
</dt> </dl>

 

 
