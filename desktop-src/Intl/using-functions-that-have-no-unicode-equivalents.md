---
description: Funções que não foram implementadas com uma versão Unicode normalmente foram substituídas por funções mais avançadas ou estendidas que suportam Unicode.
ms.assetid: 9e02c8fe-4fed-4b77-9b09-35850350859a
title: Usando funções que não têm equivalentes Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00781db9bce98c335c4a9071b9643ef5fdcb3716478cbffe12a5b53b33e2313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787876"
---
# <a name="using-functions-that-have-no-unicode-equivalents"></a>Usando funções que não têm equivalentes Unicode

Funções que não foram implementadas com uma versão [Unicode](unicode.md) normalmente foram substituídas por funções mais avançadas ou estendidas que suportam Unicode. Por exemplo, se você estiver portando código que chama a [**função OpenFile,**](/windows/win32/api/winbase/nf-winbase-openfile) seu aplicativo poderá dar suporte a Unicode usando a [**função CreateFile.**](/windows/win32/api/fileapi/nf-fileapi-createfilea)

Se uma função não tiver nenhum equivalente a Unicode, o aplicativo poderá mapear caracteres de e para conjuntos de caracteres de 8 bits antes e depois da chamada de função. Por exemplo, as funções de formatação de número **atoi** e **itoa** usam apenas os dígitos de 0 a 9. Normalmente, o mapeamento de Unicode para caracteres de 8 bits causa perda de dados, mas isso pode ser evitado tornando o tipo de código independente e tornando as expressões condicionais. As instruções no exemplo a seguir, escritas para caracteres de 8 bits, são dependentes de tipo e devem ser alteradas para dar suporte a Unicode.


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



Neste exemplo, a função de biblioteca C padrão **wcstombs** converte Unicode em ASCII. O exemplo se baseia no fato de que os dígitos de 0 a 9 sempre podem ser convertidos de Unicode para ASCII, mesmo que parte do texto ao redor não possa. A **função atoi** para em qualquer caractere que não seja um dígito.

Seu aplicativo pode usar a função [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) do NLS (National Language Support) para processar o texto que inclui os dígitos nativos [fornecidos](digit-shapes.md) para alguns dos scripts em Unicode.

> [!Caution]  
> Usar a **função wcstombs** incorretamente pode comprometer a segurança do aplicativo. Certifique-se de que o buffer do aplicativo para a cadeia de caracteres de 8 bits seja pelo menos do tamanho 2 ( comprimento do caractere +1), em que o comprimento do caractere representa o comprimento da cadeia de caracteres \* Unicode.*\_* *\_* Essa restrição é feita porque, com DBCSs (conjuntos de caracteres de dois [byte),](double-byte-character-sets.md) cada caractere Unicode pode ser mapeado para dois caracteres de 8 bits consecutivos. Se o buffer não manter a cadeia de caracteres inteira, a cadeia de caracteres de resultado não será terminada em nulo, representando um risco de segurança. Para obter mais informações sobre a segurança do aplicativo, consulte [Considerações sobre segurança: recursos internacionais.](security-considerations--international-features.md)

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando unicode e conjuntos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
