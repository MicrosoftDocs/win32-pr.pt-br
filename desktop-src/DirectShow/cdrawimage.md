---
description: A classe CDrawImage é uma classe auxiliar que gerencia o desenho de um filtro de processador de vídeo.
ms.assetid: 7a6b3726-dbf5-4b60-8cf1-42034a321293
title: Classe CDrawImage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 951744cded927707ac0b39e562b4207acbecdd92420c91a2b130f0b493444b01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999546"
---
# <a name="cdrawimage-class"></a>Classe CDrawImage

A `CDrawImage` classe é uma classe auxiliar que gerencia o desenho de um filtro de processador de vídeo. Todas as operações de desenho são executadas usando GDI. Essa classe não fornece suporte para renderização com o DirectDraw. A `CDrawImage` classe requer que o filtro proprietário também use a classe [**CBaseWindow**](cbasewindow.md) , que gerencia a janela de vídeo. O `CDrawImage` construtor usa um ponteiro para o objeto **CBaseWindow** .

O diagrama a seguir mostra a maneira preferida de usar essa classe em um filtro de processador de vídeo personalizado.

![processador de vídeo personalizado usando cdrawimage](images/videorenderer.png)

Para usar essa classe, faça o seguinte:

-   Quando os PINs se conectarem, chame os métodos [**CDrawImage:: NotifyMediaType**](cdrawimage-notifymediatype.md) e [**CDrawImage:: NotifyAllocator**](cdrawimage-notifyallocator.md) .
-   Sempre que o tipo de mídia for alterado, chame **NotifyMediaType** novamente.
-   Antes que qualquer renderização ocorra, chame [**CDrawImage:: SetDrawContext**](cdrawimage-setdrawcontext.md).
-   Chame [**CDrawImage:: SetSourceRect**](cdrawimage-setsourcerect.md) se o retângulo de origem for alterado e [**CDrawImage:: SetTargetRect**](cdrawimage-settargetrect.md) se o retângulo de destino for alterado.
-   Gerencie a paleta para imagens palettized, conforme descrito na seção sobre paletas a seguir.

## <a name="allocators"></a>Alocadores

O filtro mostrado no diagrama anterior usa uma classe de alocador personalizada, [**CImageAllocator**](cimageallocator.md). Esse alocador cria DIBs na memória compartilhada, usando a função **CreateDIBSection** do GDI. Os exemplos criados pelo alocador são objetos [**CImageSample**](cimagesample.md) .

Se o filtro possuir o alocador para a conexão, os exemplos de mídia serão garantidos como objetos [**CImageSample**](cimagesample.md) . Nesse caso, o objeto **CDrawImage** pode otimizar o desenho usando **BitBlt** ou StretchBlt. Caso contrário, ele deve usar as funções **SetDIBitsToDevice** ou **StretchDIBits** mais lentas. A opção mais rápida é implementada pelo método [**CDrawImage:: FastRender**](cdrawimage-fastrender.md) , a opção mais lenta pelo método [**CDrawImage:: SlowRender**](cdrawimage-slowrender.md) . (Apesar do nome, você provavelmente não verá um grande impacto no desempenho em **SlowRender**, especialmente em hardware mais recente.)

## <a name="palettes"></a>Paletas

Se o método [**FastRender**](cdrawimage-fastrender.md) for usado para desenhar e a imagem for palettized, o filtro precisará gerenciar a paleta da seguinte maneira:

-   A classe [**CImageSample**](cimagesample.md) contém um número de versão da paleta, armazenado na estrutura [**DIBDATA**](dibdata.md) . O valor é inicializado quando o alocador cria o exemplo.
-   A classe **CDrawImage** também contém um número de versão da paleta, que é inicializado na criação.
-   Sempre que o tipo de mídia for alterado para um novo formato palettized, chame [**CDrawImage:: IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md). Esse método incrementa o número de versão da paleta do objeto **CDrawImage** . Se o filtro usar a classe [**CImagePalette**](cimagepalette.md) para gerenciar as informações da paleta, você poderá simplesmente chamar [**CImagePalette::P reparepalette**](cimagepalette-preparepalette.md) sempre que o tipo de mídia for alterado. O método **PreparePalette** incrementa a versão da paleta somente quando necessário.
-   O método [**FastRender**](cdrawimage-fastrender.md) compara a versão da paleta **CDrawImage** com a versão da paleta da amostra. Se o número de versão do exemplo estiver atrasado atrás do número de versão **CDrawImage** , o método **FastRender** chamará [**CDrawImage:: UpdateColourTable**](cdrawimage-updatecolourtable.md). O método **UpdateColourTable** define a tabela de cores no contexto do dispositivo, usando a função **SetDIBColorTable** do GDI. Além disso, a versão da paleta no exemplo é atualizada para o número de versão atual.
-   Se o PIN se reconectar, o filtro deverá chamar [**CDrawImage:: ResetPaletteVersion**](cdrawimage-resetpaletteversion.md) para redefinir a versão da paleta. Na reconexão do PIN, o alocador aloca novamente todas as amostras.



| Variáveis de membro protegido                                            | Descrição                                                                                                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**\_bStretch m**](cdrawimage-m-bstretch.md)                          | Indica se a imagem de vídeo deve ser ampliada para se ajustar à janela de destino.                                              |
| [**\_bUsingImageAllocator m**](cdrawimage-m-busingimageallocator.md)  | Indica se o alocador para a conexão de PIN é um objeto **CImageAllocator** .                                         |
| [**exemplo de end \_**](cdrawimage-m-endsample.md)                        | Especifica a hora de parada do exemplo mais recente.                                                                              |
| [**\_HDC m**](cdrawimage-m-hdc.md)                                    | Identificador para o contexto do dispositivo da janela proprietária.                                                                              |
| [**\_MemoryDC m**](cdrawimage-m-memorydc.md)                          | Identificador para o contexto de dispositivo de memória da janela proprietária.                                                                       |
| [**\_PaletteVersion m**](cdrawimage-m-paletteversion.md)              | Usado para controlar quando a paleta é alterada.                                                                                         |
| [**\_pBaseWindow m**](cdrawimage-m-pbasewindow.md)                    | Ponteiro para o objeto **CBaseWindow** proprietário.                                                                                   |
| [**\_pMediaType m**](cdrawimage-m-pmediatype.md)                      | Ponteiro para o tipo de mídia atual.                                                                                              |
| [**\_SourceRect m**](cdrawimage-m-sourcerect.md)                      | Especifica o retângulo de origem para desenho.                                                                                     |
| [**\_StartSample m**](cdrawimage-m-startsample.md)                    | Especifica a hora de início do exemplo mais recente.                                                                             |
| [**\_TargetRect m**](cdrawimage-m-targetrect.md)                      | Especifica o retângulo de destino para desenho.                                                                                     |
| Métodos Protegidos                                                     | Descrição                                                                                                                     |
| [**DisplaySampleTimes**](cdrawimage-displaysampletimes.md)           | Desenha os carimbos de data/hora de um exemplo de mídia sobre a imagem de vídeo.                                                              |
| [**FastRender**](cdrawimage-fastrender.md)                           | Desenha a imagem de vídeo usando as funções **BitBlt** ou **StretchBlt** .                                                         |
| [**Setstretchmode**](cdrawimage-setstretchmode.md)                   | Calcula se a imagem de vídeo deve ser ampliada.                                                                           |
| [**SlowRender**](cdrawimage-slowrender.md)                           | Desenha a imagem de vídeo usando as funções **SetDIBitsToDevice** ou **StretchDIBits** .                                           |
| [**UpdateColourTable**](cdrawimage-updatecolourtable.md)             | Atualiza a tabela de cores com uma nova paleta.                                                                                     |
| Métodos públicos                                                        | Descrição                                                                                                                     |
| [**CDrawImage**](cdrawimage-cdrawimage.md)                           | Método de construtor.                                                                                                             |
| [**DrawImage**](cdrawimage-drawimage.md)                             | Desenha um quadro de vídeo na janela de vídeo.                                                                                        |
| [**DrawVideoImageHere**](cdrawimage-drawvideoimagehere.md)           | Desenha uma imagem de um exemplo de mídia para um contexto de dispositivo especificado.                                                               |
| [**GetPaletteVersion**](cdrawimage-getpaletteversion.md)             | Recupera a versão da paleta.                                                                                                  |
| [**GetSourceRect**](cdrawimage-getsourcerect.md)                     | Recupera o retângulo de origem atual.                                                                                         |
| [**GetTargetRect**](cdrawimage-gettargetrect.md)                     | Recupera o retângulo de destino atual.                                                                                    |
| [**IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) | Incrementa a versão da paleta.                                                                                                 |
| [**NotifyAllocator**](cdrawimage-notifyallocator.md)                 | Informa ao `CDrawImage` objeto se o alocador da conexão é um objeto **CImageAllocator** .                       |
| [**NotifyEndDraw**](cdrawimage-notifyenddraw.md)                     | Sem suporte.                                                                                                                  |
| [**NotifyMediaType**](cdrawimage-notifymediatype.md)                 | Notifica o objeto do tipo de mídia atual.                                                                                  |
| [**NotifyStartDraw**](cdrawimage-notifystartdraw.md)                 | Sem suporte.                                                                                                                  |
| [**ResetPaletteVersion**](cdrawimage-resetpaletteversion.md)         | Redefine a versão da paleta.                                                                                                     |
| [**ScaleSourceRect**](cdrawimage-scalesourcerect.md)                 | Dimensiona um retângulo de origem especificado, se houver uma diferença entre o tamanho do vídeo nativo e o formato de tipo de mídia. Virtual. |
| [**SetDrawContext**](cdrawimage-setdrawcontext.md)                   | Define os contextos de dispositivo usados para desenho.                                                                                      |
| [**SetSourceRect**](cdrawimage-setsourcerect.md)                     | Define o retângulo de origem.                                                                                                      |
| [**SetTargetRect**](cdrawimage-settargetrect.md)                     | Define o retângulo de destino.                                                                                                      |
| [**UsingImageAllocator**](cdrawimage-usingimageallocator.md)         | Indica se o alocador atual é um [**objeto CImageAllocator.**](cimageallocator.md)                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




