---
title: Assistente de Impressão de Fotos
description: O Assistente de Impressão de Fotos ajuda os usuários a imprimir fotos fornecendo uma interface de assistente fácil de usar.
ms.assetid: 9cc2c7d4-a2aa-4abc-9c63-b091e044804f
keywords:
- Assistente de Impressão de Fotos
- IDropTarget, Assistente de Impressão de Fotos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38199f7977e428f41cbc0560e0eab9ad2e106709579255ec8c3a1e74d7f7a402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475435"
---
# <a name="photo-printing-wizard"></a>Assistente de Impressão de Fotos

O Assistente de Impressão de Fotos ajuda os usuários a imprimir fotos fornecendo uma interface de assistente fácil de usar. O assistente permite que o usuário especifique tamanhos de impressão de foto e outras opções de impressão e, em seguida, envia as fotos para a impressora. O assistente foi projetado para que ele possa ser invocado programaticamente por qualquer aplicativo que queira oferecer aos usuários a capacidade de imprimir fotos e especificar oizing e outras opções de impressão. O Assistente de Impressão de Fotos está disponível no Windows XP e Windows Vista.

-   [Recursos fornecidos pelo Assistente para Impressão De Fotos](#features-provided-by-the-photo-print-wizard)
-   [Formatos de arquivo de foto com suporte](#supported-photo-file-formats)
-   [Iniciando programaticamente o Assistente de Impressão De Foto](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a>Recursos fornecidos pelo Assistente para Impressão De Fotos

O Assistente de Impressão de Fotos oferece várias opções que podem não estar disponíveis em caixas de diálogo comuns de impressora, como modelos de vários layouts com dimensões precisas. Os modelos de layout permitem que os usuários façam o uso mais eficiente do espaço disponível em papel de impressão gráfica. Outras opções que podem ser especificadas ou acessadas por meio do Assistente de Impressão De Foto incluem:

-   Selecionar uma impressora em uma lista de impressoras disponíveis ou destinos de impressão virtual (por exemplo, o Microsoft XPS Document Writer). No Windows Vista, as seguintes opções podem estar disponíveis, dependendo dos recursos da impressora ou do destino de impressão virtual:
    -   Tamanho do papel. Por exemplo, "Letra", "Legal", "A3".
    -   Qualidade de impressão, em termos de resoluções dpi (pontos por polegada) com suporte.
    -   Tipo de papel. Por exemplo, "Plain" ou "Glossy".
-   Iniciando as preferências de impressão e as propriedades de uma impressora específica.
-   Definir as **Cópias de cada** imagem (no Windows Vista) ou Número de vezes para usar cada imagem (no Windows XP). 
-   Especificando um modelo de layout de impressão. Por exemplo, **Foto de página inteira ou** Carteira **imprime**.
-   Selecionando **a opção Ajustar imagem ao quadro** (disponível somente Windows Vista).
-   Visualizando a foto impressa com as opções especificadas no momento.
-   Acessando opções de impressão avançadas, como **Desa digitalização** para impressão e Gerenciamento de cores **(disponível** somente Windows Vista).

Qualquer aplicativo pode se beneficiar dos recursos e da funcionalidade de impressão de fotos oferecida pelo Assistente de Impressão De Fotos. Um aplicativo pode passar os arquivos a serem impressos. Em seguida, o Assistente de Impressão de Fotos cuida da preparação do arquivo para impressão com base nas opções especificadas pelo usuário e envia os arquivos preparados para a impressora.

A figura a seguir mostra a interface do Assistente para Impressão de Fotos Windows Vista

![o assistente de impressão de foto no Windows Vista](images/ppw-vista.png)

A figura a seguir mostra a interface do Assistente para Impressão de Fotos Windows XP

![o assistente de impressão de foto no Windows Xp](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a>Formatos de arquivo de foto com suporte

No Windows XP, o Assistente de Impressão De Foto dá suporte a todos os formatos de arquivo gráfico com suporte do Windows GDI+. Atualmente, esses formatos de arquivo incluem:

-   BMP (Bitmap)
-   GIF
-   JPEG
-   Exchangeable Image File (EXIF)
-   PNG
-   TIFF

Para obter mais informações sobre formatos de arquivo gráficos com suporte GDI+, consulte [Tipos de bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md).

No Windows Vista, o Assistente para Impressão de Fotos dá suporte a qualquer formato de arquivo de imagem para o qual um codec do WIC (Componente de Imagem Windows) está instalado. O WIC fornece vários codecs padrão, incluindo:

-   BMP (Bitmap)
-   GIF
-   Formato de ícone (ICO)
-   JPEG
-   PNG
-   TIFF
-   Windows Formato de foto de mídia

Para obter mais informações sobre codecs WIC e WIC, [consulte Windows componente de imagens](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)

## <a name="programmatically-launching-the-photo-print-wizard"></a>Iniciando programaticamente o Assistente de Impressão De Foto

Para invocar o Assistente de Impressão de Fotos, chame a interface [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) com o seguinte identificador de classe (CLSID):


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



Os arquivos a serem processados pelo Assistente de Impressão De Fotos são especificados em um [objeto IDataObject.](/windows/win32/api/objidl/nn-objidl-idataobject)

O exemplo de código a seguir demonstra como invocar o Assistente para Impressão de Fotos.


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



 

 