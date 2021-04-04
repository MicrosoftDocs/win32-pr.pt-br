---
title: converter cadeias de caracteres
description: converter cadeias de caracteres
ms.assetid: 40621c71-4264-40bc-b6c3-6b639d2f28fa
keywords:
- função mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1db4cb4b3d02a93adecc82d6ce95de436fb2e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917175"
---
# <a name="converting-strings"></a><span data-ttu-id="73040-104">converter cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="73040-104">Converting Strings</span></span>

<span data-ttu-id="73040-105">Quando você usa a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , todos os valores passados com o comando e todos os valores de retorno são cadeias de caracteres de texto, de modo que seu aplicativo precisa de rotinas de conversão para traduzir de variáveis para cadeias de caracteres ou de volta.</span><span class="sxs-lookup"><span data-stu-id="73040-105">When you use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function, all values passed with the command and all return values are text strings, so your application needs conversion routines to translate from variables to strings or back again.</span></span> <span data-ttu-id="73040-106">O exemplo a seguir recupera o retângulo de origem e converte a cadeia de caracteres retornada em coordenadas de retângulo.</span><span class="sxs-lookup"><span data-stu-id="73040-106">The following example retrieves the source rectangle and converts the returned string into rectangle coordinates.</span></span>


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
> <span data-ttu-id="73040-107">As estruturas **Rect** são tratadas de forma diferente no MCI do que em outras partes do Windows; no MCI, o membro **correto** contém a largura do retângulo e o membro **inferior** contém sua altura.</span><span class="sxs-lookup"><span data-stu-id="73040-107">**RECT** structures are handled differently in MCI than in other parts of Windows; in MCI, the **right** member contains the width of the rectangle and the **bottom** member contains its height.</span></span> <span data-ttu-id="73040-108">Na interface de cadeia de caracteres, um retângulo é especificado como *X1*, *Y1*, *X2* e *Y2*.</span><span class="sxs-lookup"><span data-stu-id="73040-108">In the string interface, a rectangle is specified as *X1*, *Y1*, *X2*, and *Y2*.</span></span> <span data-ttu-id="73040-109">As coordenadas *X1* e *Y1* especificam o canto superior esquerdo do retângulo, e as coordenadas *X2* e *Y2* especificam a largura e a altura.</span><span class="sxs-lookup"><span data-stu-id="73040-109">The coordinates *X1* and *Y1* specify the upper-left corner of the rectangle, and the coordinates *X2* and *Y2* specify the width and height.</span></span>

 

 

 