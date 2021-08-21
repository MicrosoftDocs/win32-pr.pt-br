---
description: Se você usar tipos de dados genéricos em seu código, ele poderá ser compilado para Unicode simplesmente usando uma diretiva de pré-processador para definir &\# 0034; UNICODE&\# 0034; antes das \# instruções include para os arquivos de header.
ms.assetid: 1c9cbb18-9295-4847-86c1-d596668cbe57
title: Usando tipos de dados genéricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a61bed094506f0d31718b0b88fe519028ba1db785ebda3e00404a7aa3257e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535456"
---
# <a name="using-generic-data-types"></a>Usando tipos de dados genéricos

Se você usar tipos de dados genéricos em seu código, ele poderá ser compilado para [Unicode](unicode.md) simplesmente usando uma diretiva de pré-processador para definir "UNICODE" antes das instruções **\# include** para os arquivos de header. Para compilar o código [para Windows de código (ANSI),](code-pages.md)omita a definição "UNICODE". Novos Windows aplicativos devem usar Unicode para evitar inconsistências de páginas de código variadas e simplificar a localização.

Para criar o código-fonte que pode ser compilado para usar caracteres Unicode e cadeias de caracteres ou para usar caracteres e cadeias de caracteres Windows páginas de código:

1.  Use tipos de dados genéricos, como TCHAR, LPTSTR e LPTCH, para todos os tipos de caractere e cadeia de caracteres usados para texto. Para obter mais informações sobre tipos genéricos, [consulte Windows de dados para cadeias de caracteres](windows-data-types-for-strings.md).
2.  Certifique-se de que os ponteiros para buffers de dados sem texto ou matrizes de byte binários sejam codificados com tipos de dados como LPBYTE ou LPWORD, em vez do tipo LPTSTR ou LPTCH.
3.  Declare ponteiros do tipo indeterminado explicitamente como ponteiros nulos usando LPVOID conforme apropriado.
4.  Tornar o tipo aritmético de ponteiro independente. O uso de unidades de tamanho TCHAR produzirá variáveis de 2 bytes se UNICODE for definido e 1 byte se UNICODE não estiver definido. Usar a aritmética de ponteiro sempre retorna o número de elementos indicados pelo ponteiro, independentemente de os elementos ter 1 ou 2 bytes de tamanho. A expressão a seguir sempre recupera o número de elementos, independentemente de UNICODE estar definido.

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    A expressão a seguir determina o número de bytes usados.

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    Não é necessário alterar uma instrução como a seguinte, porque o incremento de ponteiro aponta para o próximo elemento de caractere.

    ```C++
    chNext = *++lpText;
    ```

    

5.  Substitua cadeias de caracteres literais e constantes de caractere de manifesto por macros. Altere expressões como a seguinte.

    ```C++
    while(*lpFileName++ != '\\')
    {
        // ...
    }
    ```

    

    Use a macro [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) da seguinte forma nesta expressão.

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    A [**macro TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) faz com que cadeias de caracteres sejam avaliadas como L"string" quando UNICODE for definido e como "cadeia de caracteres", caso contrário. Para facilitar o gerenciamento, mova cadeias de caracteres literais para recursos, especialmente se elas contêm caracteres fora do intervalo ASCII (0x00 a 0x7F) ou sejam expostas na interface do usuário. Para dar suporte à localização do aplicativo para diferentes idiomas nacionais, é muito importante que todas as cadeias de caracteres de interface do usuário sejam recursos localizáveis.

6.  Use as versões genéricas das Windows funções. Para obter mais informações, consulte [Convenções para protótipos de função](conventions-for-function-prototypes.md).
7.  Use as versões genéricas das funções de cadeia de caracteres da biblioteca C padrão e lembre-se de definir " UNICODE", bem como \_ "UNICODE", conforme discutido em [Funções C Padrão](standard-c-functions.md).
8.  Se você estiver adaptando um aplicativo originalmente escrito para Windows páginas de código, lembre-se de alterar qualquer código que se basear em 255 como o maior valor para um caractere.

Quando você compila o código que você escreveu conforme descrito acima, o compilador pode criar versões de página de código Unicode e Windows do aplicativo da mesma fonte. Dependendo das definições para UNICODE, as funções genéricas são resolvidas para produzir os mesmos arquivos binários como se você escreve o código exclusivamente para Unicode ou exclusivamente para Windows páginas de código.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando unicode e conjuntos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 



