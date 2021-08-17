---
title: Recuperar atributos de objeto, selecionar novos objetos
description: Um aplicativo pode recuperar os atributos de uma caneta, pincel, paleta, fonte ou bitmap chamando as funções GetCurrentObject e GetObject.
ms.assetid: 09d8412f-a67d-48d5-9c04-9233dee43cf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c58d946f61a6a83dcfeb2ddae24d735d3596e5e864cf672bab832d7db3aedf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886137"
---
# <a name="retrieve-object-attributes-select-new-objects"></a>Recuperar atributos de objeto, selecionar novos objetos

Um aplicativo pode recuperar os atributos de uma caneta, pincel, paleta, fonte ou bitmap chamando as funções [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) e [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) . A função **GetCurrentObject** retorna um identificador que identifica o objeto selecionado atualmente no controlador de domínio; a função **GetObject** retorna uma estrutura que descreve os atributos do objeto.

O exemplo a seguir mostra como um aplicativo pode recuperar os atributos de pincel atuais e usar os dados recuperados para determinar se é necessário selecionar um novo pincel.


```C++
    HDC hdc;                     // display DC handle  
    HBRUSH hbrushNew, hbrushOld; // brush handles  
    HBRUSH hbrush;               // brush handle  
    LOGBRUSH lb;                 // logical-brush structure  
 
    // Retrieve a handle identifying the current brush.  
 
    hbrush = GetCurrentObject(hdc, OBJ_BRUSH); 
 
    // Retrieve a LOGBRUSH structure that contains the  
    // current brush attributes.  
 
    GetObject(hbrush, sizeof(LOGBRUSH), &lb); 
 
    // If the current brush is not a solid-black brush,  
    // replace it with the solid-black stock brush.  
 
    if ((lb.lbStyle != BS_SOLID) 
           || (lb.lbColor != 0x000000)) 
    { 
        hbrushNew = GetStockObject(BLACK_BRUSH); 
        hbrushOld = SelectObject(hdc, hbrushNew); 
    } 
 
    // Perform painting operations with the white brush.  
 
 
    // After completing the last painting operation with the new  
    // brush, the application should select the original brush back  
    // into the device context and delete the new brush.  
    // In this example, hbrushNew contains a handle to a stock object.  
    // It is not necessary (but it is not harmful) to call  
    // DeleteObject on a stock object. If hbrushNew contained a handle  
    // to a brush created by a function such as CreateBrushIndirect,  
    // it would be necessary to call DeleteObject.  
 
    SelectObject(hdc, hbrushOld); 
    DeleteObject(hbrushNew); 
```



> [!Note]
>
> O aplicativo salvou o identificador de pincel original ao chamar a função [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) pela primeira vez. Esse identificador é salvo para que o pincel original possa ser selecionado novamente no controlador de domínio após a conclusão da última operação de pintura com o novo pincel. Depois que o pincel original é selecionado de volta ao controlador de domínio, o novo pincel é excluído, liberando memória no heap GDI.

 

 

 



