---
title: converter cadeias de caracteres
description: converter cadeias de caracteres
ms.assetid: 40621c71-4264-40bc-b6c3-6b639d2f28fa
keywords:
- função mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efeb5801c46d89686ed3fe9fcf25b311d57d4d553c220902907ac0e70a5b7e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144789"
---
# <a name="converting-strings"></a>converter cadeias de caracteres

Quando você usa a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , todos os valores passados com o comando e todos os valores de retorno são cadeias de caracteres de texto, de modo que seu aplicativo precisa de rotinas de conversão para traduzir de variáveis para cadeias de caracteres ou de volta. O exemplo a seguir recupera o retângulo de origem e converte a cadeia de caracteres retornada em coordenadas de retângulo.


```C++
BOOL GetSourceRect(LPTSTR lpstrAlias, LPRECT lprc) 
{ 
    TCHAR achRetBuff[128]; 
    TCHAR achCommandBuff[128]; 

    int result;
    MCIERROR err;
 
    // Build the command string. 
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("where %s source"), 
        lpstrAlias); 

    if (result == -1)
    {
        return FALSE;
    }
    
    // Clear the RECT.
    SetRectEmpty(lprc);
 
    // Send the MCI command. 
    err = mciSendString(
        achCommandBuff, 
        achRetBuff, 
        sizeof(achRetBuff), 
        NULL);

    if (err != 0)
    {
        return FALSE;
    }
        
    // The rectangle is returned as "x y dx dy". 
    // Translate the string into the RECT structure. 

    // Warning: This example omits error checking
    // for the _tcstok_s and _tstoi functions.
    TCHAR *p; 
    TCHAR *context;

    // Left.
    p = _tcstok_s(achRetBuff, TEXT(" "), &context);
    lprc->left = _tstoi(p);

    // Top.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->top = _tstoi(p);

    // Right.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->right = _tstoi(p);
    
    // Bottom.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->bottom = _tstoi(p);

    return TRUE;
}
 
```



> [!Note]  
> As estruturas **Rect** são tratadas de forma diferente no MCI do que em outras partes do Windows; no MCI, o membro **correto** contém a largura do retângulo e o membro **inferior** contém sua altura. Na interface de cadeia de caracteres, um retângulo é especificado como *X1*, *Y1*, *X2* e *Y2*. As coordenadas *X1* e *Y1* especificam o canto superior esquerdo do retângulo, e as coordenadas *X2* e *Y2* especificam a largura e a altura.

 

 

 