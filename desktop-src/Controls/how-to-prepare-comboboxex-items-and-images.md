---
title: Como preparar itens e imagens comboBoxEx
description: Este tópico demonstra como adicionar itens a um controle ComboBoxEx.
ms.assetid: 2603DFBE-9E7A-4B2F-BE33-418997D323B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ea0b6defc7e99bd98c3dac551346280f0650da9e58a948e77ccc98aec81cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958695"
---
# <a name="how-to-prepare-comboboxex-items-and-images"></a>Como preparar itens e imagens comboBoxEx

Este tópico demonstra como adicionar itens a um controle ComboBoxEx.

Para adicionar um item a um controle ComboBoxEx, primeiro defina uma [**estrutura COMBOBOXEXITEM.**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) Em seguida, de **definir o** membro de máscara da estrutura para indicar quais membros você deseja que o controle use. Por fim, de definir os membros especificados da estrutura para os valores desejados e enviar a mensagem [**CBEM \_ INSERTITEM**](cbem-insertitem.md) para adicionar o item ao controle.

A função definida pelo aplicativo a seguir adiciona 15 itens a um controle ComboBoxEx existente.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Para adicionar um item a um controle ComboBoxEx, primeiro defina uma [**estrutura COMBOBOXEXITEM.**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)


```C++
COMBOBOXEXITEM cbei;
int iCnt;


typedef struct {
    int iImage;
    int iSelectedImage;
    int iIndent;
    LPTSTR pszText;
} ITEMINFO, *PITEMINFO;

ITEMINFO IInf[ ] = {
    { 0, 3,  0, L"first"}, 
    { 1, 4,  1, L"second"},
    { 2, 5,  2, L"third"},
    { 0, 3,  0, L"fourth"},
    { 1, 4,  1, L"fifth"},
    { 2, 5,  2, L"sixth"},
    { 0, 3,  0, L"seventh"},
    { 1, 4,  1, L"eighth"},
    { 2, 5,  2, L"ninth"},
    { 0, 3,  0, L"tenth"},
    { 1, 4,  1, L"eleventh"},
    { 2, 5,  2, L"twelfth"},
    { 0, 3,  0, L"thirteenth"},
    { 1, 4,  1, L"fourteenth"},
    { 2, 5,  2, L"fifteenth"}
};
```



### <a name="step-2"></a>Etapa 2:

De definir **o membro** de máscara da estrutura para indicar quais membros você deseja que o controle use. Observe que o **membro de** máscara da estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) inclui valores de sinalizador que informam ao controle para exibir imagens para cada item.


```C++
// Set the mask common to all items.
cbei.mask = CBEIF_TEXT | CBEIF_INDENT |
            CBEIF_IMAGE| CBEIF_SELECTEDIMAGE;
```



### <a name="step-3"></a>Etapa 3:

Defina os membros especificados da estrutura para os valores que você deseja e, em seguida, envie a mensagem [**CBEM \_ INSERTITEM**](cbem-insertitem.md) para adicionar o item ao controle.


```C++
for(iCnt=0;iCnt<MAX_ITEMS;iCnt++){
    // Initialize the COMBOBOXEXITEM struct.
    cbei.iItem          = iCnt;
    cbei.pszText        = IInf[iCnt].pszText;
    cbei.cchTextMax     = sizeof(IInf[iCnt].pszText);
    cbei.iImage         = IInf[iCnt].iImage;
    cbei.iSelectedImage = IInf[iCnt].iSelectedImage;
    cbei.iIndent        = IInf[iCnt].iIndent;

    
    // Tell the ComboBoxEx to add the item. Return FALSE if 
    // this fails.
    if(SendMessage(hwndCB,CBEM_INSERTITEM,0,(LPARAM)&cbei) == -1)
        return FALSE;
```



### <a name="step-4"></a>Etapa 4:

Atribua a lista de imagens existente ao controle ComboBoxEx e de definido o tamanho do controle.


```C++
// Assign the existing image list to the ComboBoxEx control 
// and return TRUE. 
// g_himl is the handle to the existing image list
SendMessage(hwndCB,CBEM_SETIMAGELIST,0,(LPARAM)g_himl);

// Set size of control to make sure it's displayed correctly now
// that the image list is set.
SetWindowPos(hwndCB,NULL,20,20,250,120,SWP_NOACTIVATE);

return TRUE; 
```



## <a name="complete-example"></a>Exemplo completo


```C++
// AddItems - Uses the CBEM_INSERTITEM message to add items to an
// existing ComboBoxEx control.

BOOL WINAPI AddItems(HWND hwndCB)
{
    
    //  Declare and init locals.
    COMBOBOXEXITEM cbei;
    int iCnt;
    

    typedef struct {
        int iImage;
        int iSelectedImage;
        int iIndent;
        LPTSTR pszText;
    } ITEMINFO, *PITEMINFO;

    ITEMINFO IInf[ ] = {
        { 0, 3,  0, L"first"}, 
        { 1, 4,  1, L"second"},
        { 2, 5,  2, L"third"},
        { 0, 3,  0, L"fourth"},
        { 1, 4,  1, L"fifth"},
        { 2, 5,  2, L"sixth"},
        { 0, 3,  0, L"seventh"},
        { 1, 4,  1, L"eighth"},
        { 2, 5,  2, L"ninth"},
        { 0, 3,  0, L"tenth"},
        { 1, 4,  1, L"eleventh"},
        { 2, 5,  2, L"twelfth"},
        { 0, 3,  0, L"thirteenth"},
        { 1, 4,  1, L"fourteenth"},
        { 2, 5,  2, L"fifteenth"}
    };

    // Set the mask common to all items.
    cbei.mask = CBEIF_TEXT | CBEIF_INDENT |
                CBEIF_IMAGE| CBEIF_SELECTEDIMAGE;

    for(iCnt=0;iCnt<MAX_ITEMS;iCnt++){
        // Initialize the COMBOBOXEXITEM struct.
        cbei.iItem          = iCnt;
        cbei.pszText        = IInf[iCnt].pszText;
        cbei.cchTextMax     = sizeof(IInf[iCnt].pszText);
        cbei.iImage         = IInf[iCnt].iImage;
        cbei.iSelectedImage = IInf[iCnt].iSelectedImage;
        cbei.iIndent        = IInf[iCnt].iIndent;
    
        
        // Tell the ComboBoxEx to add the item. Return FALSE if 
        // this fails.
        if(SendMessage(hwndCB,CBEM_INSERTITEM,0,(LPARAM)&cbei) == -1)
            return FALSE;
    }
    // Assign the existing image list to the ComboBoxEx control 
    // and return TRUE. 
    // g_himl is the handle to the existing image list
    SendMessage(hwndCB,CBEM_SETIMAGELIST,0,(LPARAM)g_himl);

    // Set size of control to make sure it's displayed correctly now
    // that the image list is set.
    SetWindowPos(hwndCB,NULL,20,20,250,120,SWP_NOACTIVATE);

    return TRUE; 
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre controles ComboBoxEx](comboboxex-controls.md)
</dt> <dt>

[Referência de controle ComboBoxEx](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Usando controles ComboBoxEx](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[Comboboxex](comboboxex-control-reference.md)
</dt> </dl>

 

 