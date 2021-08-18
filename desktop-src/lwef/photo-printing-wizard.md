---
title: Assistente de impressão de fotos
description: O assistente de impressão de fotos ajuda os usuários a imprimir fotos fornecendo uma interface de assistente fácil de usar.
ms.assetid: 9cc2c7d4-a2aa-4abc-9c63-b091e044804f
keywords:
- Assistente de impressão de fotos
- IDropTarget, assistente de impressão de fotos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38199f7977e428f41cbc0560e0eab9ad2e106709579255ec8c3a1e74d7f7a402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475435"
---
# <a name="photo-printing-wizard"></a>Assistente de impressão de fotos

O assistente de impressão de fotos ajuda os usuários a imprimir fotos fornecendo uma interface de assistente fácil de usar. O assistente permite que o usuário especifique tamanhos de impressão fotográficas e outras opções de impressão e, em seguida, envia as fotos para a impressora. O assistente foi projetado para que possa ser invocado programaticamente por qualquer aplicativo que queira oferecer aos usuários a capacidade de imprimir fotos e especificar o dimensionamento e outras opções de impressão. o assistente de impressão de fotos está disponível no Windows XP e Windows Vista.

-   [Recursos fornecidos pelo assistente de impressão de fotos](#features-provided-by-the-photo-print-wizard)
-   [Formatos de arquivo de fotos com suporte](#supported-photo-file-formats)
-   [Iniciando o assistente de impressão de fotos programaticamente](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a>Recursos fornecidos pelo assistente de impressão de fotos

O assistente de impressão de fotos oferece várias opções que podem não estar disponíveis em caixas de diálogo de impressora comuns, como modelos de vários layouts com dimensões precisas. Os modelos de layout permitem que os usuários façam o uso mais eficiente do espaço disponível no papel de impressão fotográfica. Outras opções que podem ser especificadas ou acessadas por meio do assistente de impressão de fotos incluem:

-   Selecionar uma impressora em uma lista de impressoras disponíveis ou destinos de impressão virtual (por exemplo, Microsoft XPS Document Writer). no Windows Vista, as seguintes opções podem estar disponíveis, dependendo dos recursos da impressora ou destino de impressão virtual:
    -   Tamanho do papel. Por exemplo, "letra", "legal", "A3".
    -   Qualidade de impressão, em termos de resoluções de pontos por polegada (DPI) com suporte.
    -   Tipo de papel. Por exemplo, "Plain" ou "glossy".
-   Iniciando as propriedades e preferências de impressão para uma impressora específica.
-   definir as **cópias de cada imagem** (no Windows Vista) ou o **número de vezes para usar cada imagem** (em Windows XP) valores da caixa de rotação.
-   Especificando um modelo de layout de impressão. Por exemplo, **fotos de página inteira** ou **impressões de carteira**.
-   selecionando a opção **ajustar imagem a quadro** (disponível somente no Windows Vista).
-   Visualizando a foto impressa com as opções especificadas no momento.
-   acessando opções avançadas de impressão, como **nitidez para impressão** e **gerenciamento de cores** (disponível somente no Windows Vista).

Qualquer aplicativo pode se beneficiar dos recursos e da funcionalidade de impressão de fotos oferecida pelo assistente de impressão de fotos. Um aplicativo pode passar os arquivos a serem impressos. Em seguida, o assistente de impressão de fotos cuida da preparação do arquivo para impressão com base nas opções especificadas pelo usuário e envia os arquivos preparados para a impressora.

a figura a seguir mostra a interface do assistente de impressão de fotos no Windows Vista

![o assistente de impressão de fotos no Windows Vista](images/ppw-vista.png)

a figura a seguir mostra a interface do assistente de impressão de fotos no Windows XP

![o assistente de impressão de fotos no Windows XP](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a>Formatos de arquivo de fotos com suporte

no Windows XP, o assistente de impressão de fotos dá suporte a todos os formatos de arquivo gráficos com suporte Windows GDI+. Atualmente, esses formatos de arquivo incluem:

-   BMP (Bitmap)
-   GIF
-   JPEG
-   Exchangeable Image File (EXIF)
-   PNG
-   TIFF

para obter mais informações sobre formatos de arquivos gráficos com suporte pelo GDI+, consulte [tipos de bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md).

no Windows Vista, o assistente de impressão de fotos dá suporte a qualquer formato de arquivo de imagem para o qual um codec de Windows Imaging Component (WIC) está instalado. O WIC fornece vários codecs padrão, incluindo:

-   BMP (Bitmap)
-   GIF
-   Formato de ícone (ICO)
-   JPEG
-   PNG
-   TIFF
-   Windows Formato de foto de mídia

para obter mais informações sobre os codecs wic e wic, consulte [Windows componente de geração de imagens](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)

## <a name="programmatically-launching-the-photo-print-wizard"></a>Iniciando o assistente de impressão de fotos programaticamente

Para invocar o assistente de impressão de fotos, chame a interface [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) com o seguinte CLSID (identificador de classe):


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



Os arquivos a serem processados pelo assistente de impressão de fotos são especificados em um objeto [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .

O exemplo de código a seguir demonstra como invocar o assistente de impressão de fotos.


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
            
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PrintPhotosDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



 

 