---
title: Estrutura PROPSHEETHEADER (Prsht.h)
description: Define o quadro e as páginas de uma folha de propriedades.
keywords:
- controles de Windows de estrutura PROPSHEETHEADER
topic_type:
- apiref
api_name:
- PROPSHEETHEADER
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/23/2021
ms.openlocfilehash: 719982c1e17ab74dc5c624352625d226f8f4bef90ae84dce4f2b85d5dc2713f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085116"
---
# <a name="propsheetheader--structure"></a>Estrutura PROPSHEETHEADER

Define o quadro e as páginas de uma folha de propriedades.

## <a name="syntax"></a>Sintaxe

```cpp
typedef struct {
    DWORD      dwSize;
    DWORD      dwFlags;
    HWND       hwndParent;
    HINSTANCE  hInstance;
    union {
        HICON   hIcon;
        LPCTSTR pszIcon;
    };
    LPCTSTR  pszCaption;
    UINT     nPages;
    union {
        UINT    nStartPage;
        LPCTSTR pStartPage;
    };
    union {
        LPCPROPSHEETPAGE ppsp;
        HPROPSHEETPAGE   *phpage;
    };
    PFNPROPSHEETCALLBACK pfnCallback;
    union {
        HBITMAP hbmWatermark;
        LPCTSTR pszbmWatermark;
    };
    HPALETTE  hplWatermark;
    union {
        HBITMAP hbmHeader;
        LPCSTR  pszbmHeader;
    };
} PROPSHEETHEADER, *LPPROPSHEETHEADER;
```

## <a name="members"></a>Membros

*dwSize* 

Tipo: [DWORD](../winprog/windows-data-types.md)

Tamanho, em bytes, dessa estrutura. O Gerenciador de folhas de propriedades usa esse membro para determinar qual versão da estrutura **PROPSHEETHEADER** você está usando. Para obter mais informações, consulte Comentários.

*dwFlags* 

Tipo: [DWORD](../winprog/windows-data-types.md)

Sinalizadores que indicam quais opções usar ao criar a página da folha de propriedades. Esse membro pode ser uma combinação dos valores a seguir.

| Valor | Significado |
|-------|---------|
| PSH_DEFAULT (0x00000000) | Usa o significado padrão para todos os membros da estrutura e cria uma folha de propriedades normal. Esse sinalizador tem um valor de zero e não é combinado com outros sinalizadores. |
| PSH_AEROWIZARD (0x00004000) | [Versão 6, 0](common-control-versions.md) e posterior. Cria uma folha de propriedades do assistente que usa o estilo Aero. O sinalizador de PSH_WIZARD também deve ser definido. O modelo STA (single-threaded apartment) deve ser usado. |
| PSH_HASHELP (0x00000200) | Permite que as páginas da folha de propriedades exibam um botão de **ajuda** . Você também deve definir o sinalizador PSP_HASHELP na estrutura [PROPSHEETPAGE](pss-propsheetpage.md) da página quando a página é criada. Se qualquer uma das páginas da folha de propriedades inicial habilitar um botão de **ajuda** , PSH_HASHELP será definida automaticamente. Se nenhuma das páginas iniciais habilitar um botão de **ajuda** , você deverá definir explicitamente PSH_HASHELP se desejar ter botões de ajuda em todas as páginas que possam ser adicionadas posteriormente. Não há suporte para esse sinalizador em conjunto com PSH_AEROWIZARD.|
| PSH_HEADER (0x00080000) | [Versão 5,80](common-control-versions.md) e posterior. Indica que um bitmap de cabeçalho será usado com um assistente de Wizard97. Você também deve definir o sinalizador PSH_WIZARD97. Se o sinalizador PSH_USEHBMHEADER for definido, o bitmap do cabeçalho será obtido do membro *hbmHeader* . Caso contrário, o bitmap do cabeçalho será obtido do membro *pszbmHeader* . Não há suporte para esse sinalizador em conjunto com PSH_AEROWIZARD. |
| PSH_HEADERBITMAP (0x08000000) | [Versão 6, 0](common-control-versions.md) e posterior. O membro *pszbmHeader* especifica um bitmap que é exibido na área de cabeçalho. Deve ser usado em combinação com PSH_AEROWIZARD. |
| PSH_MODELESS (0x00000400) | Faz com que a função [folha](/windows/win32/api/prsht/nf-prsht-propertysheeta) crie a folha de propriedades como uma caixa de diálogo sem janela restrita em vez de como uma caixa de diálogo modal. Quando esse sinalizador é definido, [folha](/windows/win32/api/prsht/nf-prsht-propertysheeta) retorna imediatamente depois que a caixa de diálogo é criada, e o valor de retorno de [folha](/windows/win32/api/prsht/nf-prsht-propertysheeta) é o identificador da janela para a caixa de diálogo da folha de propriedades. Não há suporte para esse sinalizador em conjunto com PSH_AEROWIZARD. |
| PSH_NOAPPLYNOW (0x00000080) | Remove o botão **aplicar** . Não há suporte para esse sinalizador em conjunto com PSH_AEROWIZARD. |
| PSH_NOCONTEXTHELP (0x02000000) | [Versão 5,80](common-control-versions.md) e posterior. Remove o botão de ajuda contextual ("?"), que geralmente está presente na barra de legenda das folhas de propriedades. Este sinalizador não é válido para assistentes. Consulte [sobre folhas de propriedades](property-sheets.md) para obter uma discussão de como remover o botão de **ajuda** da barra de legenda para versões anteriores dos controles comuns. Não há suporte para esse sinalizador em conjunto com PSH_AEROWIZARD. |
| PSH_NOMARGIN (0x10000000) | [Versão 6, 0](common-control-versions.md) ou posterior. Especifica que nenhuma margem é inserida entre a página e o quadro. Deve ser usado em combinação com PSH_AEROWIZARD. |
| PSH_PROPSHEETPAGE (0x00000008) | Usa o membro *PPSP* e ignora o membro *phpage* ao criar as páginas para a folha de propriedades. |
| PSH_PROPTITLE (0x00000001) | Indica que *pszCaption* é o nome do item para o qual as propriedades estão sendo mostradas. Windows torna um ajuste de versão e de idioma dependente da legenda. Por exemplo, em inglês, a frase "Propriedades de" é anexada a um *pszCaption* não vazio (e, se o *pszCaption* produz uma legenda vazia, o título é simplesmente "Propriedades"). Se esse sinalizador for omitido, o pszCaption será usado inalterado.  |
| PSH_RESIZABLE (0x04000000) | Permite que o assistente seja redimensionado pelo usuário. Os botões maximizar e minimizar aparecem no quadro do assistente e o quadro é dimensionável. Para usar esse sinalizador, você também deve definir PSH_AEROWIZARD. |
| PSH_RTLREADING (0x00000800) | Define a folha de propriedades ou a janela do assistente como a ordem de leitura da direita para a esquerda (RTL), apropriada para linguagens como hebraico e árabe. Se esse sinalizador não for especificado, a janela da folha de propriedades padrão será a ordem de leitura da esquerda para a direita (EPD) e as janelas do assistente corresponderão à ordem de leitura da página atual. |
| PSH_STRETCHWATERMARK (0x00040000) | Alonga a marca-d ' água nos assistentes de estilo Wizard97. Não há suporte para esse sinalizador em conjunto com PSH_AEROWIZARD. Esse sinalizador de estilo só é incluído para fornecer compatibilidade com versões anteriores para determinados aplicativos. Seu uso não é recomendado e só é compatível com as versões 4,0 e 4, 1 dos controles comuns. Com os controles comuns versão 5,80 e posteriores, esse sinalizador é ignorado. |
| PSH_USECALLBACK (0x00000100) | Chama a função especificada pelo parâmetro *pfnCallback* quando determinados eventos ocorrem. Para obter mais informações, consulte a descrição da função de retorno de chamada [PFNPROPSHEETCALLBACK](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) . |
| PSH_USEHBMHEADER (0x00100000) | [Versão 5,80](common-control-versions.md). Obtém o bitmap de cabeçalho do membro *hbmHeader* em vez do membro *pszbmHeader* . Você também deve definir o sinalizador PSH_AEROWIZARD ou o sinalizador PSH_WIZARD97 junto com o sinalizador PSH_HEADER. |
| PSH_USEHBMWATERMARK (0x00010000) | [Versão 5,80](common-control-versions.md). Obtém o bitmap de marca d' água do membro *hbmWatermark* em vez do membro *pszbmWatermark* . Você também deve definir PSH_WIZARD97 e PSH_WATERMARK. Não há suporte para esse sinalizador em conjunto com PSH_AEROWIZARD. |
| PSH_USEHICON (0x00000002) | Usa *HICON* como o ícone pequeno na barra de título da caixa de diálogo da folha de propriedades. |
| PSH_USEHPLWATERMARK (0x00020000) | [Versão 5,80](common-control-versions.md). Usa a estrutura **HPALETTE** apontada pelo membro *hplWatermark* em vez da paleta padrão para desenhar o bitmap de marca d' água e/ou o bitmap de cabeçalho para um assistente de Wizard97. Você também deve definir PSH_WIZARD97 e PSH_WATERMARK ou PSH_HEADER. Não há suporte para esse sinalizador em conjunto com PSH_AEROWIZARD.  |
| PSH_USEICONID (0x00000004) | Usa *pszIcon* como o nome do recurso de ícone para carregar e usar como o ícone pequeno na barra de título da caixa de diálogo da folha de propriedades. |
| PSH_USEPAGELANG (0x00200000) | [Versão 5,80](common-control-versions.md). Especifica que o idioma da folha de propriedades será obtido do recurso da primeira página. Essa página deve ser especificada pelo identificador de recurso. |
| PSH_USEPSTARTPAGE (0x00000040) | Usa o membro *pStartPage* em vez do membro *nStartPage* ao exibir a página inicial da folha de propriedades. |
| PSH_WATERMARK (0x00008000) | [Versão 5,80](common-control-versions.md). Especifica que um bitmap de marca d' água será usado com um assistente de Wizard97 em páginas que têm o estilo de PSP_HIDEHEADER. Você também deve definir o sinalizador PSH_WIZARD97. O bitmap de marca d' água é obtido do membro *pszbmWatermark* , a menos que PSH_USEHBMWATERMARK esteja definido. Nesse caso, o bitmap do cabeçalho é obtido do membro *hbmWatermark* . Não há suporte para esse sinalizador em conjunto com PSH_AEROWIZARD.  |
| PSH_WIZARD (0x00000020) | Cria uma folha de propriedades do assistente. Ao usar PSH_AEROWIZARD, você também deve definir esse sinalizador. |
| PSH_WIZARD97 (0x01000000) | [Versão 5,80](common-control-versions.md). Cria uma folha de propriedades estilo Wizard97, que dá suporte a bitmaps no cabeçalho de páginas interiores e no lado esquerdo das páginas exteriores. Não há suporte para esse sinalizador em conjunto com PSH_AEROWIZARD. |
| PSH_WIZARDCONTEXTHELP (0x00001000) | Adiciona um botão de **ajuda** contextual ("?"), que geralmente está ausente da barra de legenda de um assistente. Este sinalizador não é válido para folhas de propriedades regulares. Não há suporte para esse sinalizador em conjunto com PSH_AEROWIZARD. |
| PSH_WIZARDHASFINISH (0x00000010)  | Sempre exibe o botão **concluir** no assistente. Você também deve definir PSH_WIZARD, PSH_WIZARD97 ou PSH_AEROWIZARD. |
| PSH_WIZARD_LITE (0x00400000) | [Versão 5,80](common-control-versions.md). Usa o estilo Wizard-Lite. Esse estilo é semelhante à aparência para PSH_WIZARD97, mas é implementado de forma muito semelhante a PSH_WIZARD. Há algumas restrições sobre como as páginas são formatadas. Por exemplo, não há nenhuma borda imposta e o estilo de PSH_WIZARD_LITE não pinta os bitmaps de cabeçalho e marca d' água para você da maneira que o Wizard97 faz. Não há suporte para esse sinalizador em conjunto com PSH_AEROWIZARD. |

*hwndParent* 

Digite: [HWND](../winprog/windows-data-types.md)

Identificador para a janela do proprietário da folha de propriedades.

*hInstance* 

Tipo: [HINSTANCE](../winprog/windows-data-types.md)

Identificador para a instância da qual carregar o ícone, o recurso de cadeia de caracteres do título, o nome da página inicial, o bitmap do cabeçalho ou a marca-d ' água. Se o membro *pszIcon*, *pszCaption*, *pStartPage*, *pszbmHeader* ou *pszbmWatermark* identificar um recurso a ser carregado, esse membro deverá ser especificado.

*hIcon* 

Tipo: [HICON](../winprog/windows-data-types.md)

Manipule o ícone a ser usado como ícone pequeno na barra de título da caixa de diálogo da folha de propriedades. Esse membro será usado se o membro *dwFlags* incluir PSH_USEHICON. Esse membro é declarado como uma União com *pszIcon*.

*pszIcon* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

O recurso de ícone a ser usado como ícone pequeno na barra de título da caixa de diálogo da folha de propriedades. Esse membro será usado se o membro *dwFlags* incluir PSH_USEICONID. Esse membro pode especificar o identificador do recurso de ícone ou o endereço da cadeia de caracteres que especifica o nome do recurso de ícone. Em ambos os casos, o ícone é carregado a partir da instância fornecida pelo membro *HINSTANCE* . Esse membro é declarado como uma União com *HICON*.

*pszCaption* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

Título da caixa de diálogo da folha de propriedades. Esse membro pode especificar o identificador de um recurso de cadeia de caracteres (carregado da instância especificada pelo membro *HINSTANCE* ) ou o endereço de uma cadeia de caracteres que especifica o título. Se o membro *dwFlags* incluir PSH_PROPTITLE, as **Propriedades de cadeia de caracteres para** serão inseridas no início do título. Este campo é ignorado para assistentes de Wizard97. Para assistentes Aero, a cadeia de caracteres sozinha é usada para a legenda, independentemente de o sinalizador PSH_PROPTITLE ser definido.

*nPages* 

Tipo: [uint](../winprog/windows-data-types.md)

Número de páginas de folha de propriedades fornecidas na matriz *PPSP* ou *phpage* .

*nStartPage* 

Tipo: [uint](../winprog/windows-data-types.md)

Índice de base zero da página inicial que aparece quando a caixa de diálogo da folha de propriedades é criada. Esse membro será usado se o membro *dwFlags* não incluir o sinalizador PSH_USEPSTARTPAGE. Esse membro é declarado como uma União com *pStartPage*.

*pStartPage* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

Nome da página inicial que aparece quando a caixa de diálogo da folha de propriedades é criada. Esse membro será usado se o membro *dwFlags* incluir o sinalizador PSH_USESTARTPAGE. Esse membro pode especificar o identificador de um recurso de cadeia de caracteres (carregado da instância especificada pelo membro *HINSTANCE* ) ou o endereço de uma cadeia de caracteres que especifica o nome. O nome da página inicial é comparado com as legendas das páginas. Esse membro é declarado como uma União com *nStartPage*.

*ppsp* 

Tipo: **LPCPROPSHEETPAGE**

Ponteiro para uma matriz de estruturas [PROPSHEETPAGE](pss-propsheetpage.md) que definem as páginas na folha de propriedades. Se o membro *dwFlags* não incluir PSH_PROPSHEETPAGE, esse membro será ignorado. Observe que a estrutura **PROPSHEETPAGE** é de tamanho variável. Os aplicativos que analisam a matriz apontada pelo *PPSP* devem levar em conta o tamanho de cada página. Esse membro é declarado como uma União com *phpage*.

*phpage* 

Tipo: **HPROPSHEETPAGE \***

Ponteiro para uma matriz de identificadores para as páginas da folha de propriedades. Esse membro será usado se o membro *dwFlags* não incluir PSH_PROPSHEETPAGE. Cada identificador deve ter sido criado por uma chamada anterior para a função [CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) . Quando a função [folha](/windows/win32/api/prsht/nf-prsht-propertysheeta) retornar, quaisquer identificadores HPROPSHEETPAGE na matriz *phpage* serão destruídos. Esse membro é declarado como uma União com *PPSP*.

*pfnCallback* 

Tipo: **PFNPROPSHEETCALLBACK**

Ponteiro para uma função de retorno de chamada definida pelo aplicativo que é chamada quando determinados eventos ocorrem. Para obter mais informações sobre a função de retorno de chamada, consulte a descrição da função de retorno de chamada [PFNPROPSHEETCALLBACK](/windows/win32/api/prsht/nc-prsht-pfnpropsheetcallback) . Se o membro *dwFlags* não incluir PSH_USECALLBACK, esse membro será ignorado.

*hbmWatermark* 

Tipo: [HBITMAP](../winprog/windows-data-types.md)

[Versão 5,80](common-control-versions.md) ou posterior. Identificador para o bitmap de marca d' água. Se o membro *dwFlags* não incluir PSH_USEHBMWATERMARK, esse membro será ignorado.

*pszbmWatermark* 

Tipo: [LPCTSTR](../winprog/windows-data-types.md)

[Versão 5,80](common-control-versions.md) ou posterior. Recurso de bitmap a ser usado como a marca d' água. Esse membro pode especificar o identificador do recurso de bitmap ou o endereço da cadeia de caracteres que especifica o nome do recurso de bitmap. Se o membro *dwFlags* incluir PSH_USEHBMWATERMARK, esse membro será ignorado.

*hplWatermark*

Tipo: [HPALETTE](../winprog/windows-data-types.md)

[Versão 5,80](common-control-versions.md) ou posterior. Estrutura **HPALETTE** usada para desenhar o bitmap de marca d' água e/ou o bitmap do cabeçalho. Se o membro *dwFlags* não incluir PSH_USEHPLWATERMARK, esse membro será ignorado.

*hbmHeader*

Tipo: [HBITMAP](../winprog/windows-data-types.md)

[Versão 5,80](common-control-versions.md) ou posterior. Identificador para o bitmap de cabeçalho. Se o membro *dwFlags* não incluir PSH_USEHBMHEADER, esse membro será ignorado.

*pszbmHeader*

Tipo: [LPCSTR](../winprog/windows-data-types.md)

[Versão 5,80](common-control-versions.md) ou posterior. Recurso de bitmap a ser usado como o cabeçalho. Esse membro pode especificar o identificador do recurso de bitmap ou o endereço da cadeia de caracteres que especifica o nome do recurso de bitmap. Se o membro *dwFlags* incluir PSH_USEHBMHEADER, esse membro será ignorado.

## <a name="remarks"></a>Comentários

Se o usuário escolher uma configuração como fontes grandes, o que amplia a caixa de diálogo, a marca d' água pintada nas páginas de início e término também será ampliada. O tamanho e a posição do bitmap original permanecerão os mesmos. A área adicional será preenchida com a cor do pixel no canto superior esquerdo do bitmap.

Os estilos PSH_WIZARD, PSH_WIZARD97 e PSH_WIZARD_LITE são mutuamente incompatíveis. Somente um desses sinalizadores de estilo deve ser definido. PSH_AEROWIZARD deve ser combinado com PSH_WIZARD.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows \[Somente aplicativos da área de trabalho do vista\]                                    |
| Servidor mínimo com suporte | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]                              |
| Cabeçalho                   | Prsht. h |
| Nomes Unicode e ANSI                   | **PROPSHEETHEADERW** (Unicode) e **PROPSHEETHEADERA** (ANSI) |
