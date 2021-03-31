---
description: As funções que não foram implementadas com uma versão Unicode normalmente foram substituídas por funções mais poderosas ou estendidas que dão suporte a Unicode.
ms.assetid: 9e02c8fe-4fed-4b77-9b09-35850350859a
title: Usando funções que não têm equivalentes Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0850eea442b98c81918c7c6733da65f730936be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172180"
---
# <a name="using-functions-that-have-no-unicode-equivalents"></a>Usando funções que não têm equivalentes Unicode

As funções que não foram implementadas com uma versão [Unicode](unicode.md) normalmente foram substituídas por funções mais poderosas ou estendidas que dão suporte a Unicode. Por exemplo, se você estiver portando um código que chama a função [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) , seu aplicativo poderá dar suporte a Unicode usando a função [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) em vez disso.

Se uma função não tiver nenhum equivalente Unicode, o aplicativo poderá mapear os caracteres de e para os conjuntos de caracteres de 8 bits antes e depois da chamada de função. Por exemplo, as funções de formatação de número **atoi** e **itoa** usam apenas os dígitos de 0 a 9. Normalmente, o mapeamento de Unicode para caracteres de 8 bits causa perda de dados, mas isso pode ser evitado, tornando o código independente e tornando as expressões condicionais. As instruções no exemplo a seguir, gravadas para caracteres de 8 bits, são dependentes de tipo e devem ser alteradas para dar suporte a Unicode.


```C++
char str[4] = "137";

int num = atoi(str);
```



Essas instruções podem ser reescritas da seguinte maneira para torná-las independentes de tipo.


```C++
TCHAR tstr[4] = TEXT("137");

#ifdef UNICODE
size_t cCharsConverted;
CHAR strTmp[SIZE]; // SIZE equals (2*(sizeof(tstr)+1)). This ensures enough
                   // room for the multibyte characters if they are two 
                   // bytes long and a terminating null character. See Security 
                   // Alert below. 

wcstombs_s(&cCharsConverted, strTmp, sizeof(strTmp), (const wchar_t *)tstr, sizeof(strTmp));
num = atoi(strTmp);

#else

int num = atoi(tstr);

#endif 
```



Neste exemplo, a função de biblioteca C padrão **wcstombs** converte o Unicode em ASCII. O exemplo se baseia no fato de que os dígitos de 0 a 9 sempre podem ser traduzidos de Unicode para ASCII, mesmo que parte do texto ao redor não possa. A função **atoi** para qualquer caractere que não seja um dígito.

Seu aplicativo pode usar a função [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) do NLS (suporte ao idioma nacional) para processar o texto que inclui os [dígitos nativos](digit-shapes.md) fornecidos para alguns dos scripts em Unicode.

> [!Caution]  
> O uso incorreto da função **wcstombs** pode comprometer a segurança do seu aplicativo. Verifique se o buffer do aplicativo para a cadeia de caracteres de 8 bits tem pelo menos tamanho 2 \* (*\_ tamanho do caractere* + 1), em que *\_ comprimento do char* representa o comprimento da cadeia de caracteres Unicode. Essa restrição é feita porque, com DBCS ( [conjuntos de caracteres de dois bytes](double-byte-character-sets.md) ), cada caractere Unicode pode ser mapeado para dois caracteres consecutivos de 8 bits. Se o buffer não mantiver toda a cadeia de caracteres, a cadeia de caracteres de resultado não será terminada em nulo, apresentando um risco de segurança. Para obter mais informações sobre segurança de aplicativos, consulte [Considerações sobre segurança: recursos internacionais](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando Unicode e conjuntos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
