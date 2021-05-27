---
title: Estrutura PROPSHEETPAGE (Prsht.h)
description: Define uma página em uma folha de propriedades.
keywords:
- Controles do Windows da estrutura PROPSHEETPAGE
topic_type:
- apiref
api_name:
- PROPSHEETPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/23/2021
ms.openlocfilehash: 78e1d1e4e6b4b2067083443bdb5dc4db5df59558
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550341"
---
# <a name="propsheetpage-structure"></a>Estrutura PROPSHEETPAGE

Define uma página em uma folha de propriedades.

## <a name="syntax"></a>Sintaxe

```cpp
typedef struct {
    DWORD      dwSize;
    DWORD      dwFlags;
    HINSTANCE  hInstance;
    union {
        LPCSTR                 pszTemplate;
        PROPSHEETPAGE_RESOURCE pResource;
    };
    union {
        HICON  hIcon;
        LPCSTR pszIcon;
    };
    LPCSTR          pszTitle;
    DLGPROC         pfnDlgProc;
    LPARAM          lParam;
    LPFNPSPCALLBACK pfnCallback;
    UINT            *pcRefParent;
    LPCTSTR         pszHeaderTitle;
    LPCTSTR         pszHeaderSubTitle;
    HANDLE          hActCtx;
    union 
    {
        HBITMAP     hbmHeader;
        LPCSTR      pszbmHeader;
    }
} PROPSHEETPAGE, *LPPROPSHEETPAGE;
```

## <a name="members"></a>Membros

*Dwsize* 

Tipo: [DWORD](../winprog/windows-data-types.md)

Tamanho, em bytes, dessa estrutura.

*dwFlags* 

Tipo: [DWORD](../winprog/windows-data-types.md)

Sinalizadores que indicam quais opções usar ao criar a página de folha de propriedades. Esse membro pode ser uma combinação dos valores a seguir.

| Valor | Significado |
|-------|---------|
| PSP_DEFAULT | Usa o significado padrão para todos os membros da estrutura. Não há suporte para esse sinalizador ao usar o assistente de estilo Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_DLGINDIRECT | Cria a página do modelo de caixa de diálogo na memória apontada pelo *membro pResource.* A [função PropertySheet](/windows/win32/api/prsht/nf-prsht-propertysheeta) presume que o modelo que está na memória não está protegido por gravação. Um modelo somente leitura causará uma exceção em algumas versões do Windows. |
| PSP_HASHELP | Habilita o botão **Ajuda da folha** de propriedades quando a página está ativa. Não há suporte para esse sinalizador ao usar o assistente de estilo Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_HIDEHEADER | [Versão 5,80](common-control-versions.md) e posterior. Faz com que a folha de propriedades do assistente oculte a área do cabeçalho quando a página é selecionada. Se uma marca d' água tiver sido fornecida, ela será pintada no lado esquerdo da página. Esse sinalizador deve ser definido para as páginas de boas-vindas e de conclusão e omitido para páginas interiores. Não há suporte para esse sinalizador ao usar o assistente de estilo Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_PREMATURE | [Versão 4,71](common-control-versions.md) ou posterior. Faz com que a página seja criada quando a folha de propriedades é criada. Se esse sinalizador não for especificado, a página não será criada até que seja selecionada na primeira vez. Não há suporte para esse sinalizador ao usar o assistente de estilo Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_RTLREADING | Inverte a direção na qual *pszTitle* é exibido. Janelas normais exibem todo o texto, incluindo *pszTitle*, da esquerda para a direita (EPD). Para idiomas como hebraico ou árabe que lêem da direita para a esquerda (RTL), uma janela pode ser espelhada e todo o texto será exibido em DPE. Se PSP_RTLREADING for definido, *pszTitle* lerá DPE em uma janela pai normal e EPD em uma janela pai espelhada. |
| PSP_USECALLBACK | Chama a função especificada pelo membro *pfnCallback* ao criar ou destruir a página da folha de propriedades definida por essa estrutura. |
| PSP_USEFUSIONCONTEXT | [Versão 6,0](common-control-versions.md) e posterior. Use um contexto de ativação. Para usar um contexto de ativação, você deve definir esse sinalizador e atribuir o handle de contexto de ativação a *hActCtx.* Consulte os Comentários. |
| PSP_USEHEADERSUBTITLE | [Versão 5.80](common-control-versions.md) ou posterior. Exibe a cadeia de caracteres apontada pelo membro *pszHeaderSubTitle* como o subtítulo da área de título de uma página do Assistente97. Para usar esse sinalizador, você também deve definir o sinalizador PSH_WIZARD97 no membro *dwFlags* da estrutura [PROPSHEETHEADER](pss-propsheetheader.md) associada. O PSP_USEHEADERSUBTITLE sinalizador será ignorado se PSP_HIDEHEADER estiver definido. Em assistentes de estilo Aero, o título aparece próximo à parte superior da área do cliente. |
| PSP_USEHEADERTITLE | [Versão 5.80](common-control-versions.md) ou posterior. Exibe a cadeia de caracteres apontada pelo membro *pszHeaderTitle* como o título no título de uma página interior do Assistente97. Você também deve definir o PSH_WIZARD97 no *membro dwFlags* da estrutura [PROPSHEETHEADER](pss-propsheetheader.md) associada. O PSP_USEHEADERTITLE de dados será ignorado se PSP_HIDEHEADER estiver definido. Não há suporte para esse sinalizador ao usar o assistente de estilo Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_USEHICON | Usa *hIcon* como o ícone pequeno na guia da página. Não há suporte para esse sinalizador ao usar o assistente de estilo Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)).  |
| PSP_USEICONID | Usa *pszIcon* como o nome do recurso de ícone para carregar e usar como o ícone pequeno na guia da página. Não há suporte para esse sinalizador ao usar o assistente de estilo Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |
| PSP_USEREFPARENT | Mantém a contagem de referência especificada pelo membro *pcRefParent* para o tempo de vida da página da folha de propriedades criada a partir dessa estrutura. |
| PSP_USETITLE | Usa o membro *pszTitle* como o título da caixa de diálogo da folha de propriedades em vez do título armazenado no modelo da caixa de diálogo. Não há suporte para esse sinalizador ao usar o assistente de estilo Aero ([PSH_AEROWIZARD](pss-propsheetheader.md)). |

*hInstance* 

Tipo: [HINSTANCE](../winprog/windows-data-types.md)

Identificador para a instância da qual carregar um recurso de ícone ou de cadeia de caracteres. Se o membro *pszIcon*, *pszTitle*, *pszHeaderTitle* ou *pszHeaderSubTitle* identificar um recurso a ser carregado, *HINSTANCE* deverá ser especificado.

*pszTemplate* 

Tipo: [LPCSTR](../winprog/windows-data-types.md)

Modelo de caixa de diálogo a ser usado para criar a página. Esse membro pode especificar o identificador de recurso do modelo ou o endereço de uma cadeia de caracteres que especifica o nome do modelo. Se o sinalizador de PSP_DLGINDIRECT no membro *dwFlags* for definido, *pszTemplate* será ignorado. Esse membro é declarado como uma União com pré *-fonte*.

*origem* 

Tipo: **LPCDLGTEMPLATE**

Ponteiro para um modelo de caixa de diálogo na memória. A função [folha](/windows/win32/api/prsht/nf-prsht-propertysheeta) pressupõe que o modelo não está protegido contra gravação. Um modelo somente leitura causará uma exceção em algumas versões do Windows. Para usar esse membro, você deve definir o sinalizador PSP_DLGINDIRECT no *membro dwFlags.* Esse membro é declarado como uma união com *pszTemplate*.

*Hicon* 

Tipo: [HICON](../winprog/windows-data-types.md)

Lidar com o ícone a ser usado como o ícone na guia da página. Se o *membro dwFlags* não incluir PSP_USEHICON, esse membro será ignorado. Esse membro é declarado como uma união com *pszIcon*.

*pszIcon* 

Tipo: [LPCSTR](../winprog/windows-data-types.md)

Recurso de ícone a ser usado como o ícone na guia da página. Esse membro pode especificar o identificador do recurso de ícone ou o endereço da cadeia de caracteres que especifica o nome do recurso de ícone. Para usar esse membro, você deve definir o sinalizador PSP_USEICONID no *membro dwFlags.* Esse membro é declarado como uma união com *hIcon*.

*Psztitle* 

Tipo: [LPCSTR](../winprog/windows-data-types.md)

Título da caixa de diálogo folha de propriedades. Esse título substitui o título especificado no modelo de caixa de diálogo. Esse membro pode especificar o identificador de um recurso de cadeia de caracteres ou o endereço de uma cadeia de caracteres que especifica o título. Para usar esse membro, você deve definir o sinalizador PSP_USETITLE no *membro dwFlags.*

*pfnDlgProc* 

Tipo: **DLGPROC**

Ponteiro para o procedimento da caixa de diálogo da página. Como as páginas são criadas como caixas de diálogo sem janela restrita, o procedimento da caixa de diálogo não deve chamar a função [EndDialog](/windows/win32/api/winuser/nf-winuser-enddialog) .

*lParam* 

Tipo: [lParam](../winprog/windows-data-types.md)

Quando a página é criada, uma cópia da estrutura **PROPSHEETPAGE** da página é passada para o procedimento da caixa de diálogo com uma mensagem [WM_INITDIALOG](../dlgbox/wm-initdialog.md) . O membro *lParam* é fornecido para permitir que você passe informações específicas do aplicativo para o procedimento da caixa de diálogo. Ele não tem nenhum efeito na própria página.

*pfnCallback* 

Tipo: **LPFNPSPCALLBACK**

Ponteiro para uma função de retorno de chamada definida pelo aplicativo que é chamada quando a página é criada e quando está prestes a ser destruída. Para obter mais informações sobre a função de retorno de chamada, consulte [função de retorno de chamada LPFNPSPCALLBACKA](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka). Para usar esse membro, você deve definir o sinalizador PSP_USECALLBACK no membro *dwFlags* .

*pcRefParent* 

Tipo: [uint *](../winprog/windows-data-types.md)

Aponta para o valor da contagem de referência. Para usar esse membro, você deve definir o sinalizador PSP_USEREFPARENT no membro *dwFlags* .

> [!NOTE]
> Quando uma página de folha de propriedades é criada, o valor apontado por *pcRefParent* é incrementado. Você cria uma página de folha de Propriedades implicitamente definindo o sinalizador PSH_PROPSHEETPAGE no membro *dwFlags* de [PROPSHEETHEADER](pss-propsheetheader.md) e chamando a função [folha](/windows/win32/api/prsht/nf-prsht-propertysheeta) . Você pode fazer isso explicitamente usando a função [CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) . Quando uma página de folha de propriedades é destruída, o valor apontado pelo membro *pcRefParent* é decrementado. Isso ocorre automaticamente quando a folha de propriedades é destruída. Você pode destruir explicitamente uma página de folha de propriedades usando a [função DestroyPropertySheetPage.](/windows/win32/api/prsht/nf-prsht-destroypropertysheetpage)

*pszHeaderTitle* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

[Versão 5.80](common-control-versions.md) ou posterior. Título da área de título. Para usar esse membro no assistente no estilo Wizard97, você também deve fazer o seguinte:

* Defina PSP_USEHEADERTITLE sinalizador no *membro dwFlags.*
* Defina PSH_WIZARD97 sinalizador no *membro dwFlags* da estrutura [PROPSHEETHEADER da](pss-propsheetheader.md) página.
* Certifique-se de PSP_HIDEHEADER sinalizador no membro *dwFlags* não está definido.

*pszHeaderSubTitle* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

[Versão 5.80](common-control-versions.md) ou posterior. Subtítulo da área de título. Para usar esse membro, você deve fazer o seguinte:

* Defina PSP_USEHEADERSUBTITLE sinalizador no *membro dwFlags.*
* Defina PSH_WIZARD97 sinalizador no *membro dwFlags* da estrutura [PROPSHEETHEADER da](pss-propsheetheader.md) página.
* Certifique-se de PSP_HIDEHEADER sinalizador no membro *dwFlags* não está definido.

> [!NOTE]
> Esse membro é ignorado ao usar o assistente de estilo Aero ([PSH_AEROWIZARD](pss-propsheetheader.md))

*hActCtx* 

Tipo: [identificador](../winprog/windows-data-types.md)

[Versão 6,0](common-control-versions.md) ou posterior. Um identificador de contexto de ativação. Defina esse membro como o identificador que é retornado quando você cria o contexto de ativação com [CreateActCtx](/windows/win32/api/winbase/nf-winbase-createactctxa). O sistema ativará esse contexto antes de criar a caixa de diálogo. Você não precisará usar esse membro se usar um manifesto global.

*hbmHeader* 

Tipo: [HBITMAP](../winprog/windows-data-types.md)

Esse membro é declarado como uma União com *pszbmHeader*.

*pszbmHeader*

Tipo: [LPCSTR](../winprog/windows-data-types.md)

Esse membro é declarado como uma União com *hbmHeader*.

## <a name="remarks"></a>Comentários

Comctl32.dll versão 6 e posterior não são redistribuíveis. Para usar Comctl32.dll versão 6 ou posterior, especifique o arquivo. dll em um manifesto. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows Vista\]                                    |
| Servidor mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows Server 2003\]                              |
| Cabeçalho                   | Prsht. h |
| Nomes Unicode e ANSI                   | **PROPSHEETHEADERW** (Unicode) e **PROPSHEETHEADERA** (ANSI) |