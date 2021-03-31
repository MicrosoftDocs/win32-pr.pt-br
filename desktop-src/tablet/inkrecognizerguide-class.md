---
description: Representa a área que o reconhecedor usa no qual a tinta pode ser desenhada. A área é conhecida como o guia de reconhecimento.
ms.assetid: c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7
title: Classe InkRecognizerGuide (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerGuide
- InkRecognizerGuide.IInkRecognizerGuide
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 55729513f748afc87f184b73eaba976184307bc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172066"
---
# <a name="inkrecognizerguide-class"></a>Classe InkRecognizerGuide

Representa a área que o reconhecedor usa no qual a tinta pode ser desenhada. A área é conhecida como o guia de reconhecimento.

**InkRecognizerGuide** tem estes tipos de membros:

-   [Interfaces](#interfaces)
-   [Propriedades](#properties)

### <a name="interfaces"></a>Interfaces

A classe **InkRecognizerGuide** define essas interfaces.



| Interface               | Descrição                                                                  |
|:------------------------|:-----------------------------------------------------------------------------|
| **IInkRecognizerGuide** | Esse objeto implementa a interface com do **IInkRecognizerGuide** .<br/> |



 

### <a name="properties"></a>Propriedades

A classe **InkRecognizerGuide** tem essas propriedades.



| Propriedade                                                       | Tipo de acesso           | Descrição                                                                                                                    |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Colunas**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns)<br/>       | Leitura/gravação<br/> | Obtém ou define o número de colunas na caixa guia.<br/>                                                                |
| [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)<br/>     | Leitura/gravação<br/> | Obtém ou define a caixa que é desenhada fisicamente na tela do Tablet e em que ocorre a gravação.<br/>              |
| [**GuideData**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_guidedata)<br/>   | Leitura/gravação<br/> | Obtém ou define os dados do guia para desenvolvedores do C++.<br/>                                                                         |
| [**Tabs no meio**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_midline)<br/>       | Leitura/gravação<br/> | Obtém ou define a altura de Tabs no meio. A altura de Tabs no meio é a distância da linha de base para o Tabs no meio da caixa de desenho.<br/> |
| [**As**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows)<br/>             | Leitura/gravação<br/> | Obtém ou define o número de linhas na caixa guia.<br/>                                                                   |
| [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)<br/> | Leitura/gravação<br/> | Obtém ou define a área de escrita invisível da caixa guia na qual a gravação pode realmente ocorrer.<br/>                  |



 

## <a name="remarks"></a>Comentários

Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .

Por padrão, não há nenhum guia do reconhecedor. Um guia padrão tem todos os valores de propriedade definidos como 0. Você deve usar as propriedades desse objeto para definir o guia.

Se o aplicativo tiver diretrizes desenhadas na tela em que o usuário deve gravar, o aplicativo deverá definir os valores das propriedades do guia do reconhecedor para informar o reconhecedor. Essas propriedades são apenas para uso do reconhecedor. Configurá-las não faz, por si só, desenhar pistas visuais na exibição. O aplicativo ou o controle desenha as pistas visuais.

O guia do reconhecedor pode consistir em linhas e colunas, e elas dão ao reconhecedor um contexto melhor para executar o reconhecimento. Letras como "t" e "I" são mais facilmente reconhecidas quando um guia é usado para dar contexto à tinta. Por exemplo, você pode desenhar linhas horizontais em uma tela, que mostram onde deve ocorrer gravação (esse tipo de guia consistiria apenas em linhas e nenhuma coluna). Ao escrever nas linhas, em vez de algum espaço arbitrário, a precisão de reconhecimento melhora.

O guia especifica os limites da tinta nas coordenadas de espaço de tinta.

A propriedade [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) pode definir uma caixa que é do mesmo tamanho que ou menor que a caixa definida pela propriedade [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) .

A figura a seguir mostra os elementos de um guia do reconhecedor com duas linhas e nenhuma coluna.

![ilustração mostrando elementos do guia do reconhecedor](images/927cc2f3-549f-4279-aab9-bd5ade070eaf.jpg)

Além de desenhar linhas na tela que mostram os usuários onde escrever, você pode desenhar células na tela em que os caracteres ou palavras são gravados. Isso é chamado de entrada em caixa e é útil em alguns idiomas asiáticos. Para determinar se o reconhecedor é capaz de entrada em caixa, chame a propriedade [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) do objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) .

A figura a seguir mostra um guia do reconhecedor com quatro colunas.

![ilustração mostrando o guia do reconhecedor com quatro colunas](images/de44c07e-4b55-42d0-8e8b-997e2da79e52.jpg)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**Classe InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> </dl>

 

