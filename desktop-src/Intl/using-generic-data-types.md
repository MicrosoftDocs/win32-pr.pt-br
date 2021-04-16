---
description: Se você usar tipos de dados genéricos em seu código, ele poderá ser compilado para Unicode simplesmente usando uma diretiva de pré-processador para definir &\# 0034; UNICODE&\# 0034; antes das \# instruções include para os arquivos de cabeçalho.
ms.assetid: 1c9cbb18-9295-4847-86c1-d596668cbe57
title: Usando tipos de dados genéricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2604f87b12e86076bed47f509c6398fa8482b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758134"
---
# <a name="using-generic-data-types"></a>Usando tipos de dados genéricos

Se você usar tipos de dados genéricos em seu código, ele poderá ser compilado para [Unicode](unicode.md) simplesmente usando uma diretiva de pré-processador para definir "Unicode" antes das instruções **\# include** para os arquivos de cabeçalho. Para compilar o código para [páginas de código do Windows (ANSI)](code-pages.md), omita a definição "Unicode". Novos aplicativos do Windows devem usar Unicode para evitar as inconsistências de páginas de código variadas e simplificar a localização.

Para criar o código-fonte que pode ser compilado para usar caracteres e cadeias Unicode ou para usar caracteres e cadeias de caractere de páginas de código do Windows:

1.  Use tipos de dados genéricos, como TCHAR, LPTSTR e LPTCH, para todos os tipos de caracteres e cadeias de caracteres usados para texto. Para obter mais informações sobre tipos genéricos, consulte [tipos de dados do Windows para cadeias de caracteres](windows-data-types-for-strings.md).
2.  Certifique-se de que os ponteiros para buffers de dados não texto ou matrizes de bytes binários sejam codificados com tipos de dados como LPBYTE ou LPWORD, em vez do tipo LPTSTR ou LPTCH.
3.  Declare ponteiros de tipo indeterminado explicitamente como ponteiros void usando LPVOID conforme apropriado.
4.  Torne o tipo aritmético de ponteiro independente. O uso de unidades de tamanho TCHAR produz variáveis que são 2 bytes se o UNICODE estiver definido e 1 byte se UNICODE não estiver definido. O uso de aritmética de ponteiro sempre retorna o número de elementos indicados pelo ponteiro, se os elementos têm 1 ou 2 bytes de tamanho. A expressão a seguir sempre recupera o número de elementos, independentemente de o UNICODE ser definido ou não.

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    A expressão a seguir determina o número de bytes usados.

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    Não é necessário alterar uma instrução como a seguinte, pois o incremento do ponteiro aponta para o próximo elemento Character.

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

    

    Use a macro de [**texto**](/windows/desktop/api/Winnt/nf-winnt-text) da seguinte maneira nesta expressão.

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    A macro [**Text**](/windows/desktop/api/Winnt/nf-winnt-text) faz com que as cadeias de caracteres sejam avaliadas como L "String" quando o Unicode é definido e como "String" caso contrário. Para um gerenciamento mais fácil, mova cadeias de caracteres literais para recursos, especialmente se eles contiverem personagens fora do intervalo ASCII (0x00 a 0x7F) ou forem expostos na interface do usuário. Para dar suporte à localização de seu aplicativo para diferentes idiomas nacionais, é muito importante que todas as cadeias de caracteres da interface do usuário estejam em recursos localizáveis.

6.  Use as versões genéricas das funções do Windows. Para obter mais informações, consulte [convenções para protótipos de função](conventions-for-function-prototypes.md).
7.  Use as versões genéricas das funções de cadeia de caracteres da biblioteca C padrão e lembre-se de definir " \_ Unicode", bem como "Unicode", conforme discutido nas [funções padrão do C](standard-c-functions.md).
8.  Se você estiver adaptando um aplicativo originalmente escrito para páginas de código do Windows, lembre-se de alterar qualquer código que dependa de 255 como o maior valor para um caractere.

Quando você compila o código escrito conforme descrito acima, o compilador pode criar versões de página de código Unicode e do Windows de seu aplicativo a partir da mesma origem. Dependendo das definições de UNICODE, as funções genéricas são resolvidas para produzir os mesmos arquivos binários como se você escrevesse o código exclusivamente para Unicode ou exclusivamente para páginas de código do Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando Unicode e conjuntos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 



