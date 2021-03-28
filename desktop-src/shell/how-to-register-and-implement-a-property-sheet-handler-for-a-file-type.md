---
description: Quando o usuário clica com o botão direito do mouse em um membro de um tipo de arquivo para exibir a folha de propriedades Propriedades, o Shell chama os manipuladores de folha de propriedades que são registrados para o tipo de arquivo. Cada manipulador pode adicionar uma página personalizada à folha de propriedades padrão.
title: Como registrar e implementar um manipulador de folha de propriedades para um tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cf54886f7819fa910da23393c6db488ddfee72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988979"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a>Como registrar e implementar um manipulador de folha de propriedades para um tipo de arquivo

Quando o usuário clica com o botão direito do mouse em um membro de um tipo de arquivo para exibir a folha de propriedades Propriedades, o Shell chama os manipuladores de folha de propriedades que são registrados para o tipo de arquivo. Cada manipulador pode adicionar uma página personalizada à folha de propriedades padrão.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   Shell

### <a name="prerequisites"></a>Pré-requisitos

-   Uma compreensão dos menus de atalho

## <a name="instructions"></a>Instruções

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a>Etapa 1: registrar um manipulador de folha de propriedades para um tipo de arquivo

Além do registro COM (normal Component Object Model), adicione uma subchave **PropertySheetHandlers** à subchave **shellex** da chave ProgID do aplicativo associado ao tipo de arquivo. Crie uma subchave de **PropertySheetHandlers** com o nome do manipulador e defina o valor padrão como a forma de cadeia de caracteres do GUID do identificador de classe (CLSID) do manipulador de folha de propriedades.

Para adicionar mais de uma página à folha de propriedades, registre um manipulador para cada página. O número máximo de páginas às quais uma folha de propriedades pode dar suporte é 32. Para registrar vários manipuladores, crie uma chave na chave **shellex** para cada manipulador, com o valor padrão definido como o GUID CLSID do manipulador. Não é necessário criar um objeto distinto para cada manipulador, o que significa que vários manipuladores podem ter o mesmo valor de GUID. As páginas serão exibidas na ordem em que suas chaves estão listadas em **shellex**.

O exemplo a seguir ilustra uma entrada de registro que habilita dois manipuladores de extensão de folha de propriedades para um tipo de arquivo. MYP de exemplo. Neste exemplo, um objeto separado é usado para cada página, mas um único objeto também pode ser usado para ambos.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {Page 1 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet1.dll
            ThreadingModel = Apartment
      {Page 2 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet2.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         PropertySheetHandlers
            MyPropSheet1
               (Default) = {Page1 Property Sheet Handler CLSID GUID}
            MyPropSheet2
               (Default) = {Page2 Property Sheet Handler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a>Etapa 2: Implementando um manipulador de folha de propriedades para um tipo de arquivo

Além da implementação geral discutida em [como funcionam os manipuladores de folha de propriedades](propsheet-handlers.md), um manipulador de folha de propriedades para um tipo de arquivo também deve ter uma implementação apropriada da interface [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) . Somente o método [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) precisa de uma implementação de não token. O shell não chama [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).

O método [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) permite que um manipulador de folha de propriedades adicione uma página a uma folha de propriedades. O método tem dois parâmetros de entrada. O primeiro, *lpfnAddPage*, é um ponteiro para uma função de retorno de chamada [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) que é usada para fornecer ao shell as informações necessárias para adicionar a página à folha de propriedades. O segundo, *lParam*, é um valor definido por shell que não é processado pelo manipulador. Ele é simplesmente passado de volta para o shell quando a função de retorno de chamada é chamada.

O procedimento geral para implementar [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) é o seguinte.

**Implementando o método AddPages**

1.  Atribua valores apropriados aos membros de uma estrutura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) . Especialmente:
    -   Atribua a variável que mantém a contagem de referência do manipulador ao membro **pcRefParent** . Essa prática impede que o objeto do manipulador seja descarregado enquanto a folha de propriedades ainda está sendo exibida.
    -   Você também pode implementar uma função de retorno de chamada [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) e atribuir seu ponteiro a um membro **pfnCallback** . Essa função é chamada quando a página é criada e quando está prestes a ser destruída.
2.  Crie o identificador HPAGE da página passando a estrutura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) para a função [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) .
3.  Chame a função que é apontada por *lpfnAddPage*. Defina seu primeiro parâmetro para o identificador HPAGE que foi criado na etapa anterior. Defina seu segundo parâmetro para o valor de *lParam* que foi passado para [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) pelo shell.
4.  Todas as mensagens associadas à página serão passadas para o procedimento da caixa de diálogo que foi atribuído ao membro **pfnDlgProc** da estrutura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) .
5.  Se você atribuiu uma função de retorno de chamada [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) a **pfnCallback**, ela será chamada quando a página estiver prestes a ser destruída. Em seguida, seu manipulador pode executar todas as operações de limpeza necessárias, como liberar todas as referências que ela contém.

O exemplo de código a seguir ilustra uma implementação simples de [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) .


```C++
STDMETHODIMP CShellPropSheetExt::AddPages(LPFNADDPROPSHEETPAGE, lpfnAddPage, LPARAM lParam)
{
    PROPSHEETPAGE  psp;
    HPROPSHEETPAGE hPage;

    psp.dwSize        = sizeof(psp);
    psp.dwFlags       = PSP_USEREFPARENT | PSP_USETITLE | PSP_USECALLBACK;
    psp.hInstance     = g_hInst;
    psp.pszTemplate   = MAKEINTRESOURCE(IDD_PAGEDLG);
    psp.hIcon         = 0;
    psp.pszTitle      = TEXT("Extension Page");
    psp.pfnDlgProc    = (DLGPROC)PageDlgProc;
    psp.pcRefParent   = &g_DllRefCount;
    psp.pfnCallback   = PageCallbackProc;
    psp.lParam        = (LPARAM)this;

    hPage = CreatePropertySheetPage(&psp);
            
    if(hPage) 
    {
        if(lpfnAddPage(hPage, lParam))
        {
            this->AddRef();
            return S_OK;
        }
        else
        {
            DestroyPropertySheetPage(hPage);
        }
    }
    else
    {
        return E_OUTOFMEMORY;
    }
    return E_FAIL;
}
```



A variável **g \_ hinst** é o identificador de instância para a dll e IDD \_ PAGEDLG é a ID de recurso do modelo de caixa de diálogo da página. A função **PageDlgProc** é o procedimento da caixa de diálogo que manipula as mensagens da página. A variável **g \_ DllRefCount** contém a contagem de referência do objeto. O método [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) chama [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) para incrementar a contagem. No entanto, a contagem de referência é liberada pela função de retorno de chamada, **PageCallbackProc**, quando a página está prestes a ser destruída.

## <a name="remarks"></a>Comentários

Para obter uma discussão geral sobre como registrar manipuladores de extensão de Shell, consulte [criando manipuladores de extensão de shell](handlers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 
