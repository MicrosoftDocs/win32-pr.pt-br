---
title: Caixa de diálogo Cor
description: Exibe uma caixa de diálogo modal que permite ao usuário escolher um valor de cor específico.
ms.assetid: 248586b5-5068-4021-8407-56eb79243789
keywords:
- entrada do usuário, biblioteca de caixa de diálogo comum
- capturando entrada do usuário, biblioteca de caixa de diálogo comum
- Biblioteca de caixa de diálogo comum
- caixas de diálogo comuns
- Caixa de diálogo Cor
- caixa de diálogo cor parcial
- caixa de diálogo cor completa
- Personalizando a caixa de diálogo cor
- Modelo de cor RGB
- Modelo de cor HSL
- luminosidade da saturação de matiz (HSL)
- HSL (luminosidade de saturação de matiz)
- RGB (vermelho verde azul)
- vermelho verde azul (RGB)
- caixa de diálogo ganchos, cor
- caixas de diálogo predefinidas
- caixas de diálogo, cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb90150f49ea7bed4edac53af40ba89e0459946
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/19/2020
ms.locfileid: "104559551"
---
# <a name="color-dialog-box"></a>Caixa de diálogo Cor

Exibe uma caixa de diálogo modal que permite ao usuário escolher um valor de cor específico. O usuário pode escolher uma cor de um conjunto de paletas de cores básicas ou personalizadas. Como alternativa, o usuário pode gerar um valor de cor modificando os valores de cor RGB ou matiz, saturação, luminosidade (HSL) da interface do usuário da caixa de diálogo. A caixa de diálogo **cor** retorna o valor RGB da cor selecionada pelo usuário.

Você cria e exibe uma caixa de diálogo de **cor** inicializando uma estrutura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) e passando a estrutura para a função [**CHOOSECOLOR**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) . Ao definir valores de parâmetros diferentes para a estrutura **CHOOSECOLOR** , você pode afetar como a caixa de diálogo cor é exibida. Por exemplo, você pode exibir uma versão completa ou parcial da interface do usuário da caixa de diálogo. A ilustração a seguir mostra a versão completa da interface do usuário da caixa de diálogo **cor** .

![caixa de diálogo de cor](images/colordialogboxxp.png)

Se o usuário clicar no botão **OK** , [**CHOOSECOLOR**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) retornará **true**. O membro **rgbResult** da estrutura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) contém o valor de cor RGB da cor selecionada pelo usuário. O valor de cor RGB especifica as intensidades das cores de vermelho, verde e azul individuais que compõem a cor selecionada. Os valores individuais variam de 0 a 255. Use as macros [**GetRValue**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue)e [**GetBValue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue) para extrair cores individuais de um valor de cor RGB.

Se o usuário cancelar a caixa de diálogo **cor** ou ocorrer um erro, [**CHOOSECOLOR**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) retornará **false** e o membro **rgbResult** não será definido. Para determinar a causa do erro, chame a função [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar o valor de erro estendido.

Os seguintes assuntos são abordados nesta seção

-   [Caixas de diálogo de cor completa e parcial](#full-and-partial-color-dialog-boxes)
-   [Personalizando a caixa de diálogo cor](#customizing-the-color-dialog-box)
    -   [Para fornecer um modelo personalizado para a caixa de diálogo cor](#to-provide-a-custom-template-for-the-color-dialog-box)
    -   [Para habilitar um procedimento de gancho para a caixa de diálogo cor](#to-enable-a-hook-procedure-for-the-color-dialog-box)
-   [Modelos de cores usados pela caixa de diálogo cor](#color-models-used-by-the-color-dialog-box)
    -   [Modelo de cor RGB](#rgb-color-model)
    -   [Modelo de cor HSL](#hsl-color-model)
    -   [Convertendo valores HSL em valores RGB](#converting-hsl-values-to-rgb-values)

## <a name="full-and-partial-color-dialog-boxes"></a>Caixas de diálogo de cor completa e parcial

A caixa de diálogo cor tem uma versão completa e uma versão parcial da interface do usuário. A versão completa inclui os controles básicos e tem controles adicionais que permitem ao usuário criar cores personalizadas. A versão parcial tem controles que exibem as paletas de cores básica e personalizada das quais o usuário pode selecionar um valor de cor.

A versão parcial da caixa de diálogo cor inclui um botão **definir cores personalizadas** . O usuário pode clicar nesse botão para exibir a versão completa. Você pode direcionar a caixa de diálogo cor para sempre exibir a versão completa definindo o sinalizador **CC \_ FULLOPEN** no membro **flags** da estrutura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) . Para impedir que o usuário crie cores personalizadas, você pode definir o **sinalizador \_ PREVENTFULLOPEN do CC** para desabilitar o botão **definir cores personalizadas** .

As cores básicas representam uma seleção das cores disponíveis no dispositivo especificado. O número real de cores exibidas é determinado pelo driver de vídeo. Por exemplo, um driver VGA exibe 48 cores e um driver de vídeo monocromático exibe apenas 16.

As cores personalizadas são aquelas que você especifica ou que o usuário cria. Ao criar uma caixa de diálogo de cor, você deve usar o membro **lpCustColors** da estrutura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) para especificar os valores iniciais para as 16 cores personalizadas. Se a versão completa da caixa de diálogo cor estiver aberta, o usuário poderá criar uma cor personalizada por um dos seguintes métodos:

-   Movendo o cursor no controle do espectro de cores e o controle deslizante de luminosidade
-   Digitando valores RGB nos controles de edição **vermelho**, **verde** e **azul**
-   Digitando valores HSL nos controles de edição **matiz**, **SAT** e **Lum**

Para adicionar uma nova cor personalizada à exibição de cores personalizadas, o usuário pode clicar no botão **Adicionar às cores personalizadas** . Isso também faz com que a caixa de diálogo Copie o valor RGB da nova cor para o elemento correspondente na matriz apontada pelo membro **lpCustColors** . Para preservar novas cores personalizadas entre chamadas para [**CHOOSECOLOR**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)), você deve alocar memória estática para a matriz. Para obter mais informações sobre os modelos de cores RGB e HSL, consulte [modelos de cores usados pela caixa de diálogo cor](#color-models-used-by-the-color-dialog-box).

## <a name="customizing-the-color-dialog-box"></a>Personalizando a caixa de diálogo cor

Para personalizar uma caixa de diálogo de cores, você pode usar qualquer um dos seguintes métodos:

-   Especificar valores na estrutura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) ao criar a caixa de diálogo
-   Fornecer um modelo personalizado
-   Fornecer um procedimento de gancho

Você pode modificar a aparência e o comportamento da caixa de diálogo cor definindo sinalizadores no membro **flags** da estrutura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) . Por exemplo, você pode definir o sinalizador **CC \_ SOLIDCOLOR** para direcionar a caixa de diálogo para exibir apenas cores sólidas. Para fazer com que a caixa de diálogo Selecione inicialmente uma cor diferente de preto, defina o sinalizador **CC \_ RGBINIT** e especifique uma cor no membro **rgbResult** .

Você pode fornecer um modelo personalizado para a caixa de diálogo cor, por exemplo, se desejar incluir controles adicionais que sejam exclusivos para seu aplicativo. A função [**CHOOSECOLOR**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) usa o modelo personalizado no lugar do modelo padrão.

### <a name="to-provide-a-custom-template-for-the-color-dialog-box"></a>Para fornecer um modelo personalizado para a caixa de diálogo cor

1.  Crie o modelo personalizado modificando o modelo padrão especificado no arquivo Color. Dlg. Os identificadores de controle usados no modelo de caixa de diálogo cor padrão são definidos no arquivo Color. Dlg.
2.  Use a estrutura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) para habilitar o modelo da seguinte maneira:
    -   Se o modelo personalizado for um recurso em um aplicativo ou biblioteca de vínculo dinâmico, defina o sinalizador de **\_ habilitação de CC** no membro **flags** . Use os membros **HINSTANCE** e **lpTemplateName** da estrutura para identificar o módulo e o nome do recurso.

        -Ou-

    -   Se o modelo personalizado já estiver na memória, defina o **sinalizador \_ ENABLETEMPLATEHANDLE do CC** . Use o membro **HINSTANCE** para identificar o objeto de memória que contém o modelo.

Você pode fornecer um procedimento de gancho [**CCHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc) para a caixa de diálogo cor. O procedimento de gancho pode processar mensagens enviadas para a caixa de diálogo. Ele também pode usar mensagens registradas para controlar o comportamento da caixa de diálogo. Se você usar um modelo personalizado para definir controles adicionais, deverá fornecer um procedimento de gancho para processar a entrada para seus controles.

### <a name="to-enable-a-hook-procedure-for-the-color-dialog-box"></a>Para habilitar um procedimento de gancho para a caixa de diálogo cor

1.  Defina o **sinalizador \_ ENABLEHOOK do CC** no membro **flags** da estrutura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) .
2.  Especifique o endereço do procedimento de gancho no membro **lpfnHook** .

Depois de processar sua mensagem do [**WM \_ INITDIALOG**](wm-initdialog.md) , o procedimento da caixa de diálogo envia uma mensagem do **WM \_ INITDIALOG** para o procedimento de gancho. O parâmetro *lParam* dessa mensagem é um ponteiro para a estrutura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) usada para inicializar a caixa de diálogo.

A caixa de diálogo envia a mensagem registrada [**COLOROKSTRING**](colorokstring.md) para o procedimento de gancho quando o usuário clica no botão **OK** . O procedimento de gancho pode rejeitar a cor selecionada e forçar a caixa de diálogo a permanecer aberta retornando zero ao receber essa mensagem. O procedimento de gancho pode forçar a caixa de diálogo a selecionar uma cor específica, enviando a mensagem registrada [**SETRGBSTRING**](setrgbstring.md) para a caixa de diálogo. Para usar essas mensagens registradas, você deve passar as constantes **COLOROKSTRING** e **SETRGBSTRING** para a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter um identificador de mensagem. Você pode usar o identificador para detectar e processar mensagens enviadas da caixa de diálogo ou para enviar mensagens para a caixa de diálogo.

## <a name="color-models-used-by-the-color-dialog-box"></a>Modelos de cores usados pela caixa de diálogo cor

A extensão cores personalizadas da caixa de diálogo cor permite que o usuário especifique uma cor usando valores RGB ou HSL. No entanto, a estrutura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) usa apenas valores RGB para relatar as cores criadas ou selecionadas pelo usuário.

-   [Modelo de cor RGB](#rgb-color-model)
-   [Modelo de cor HSL](#hsl-color-model)
-   [Convertendo valores HSL em valores RGB](#converting-hsl-values-to-rgb-values)

### <a name="rgb-color-model"></a>Modelo de cor RGB

O modelo RGB é usado para designar cores para monitores e outros dispositivos que emitem Light. Valores de vermelho, verde e azul válidos variam de 0 a 255, com 0 indicando a intensidade mínima e 255 indicando a intensidade máxima. A ilustração a seguir mostra como as cores primárias vermelho, verde e azul podem ser combinadas para produzir quatro cores adicionais. (Para dispositivos de vídeo, os resultados em preto de cor quando os valores vermelho, verde e azul são definidos como 0. Em tecnologia de vídeo, preto é a ausência de todas as cores.)

![sobrepondo círculos vermelho, verde e azul](images/rgbcolormodel.png)

A tabela a seguir lista oito cores do modelo RGB e seus valores RGB associados.



| Cor   | Valores RGB    |
|---------|---------------|
| Vermelho     | 255, 0, 0     |
| Verde   | 0, 255, 0     |
| Azul    | 0, 0, 255     |
| Cores    | 0, 255, 255   |
| Magenta | 255, 0, 255   |
| Amarelo  | 255, 255, 0   |
| Branca   | 255, 255, 255 |
| Preto   | 0, 0, 0       |



 

O sistema armazena cores internas como valores RGB de 32 bits que têm o seguinte formato hexadecimal: 0x00bbggrr.

O byte de ordem inferior contém um valor para a intensidade relativa de vermelho; o segundo byte contém um valor para verde; e o terceiro byte contém um valor para Blue. O byte de ordem superior deve ser zero.

Você pode usar a macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) para obter um valor RGB com base em intensidades especificadas para os componentes vermelho, verde e azul. Use as macros [**GetRValue**](/windows/desktop/api/wingdi/nf-wingdi-getrvalue), [**GetBValue**](/windows/desktop/api/wingdi/nf-wingdi-getbvalue)e [**GetGValue**](/windows/desktop/api/wingdi/nf-wingdi-getgvalue) para extrair cores individuais de um valor de cor RGB.

### <a name="hsl-color-model"></a>Modelo de cor HSL

A caixa de diálogo cor fornece controles para especificar valores HSL. A ilustração a seguir mostra o controle de espectro de cores e o controle de deslize de luminosidade que aparecem na caixa de diálogo cor. A ilustração também mostra os intervalos de valores que o usuário pode especificar com esses controles.

![espectro de cores e escala de luminosidade](images/colordialogranges.png)

Na caixa de diálogo cor, os valores de saturação e luminosidade devem estar no intervalo de 0 a 240, e o valor de matiz deve estar no intervalo de 0 a 239.

### <a name="converting-hsl-values-to-rgb-values"></a>Convertendo valores HSL em valores RGB

O procedimento da caixa de diálogo fornecido no Comdlg32.dll da caixa de diálogo cor contém o código que converte os valores HSL nos valores RGB correspondentes. A tabela a seguir lista oito cores do modelo RGB e seus valores HSL e RGB associados.



| Cor   | Valores HSL      | Valores RGB      |
|---------|-----------------|-----------------|
| Vermelho     | (0, 240, 120)   | (255, 0, 0)     |
| Amarelo  | (40, 240, 120)  | (255, 255, 0)   |
| Verde   | (80, 240, 120)  | (0, 255, 0)     |
| Cores    | (120, 240, 120) | (0, 255, 255)   |
| Azul    | (160, 240, 120) | (0, 0, 255)     |
| Magenta | (200, 240, 120) | (255, 0, 255)   |
| Branca   | (0, 0, 240)     | (255, 255, 255) |
| Preto   | (0, 0, 0)       | (0, 0, 0)       |



 

 

 
