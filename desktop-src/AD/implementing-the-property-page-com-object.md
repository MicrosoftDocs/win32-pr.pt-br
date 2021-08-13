---
title: Implementando o objeto COM da página de propriedades
description: Uma extensão de folha de propriedades é um objeto COM implementado como um servidor em processo.
ms.assetid: 77a71086-1949-4828-801e-073ea5a6838b
ms.tgt_platform: multiple
keywords:
- Implementando o objeto COM da página de propriedades
- Objeto COM da página de propriedades, implementando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504c27bcf4703bb49a3e8620c287c30ae9017ab6e65345d003f2acb6c9b544e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187607"
---
# <a name="implementing-the-property-page-com-object"></a>Implementando o objeto COM da página de propriedades

Uma extensão de folha de propriedades é um objeto COM implementado como um servidor em processo. A extensão da folha de propriedades deve implementar as interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) . Uma extensão de folha de propriedades é instanciada quando o usuário exibe a folha de propriedades de um objeto de uma classe para a qual a extensão da folha de propriedades foi registrada no especificador de exibição da classe.

-   [Implementando IShellExtInit](#implementing-ishellextinit)
-   [Implementando IShellPropSheetExt](#implementing-ishellpropsheetext)
-   [Passando o objeto de extensão para a página de propriedades](#passing-the-extension-object-to-the-property-page)
-   [Trabalhando com o objeto de notificação](#working-with-the-notification-object)
-   [Diversos](#miscellaneous)
-   [Folhas de propriedades de seleção múltipla](#multiple-selection-property-sheets)
-   [novo com o Windows Server 2003](#new-with-windows-server-2003)
-   [Tópicos relacionados](#related-topics)

## <a name="implementing-ishellextinit"></a>Implementando IShellExtInit

Depois que o objeto COM da extensão da folha de Propriedades for instanciado, o método [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) será chamado. **IShellExtInit:: Initialize** fornece a extensão da folha de propriedades com um objeto [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) que contém dados pertencentes ao objeto de diretório que a folha de propriedades aplica.

O [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) contém dados no formato [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) . O formato de dados **CFSTR \_ DSOBJECTNAMES** é um **HGLOBAL** que contém uma estrutura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) . A estrutura **DSOBJECTNAMES** contém dados de objeto de diretório que a extensão de folha de propriedades aplica.

O [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) também contém dados no formato [**de \_ \_ Opções de \_ especificação \_ de exibição CFSTR DS**](cfstr-ds-display-spec-options.md) . O formato de dados de **Opções de especificação de \_ \_ exibição CFSTR \_ \_ DS** é um **HGLOBAL** que contém uma estrutura [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) . O **DSDISPLAYSPECOPTIONS** contém dados de configuração para uso pela extensão.

Se qualquer valor diferente de **S \_ OK** for retornado de [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), a folha de propriedades não será exibida.

Os parâmetros *pidlFolder* e *HkeyProgID* do método [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) não são usados.

O ponteiro [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pode ser salvo pela extensão incrementando a contagem de referência do **IDataObject**. Essa interface deve ser liberada quando não for mais necessária.

## <a name="implementing-ishellpropsheetext"></a>Implementando IShellPropSheetExt

Após [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) retornar, o método [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) é chamado. A extensão da folha de propriedades deve adicionar a página ou as páginas durante esse método. Uma página de propriedades é criada preenchendo-se uma estrutura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) e, em seguida, passando essa estrutura para a função [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) . A página de propriedades é adicionada à folha de propriedades chamando a função de retorno de chamada passada para **IShellPropSheetExt:: AddPages** no parâmetro *lpfnAddPage* .

Se qualquer valor diferente de **S \_ OK** for retornado de [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages), a folha de propriedades não será exibida.

Se a extensão da folha de propriedades não for necessária para adicionar nenhuma página à folha de propriedades, ela não deverá chamar a função de retorno de chamada passada para [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) no parâmetro *lpfnAddPage* .

O método [**IShellPropSheetExt:: ReplacePage**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) não é usado.

## <a name="passing-the-extension-object-to-the-property-page"></a>Passando o objeto de extensão para a página de propriedades

O objeto de extensão de folha de propriedades é independente da página de propriedades. Em muitos casos, é desejável poder usar o objeto de extensão ou algum outro objeto da página de propriedades. Para fazer isso, defina o membro **lParam** da estrutura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) como o ponteiro do objeto. A página de propriedades pode então recuperar esse valor ao processar a mensagem do [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) . Para uma página de propriedades, o parâmetro *lParam* da mensagem do **WM \_ INITDIALOG** é um ponteiro para a estrutura **PROPSHEETPAGE** . Recupere o ponteiro do objeto, convertendo o *lParam* da mensagem **\_ INITDIALOG do WM** em um ponteiro **PROPSHEETPAGE** e, em seguida, recuperando o membro **lParam** da estrutura **PROPSHEETPAGE** .

O exemplo de código C++ a seguir mostra como passar um objeto para uma página de propriedades.


```C++
case WM_INITDIALOG:
    {
        LPPROPSHEETPAGE pPage = (LPPROPSHEETPAGE)lParam;

        if(NULL != pPage)
        {
            CPropSheetExt *pPropSheetExt;
            pPropSheetExt = (CPropSheetExt*)pPage->lParam;

            if(pPropSheetExt)
            {
                return pPropSheetExt>OnInitDialog(wParam, lParam);
            }
        }
    }
    break;
```



Lembre-se de que depois que [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) for chamado, a folha de propriedades liberará o objeto de extensão de folha de propriedades e nunca o usará novamente. Isso significa que o objeto de extensão seria excluído antes de a página de propriedades ser exibida. Quando a página tentar acessar o ponteiro do objeto, a memória será liberada e o ponteiro não será válido. Para corrigir isso, aumente a contagem de referência para o objeto de extensão quando a página for adicionada e, em seguida, libere o objeto quando a caixa de diálogo da página de Propriedades for destruída. Isso cria outro problema porque a caixa de diálogo página de propriedades não é criada até a primeira vez em que a página é exibida. Se o usuário nunca selecionar a página de extensão, a página nunca será criada e destruída. Isso faz com que o objeto de extensão nunca seja liberado, portanto ocorre um vazamento de memória. Para evitar isso, implemente uma função de retorno de chamada de página de propriedades. Para fazer isso, adicione o sinalizador **PSP \_ USECALLBACK** ao membro **dwFlags** da estrutura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) e defina o membro **pfnCallback** da estrutura **PROPSHEETPAGE** como o endereço da função [**PropSheetPageProc**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) implementada. Quando a função **PropSheetPageProc** recebe a notificação de **\_ liberação de PSPCB** , o parâmetro *PPSP* de **PropSheetPageProc** contém um ponteiro para a estrutura **PROPSHEETPAGE** . O membro **lParam** da estrutura **PROPSHEETPAGE** contém o ponteiro de extensão que pode ser usado para liberar o objeto.

O exemplo de código C++ a seguir mostra como liberar um objeto de extensão.


```C++
UINT CALLBACK CPropSheetExt::PageCallbackProc(  HWND hWnd,
                                                UINT uMsg,
                                                LPPROPSHEETPAGE ppsp)
{
    switch(uMsg)
    {
    case PSPCB_CREATE:
        // Must return TRUE to enable the page to be created.
        return TRUE;

    case PSPCB_RELEASE:
        {
            /*
            Release the object. This is called even if the page dialog box was 
            never actually created.
            */
            CPropSheetExt *pPropSheetExt = (CPropSheetExt*)ppsp->lParam;

            if(pPropSheetExt)
            {
                pPropSheetExt->Release();
            }
        }
        break;
    }

    return FALSE;
}
```



## <a name="working-with-the-notification-object"></a>Trabalhando com o objeto de notificação

Como as páginas de extensão da folha de propriedades são exibidas em uma folha de propriedades criada por um componente desconhecido para a extensão, é necessário usar um "Gerenciador" para lidar com a transferência de dados entre as páginas de extensão e a folha de propriedades. Esse "Gerenciador" é chamado de objeto de notificação. O objeto de notificação Opera como um moderador entre as páginas individuais e a folha de propriedades.

Quando o objeto de extensão de folha de propriedades é inicializado, a extensão deve criar um objeto de notificação chamando [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj), passando o [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtido de [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) e o nome do objeto de diretório. Não é necessário incrementar a contagem de referência da interface **IDataObject** , pois o objeto de notificação criado pela função **ADsPropCreateNotifyObj** fará isso. O identificador de objeto de notificação fornecido pelo **ADsPropCreateNotifyObj** deve ser salvo para uso posterior. **ADsPropCreateNotifyObj** pode ser chamado durante **IShellExtInit:: Initialize** ou [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages). Quando a extensão da folha de propriedades é desligada, ela deve enviar uma mensagem de [**saída do WM \_ ADSPROP \_ Notify \_**](wm-adsprop-notify-exit.md) para o objeto de notificação. Isso faz com que o objeto de notificação se destrua. Isso é melhor feito quando a função [**PropSheetPageProc**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) recebe a notificação de **\_ liberação de PSPCB** .

A extensão da folha de propriedades pode obter dados além dos fornecidos pelo formato de área de transferência [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) chamando [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo). Uma das vantagens de usar o **ADsPropGetInitInfo** é que ele fornece um objeto [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) usado para trabalhar de forma programática com o objeto de diretório.

> [!Note]  
> Ao contrário da maioria dos métodos e funções COM, [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) não incrementa a contagem de referência para o objeto [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) . O **IDirectoryObject** não deve ser liberado a menos que a contagem de referência seja manualmente incrementada primeiro.

 

Quando a página de propriedades é criada pela primeira vez, a extensão deve registrar a página com o objeto de notificação chamando [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) com o identificador de janela da página.

[**ADsPropCheckIfWritable**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcheckifwritable) é uma função de utilitário que a extensão de folha de propriedades pode usar para determinar se uma propriedade pode ser gravada.

## <a name="miscellaneous"></a>Diversos

O identificador da página de propriedades é passado para o procedimento da caixa de diálogo página. A folha de propriedades é o pai direto da página de propriedades, portanto, o identificador da folha de propriedades pode ser obtido chamando a função [**GetParent**](/windows/win32/api/winuser/nf-winuser-getparent) com o identificador da página de propriedades.

Quando o conteúdo da página de extensão é alterado, a extensão deve usar a macro [**PropSheet \_ Changed**](/windows/win32/api/prsht/nf-prsht-propsheet_changed) para notificar a folha de propriedades das alterações. Em seguida, a folha de propriedades habilitará o botão Aplicar.

## <a name="multiple-selection-property-sheets"></a>Multiple-Selection folhas de propriedades

com o Windows Server 2003 e sistemas operacionais posteriores, os snap-ins administrativos do MMC de Active Directory dão suporte a extensões de folha de propriedades para vários objetos de diretório. Essas folhas de propriedades são exibidas quando as propriedades são exibidas para mais de um item por vez. A principal diferença entre uma extensão de folha de propriedades de seleção única e uma extensão de folha de propriedades de seleção múltipla é que a estrutura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) fornecida pelo formato [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) clipboard em [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) conterá mais de uma estrutura de [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .

Quando o objeto de notificação é criado, uma extensão de folha de propriedades de seleção múltipla deve passar um nome exclusivo que é fornecido pelo snap-in em vez de um nome criado pela extensão. Para obter o nome exclusivo, solicite o formato de área de transferência [**CFSTR \_ DS \_ MULTISELECTPROPPAGE**](cfstr-ds-multiselectproppage.md) do [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtido de [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize). Esses dados são um **HGLOBAL** que contém uma cadeia de caracteres Unicode terminada em nulo que é o nome exclusivo. Esse nome exclusivo é passado para a função [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) para criar o objeto de notificação. A função de exemplo **CreateADsNotificationObject** no [código de exemplo para implementação do objeto com da folha de propriedades](example-code-for-implementation-of-the-property-sheet-com-object.md) demonstra como fazer isso corretamente, bem como ser compatível com versões anteriores do snap-in que não dão suporte a folhas de propriedades de seleção múltipla.

Para folhas de propriedades de seleção múltipla, o sistema só é associado ao primeiro objeto na matriz [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) . Por isso, o [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) fornece apenas os atributos [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) e Write-graváveis para o primeiro objeto na matriz. Os outros objetos na matriz não estão associados a.

Uma extensão de folha de propriedades de seleção múltipla é registrada no atributo [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) .

## <a name="new-with-windows-server-2003"></a>novo com o Windows Server 2003

os recursos a seguir são novos com o Windows Server 2003.

Se a página de propriedades encontrar um erro, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) poderá ser chamado com os dados de erro apropriados. **ADsPropSendErrorMessage** armazenará todas as mensagens de erro em uma fila. Essas mensagens serão exibidas na próxima vez em que [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) for chamado. Quando **ADsPropShowErrorDialog** retorna, as mensagens em fila são excluídas.

Windows O servidor 2003 apresenta a função [**ADsPropSetHwndWithTitle**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwndwithtitle) . Essa função é semelhante a [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd), mas inclui o título da página. Isso habilita a caixa de diálogo de erro exibida pelo [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) para fornecer dados mais úteis ao usuário. Se a extensão da folha de propriedades usar a função **ADsPropShowErrorDialog** , a extensão deverá usar **ADsPropSetHwndWithTitle** em vez de **ADsPropSetHwnd**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de código para implementação do objeto COM da folha de propriedades](example-code-for-implementation-of-the-property-sheet-com-object.md)
</dt> </dl>

 

 