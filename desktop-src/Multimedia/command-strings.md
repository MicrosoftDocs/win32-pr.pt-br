---
title: Cadeias de caracteres de comando
description: Cadeias de caracteres de comando
ms.assetid: ca9ca153-f2bf-45ed-84e6-44e86e8efaed
keywords:
- Cadeias de caracteres de comando MCI, sobre
- Cadeias de caracteres de comando MCI, sintaxe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f3638271dd004db13fe3ee2f0517eef0c1d2fe72be93da37a73f47e6666212
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807826"
---
# <a name="command-strings"></a>Cadeias de caracteres de comando

Para enviar um comando de cadeia de caracteres para um dispositivo MCI, use a [**função mciSendString,**](/previous-versions//dd757161(v=vs.85)) que inclui parâmetros para o comando de cadeia de caracteres e um buffer para quaisquer informações retornadas.

A **função mciSendString** retornará zero se for bem-sucedida. Se a função falhar, a palavra de ordem baixa do valor de retorno conterá um código de erro. Você pode passar esse código de erro para a [**função mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) para obter uma descrição de texto do erro.

## <a name="syntax-of-command-strings"></a>Sintaxe de cadeias de caracteres de comando

As cadeias de caracteres de comando MCI usam uma sintaxe verb-object-modifier consistente. Cada cadeia de caracteres de comando inclui um comando, um identificador de dispositivo e argumentos de comando. Os argumentos são opcionais para alguns comandos e são necessários para outros.

Uma cadeia de caracteres de comando tem o seguinte formato:

*argumentos de \_ ID do dispositivo de comando*

Esses componentes contêm as seguintes informações:

-   O *comando* especifica um comando MCI, como [**abrir**](open.md), [**fechar**](close.md)ou [**reproduzir**](play.md).
-   A *\_ ID do dispositivo* identifica uma instância de um driver MCI. A *\_ ID do dispositivo* é criada quando o dispositivo é aberto.
-   Os *argumentos* especificam os sinalizadores e as variáveis usados pelo comando . Sinalizadores são palavras-chave reconhecidas com o comando MCI. As variáveis são números ou cadeias de caracteres que se aplicam ao comando ou sinalizador MCI.

    Por exemplo, o **comando play** usa os argumentos "from *position"* e "to *position"* para indicar as posições nas quais iniciar e encerrar a reprodução. Você pode listar os sinalizadores usados com um comando em qualquer ordem. Ao usar um sinalizador que tem uma variável associada a ele, você deve fornecer um valor para a variável.

    Argumentos de comando não especificados (e opcionais) assumem um valor padrão.

A função de exemplo a seguir envia [**o comando play**](play.md) com os sinalizadores "from" e "to".


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



## <a name="data-types-for-command-variables"></a>Tipos de dados para variáveis de comando

Você pode usar os seguintes tipos de dados para as variáveis em uma cadeia de caracteres de comando.



| **Data type**        | **Descrição**                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cadeias de caracteres              | Os tipos de dados de cadeia de caracteres são delimitados por espaços em branco à frente e à sua frente e aspas. A MCI remove aspas simples de uma cadeia de caracteres. Para colocar aspas em uma cadeia de caracteres, use um conjunto de duas aspas em que você deseja inserir suas aspas. Para usar uma cadeia de caracteres vazia, use duas aspas delimitadas por espaços em branco à frente e à sua frente. |
| Inteiros longos com sinal | Os tipos de dados inteiros longos com sinal são delimitados por espaços em branco à frente e à frente. A menos que especificado de outra forma, inteiros podem ser positivos ou negativos. Se você usar inteiros negativos, não deverá separar o sinal de subtração e o primeiro dígito com um espaço.                                                                                                    |
| Retângulos           | Os tipos de dados rectangle são uma lista ordenada de quatro valores curtos assinados. O espaço em branco delimita esse tipo de dados e separa cada inteiro na lista.                                                                                                                                                                                                              |



 

 

 