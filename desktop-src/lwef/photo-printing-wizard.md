---
title: Assistente de impressão de fotos
description: O assistente de impressão de fotos ajuda os usuários a imprimir fotos fornecendo uma interface de assistente fácil de usar.
ms.assetid: 9cc2c7d4-a2aa-4abc-9c63-b091e044804f
keywords:
- Assistente de impressão de fotos
- IDropTarget, assistente de impressão de fotos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708f051f658739cebd08e4f8643e5dd7fc0c6f7f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365990"
---
# <a name="photo-printing-wizard"></a><span data-ttu-id="9e548-105">Assistente de impressão de fotos</span><span class="sxs-lookup"><span data-stu-id="9e548-105">Photo Printing Wizard</span></span>

<span data-ttu-id="9e548-106">O assistente de impressão de fotos ajuda os usuários a imprimir fotos fornecendo uma interface de assistente fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="9e548-106">The Photo Printing Wizard helps users print photos by providing an easy-to-use wizard interface.</span></span> <span data-ttu-id="9e548-107">O assistente permite que o usuário especifique tamanhos de impressão fotográficas e outras opções de impressão e, em seguida, envia as fotos para a impressora.</span><span class="sxs-lookup"><span data-stu-id="9e548-107">The wizard enables the user to specify photo print sizes and other print options, and then sends the photos to the printer.</span></span> <span data-ttu-id="9e548-108">O assistente foi projetado para que possa ser invocado programaticamente por qualquer aplicativo que queira oferecer aos usuários a capacidade de imprimir fotos e especificar o dimensionamento e outras opções de impressão.</span><span class="sxs-lookup"><span data-stu-id="9e548-108">The wizard is designed so that it can be invoked programmatically by any application that wants to offer users the ability to print photos and specify sizing and other print options.</span></span> <span data-ttu-id="9e548-109">O assistente de impressão de fotos está disponível no Windows XP e no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9e548-109">The Photo Printing Wizard is available on Windows XP and Windows Vista.</span></span>

-   [<span data-ttu-id="9e548-110">Recursos fornecidos pelo assistente de impressão de fotos</span><span class="sxs-lookup"><span data-stu-id="9e548-110">Features Provided by the Photo Print Wizard</span></span>](#features-provided-by-the-photo-print-wizard)
-   [<span data-ttu-id="9e548-111">Formatos de arquivo de fotos com suporte</span><span class="sxs-lookup"><span data-stu-id="9e548-111">Supported Photo File Formats</span></span>](#supported-photo-file-formats)
-   [<span data-ttu-id="9e548-112">Iniciando o assistente de impressão de fotos programaticamente</span><span class="sxs-lookup"><span data-stu-id="9e548-112">Programmatically Launching the Photo Print Wizard</span></span>](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a><span data-ttu-id="9e548-113">Recursos fornecidos pelo assistente de impressão de fotos</span><span class="sxs-lookup"><span data-stu-id="9e548-113">Features Provided by the Photo Print Wizard</span></span>

<span data-ttu-id="9e548-114">O assistente de impressão de fotos oferece várias opções que podem não estar disponíveis em caixas de diálogo de impressora comuns, como modelos de vários layouts com dimensões precisas.</span><span class="sxs-lookup"><span data-stu-id="9e548-114">The Photo Printing Wizard offers several options that may not be available on common printer dialogs, such as multi-layout templates with accurate dimensions.</span></span> <span data-ttu-id="9e548-115">Os modelos de layout permitem que os usuários façam o uso mais eficiente do espaço disponível no papel de impressão fotográfica.</span><span class="sxs-lookup"><span data-stu-id="9e548-115">The layout templates enable users to make the most efficient use of the space available on photographic printing paper.</span></span> <span data-ttu-id="9e548-116">Outras opções que podem ser especificadas ou acessadas por meio do assistente de impressão de fotos incluem:</span><span class="sxs-lookup"><span data-stu-id="9e548-116">Other options that can be specified or accessed through the Photo Print Wizard include:</span></span>

-   <span data-ttu-id="9e548-117">Selecionar uma impressora em uma lista de impressoras disponíveis ou destinos de impressão virtual (por exemplo, Microsoft XPS Document Writer).</span><span class="sxs-lookup"><span data-stu-id="9e548-117">Selecting a printer from a list of available printers or virtual printing destinations (for example, Microsoft XPS Document Writer).</span></span> <span data-ttu-id="9e548-118">No Windows Vista, as seguintes opções podem estar disponíveis, dependendo dos recursos da impressora ou destino de impressão virtual:</span><span class="sxs-lookup"><span data-stu-id="9e548-118">On Windows Vista, the following options may be available, depending on the capabilities of the printer or virtual printing destination:</span></span>
    -   <span data-ttu-id="9e548-119">Tamanho do papel.</span><span class="sxs-lookup"><span data-stu-id="9e548-119">Paper size.</span></span> <span data-ttu-id="9e548-120">Por exemplo, "letra", "legal", "A3".</span><span class="sxs-lookup"><span data-stu-id="9e548-120">For example, "Letter", "Legal", "A3".</span></span>
    -   <span data-ttu-id="9e548-121">Qualidade de impressão, em termos de resoluções de pontos por polegada (DPI) com suporte.</span><span class="sxs-lookup"><span data-stu-id="9e548-121">Print quality, in terms of supported dots per inch (dpi) resolutions.</span></span>
    -   <span data-ttu-id="9e548-122">Tipo de papel.</span><span class="sxs-lookup"><span data-stu-id="9e548-122">Paper type.</span></span> <span data-ttu-id="9e548-123">Por exemplo, "Plain" ou "glossy".</span><span class="sxs-lookup"><span data-stu-id="9e548-123">For example, "Plain" or "Glossy".</span></span>
-   <span data-ttu-id="9e548-124">Iniciando as propriedades e preferências de impressão para uma impressora específica.</span><span class="sxs-lookup"><span data-stu-id="9e548-124">Launching the printing preferences and properties for a particular printer.</span></span>
-   <span data-ttu-id="9e548-125">Definir as **cópias de cada imagem** (no Windows Vista) ou o **número de vezes para usar cada imagem** (no Windows XP) valores da caixa de rotação.</span><span class="sxs-lookup"><span data-stu-id="9e548-125">Setting the **Copies of each picture** (on Windows Vista) or **Number of times to use each picture** (on Windows XP) spin box values.</span></span>
-   <span data-ttu-id="9e548-126">Especificando um modelo de layout de impressão.</span><span class="sxs-lookup"><span data-stu-id="9e548-126">Specifying a print layout template.</span></span> <span data-ttu-id="9e548-127">Por exemplo, **fotos de página inteira** ou **impressões de carteira**.</span><span class="sxs-lookup"><span data-stu-id="9e548-127">For example, **Full page photo** or **Wallet prints**.</span></span>
-   <span data-ttu-id="9e548-128">Selecionando a opção **ajustar imagem a quadro** (disponível somente no Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="9e548-128">Selecting the **Fit picture to frame** option (available on Windows Vista only).</span></span>
-   <span data-ttu-id="9e548-129">Visualizando a foto impressa com as opções especificadas no momento.</span><span class="sxs-lookup"><span data-stu-id="9e548-129">Previewing the printed photo with the currently specified options.</span></span>
-   <span data-ttu-id="9e548-130">Acessando opções avançadas de impressão, como **nitidez para impressão** e **Gerenciamento de cores** (disponível somente no Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="9e548-130">Accesssing advanced print options, such as **Sharpen for printing** and **Color management** (available on Windows Vista only).</span></span>

<span data-ttu-id="9e548-131">Qualquer aplicativo pode se beneficiar dos recursos e da funcionalidade de impressão de fotos oferecida pelo assistente de impressão de fotos.</span><span class="sxs-lookup"><span data-stu-id="9e548-131">Any application can benefit from the features and photo printing capability offered by the Photo Printing Wizard.</span></span> <span data-ttu-id="9e548-132">Um aplicativo pode passar os arquivos a serem impressos.</span><span class="sxs-lookup"><span data-stu-id="9e548-132">An application can pass in the files to be printed.</span></span> <span data-ttu-id="9e548-133">Em seguida, o assistente de impressão de fotos cuida da preparação do arquivo para impressão com base nas opções especificadas pelo usuário e envia os arquivos preparados para a impressora.</span><span class="sxs-lookup"><span data-stu-id="9e548-133">The Photo Printing Wizard then takes care of preparing the file for printing based on the options specified by the user and sends the prepared files to the printer.</span></span>

<span data-ttu-id="9e548-134">A figura a seguir mostra a interface do assistente de impressão de fotos no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e548-134">The following figure shows the Photo Printing Wizard interface on Windows Vista</span></span>

![o assistente de impressão de fotos no Windows Vista](images/ppw-vista.png)

<span data-ttu-id="9e548-136">A figura a seguir mostra a interface do assistente de impressão de fotos no Windows XP</span><span class="sxs-lookup"><span data-stu-id="9e548-136">The following figure shows the Photo Printing Wizard interface on Windows XP</span></span>

![o assistente de impressão de fotos no Windows XP](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a><span data-ttu-id="9e548-138">Formatos de arquivo de fotos com suporte</span><span class="sxs-lookup"><span data-stu-id="9e548-138">Supported Photo File Formats</span></span>

<span data-ttu-id="9e548-139">No Windows XP, o assistente de impressão de fotos dá suporte a todos os formatos de arquivo gráficos com suporte no Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="9e548-139">On Windows XP, the Photo Print Wizard supports all graphics file formats that are supported by Windows GDI+.</span></span> <span data-ttu-id="9e548-140">Atualmente, esses formatos de arquivo incluem:</span><span class="sxs-lookup"><span data-stu-id="9e548-140">Currently, these file formats include:</span></span>

-   <span data-ttu-id="9e548-141">BMP (Bitmap)</span><span class="sxs-lookup"><span data-stu-id="9e548-141">Bitmap (BMP)</span></span>
-   <span data-ttu-id="9e548-142">GIF</span><span class="sxs-lookup"><span data-stu-id="9e548-142">Graphics Interchange Format (GIF)</span></span>
-   <span data-ttu-id="9e548-143">JPEG</span><span class="sxs-lookup"><span data-stu-id="9e548-143">Joint Photographic Experts Group (JPEG)</span></span>
-   <span data-ttu-id="9e548-144">Exchangeable Image File (EXIF)</span><span class="sxs-lookup"><span data-stu-id="9e548-144">Exchangeable Image File (EXIF)</span></span>
-   <span data-ttu-id="9e548-145">PNG</span><span class="sxs-lookup"><span data-stu-id="9e548-145">Portable Network Graphics (PNG)</span></span>
-   <span data-ttu-id="9e548-146">TIFF</span><span class="sxs-lookup"><span data-stu-id="9e548-146">Tagged Image File Format (TIFF)</span></span>

<span data-ttu-id="9e548-147">Para obter mais informações sobre formatos de arquivos gráficos com suporte no GDI+, consulte [tipos de bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md).</span><span class="sxs-lookup"><span data-stu-id="9e548-147">For more information about graphics file formats supported by GDI+, see [Types of Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md).</span></span>

<span data-ttu-id="9e548-148">No Windows Vista, o assistente de impressão de fotos dá suporte a qualquer formato de arquivo de imagem para o qual um codec do Windows Imaging Component (WIC) esteja instalado.</span><span class="sxs-lookup"><span data-stu-id="9e548-148">On Windows Vista, the Photo Print Wizard supports any image file format for which a Windows Imaging Component (WIC) codec is installed.</span></span> <span data-ttu-id="9e548-149">O WIC fornece vários codecs padrão, incluindo:</span><span class="sxs-lookup"><span data-stu-id="9e548-149">WIC provides several standard codecs, including:</span></span>

-   <span data-ttu-id="9e548-150">BMP (Bitmap)</span><span class="sxs-lookup"><span data-stu-id="9e548-150">Bitmap (BMP)</span></span>
-   <span data-ttu-id="9e548-151">GIF</span><span class="sxs-lookup"><span data-stu-id="9e548-151">GIF</span></span>
-   <span data-ttu-id="9e548-152">Formato de ícone (ICO)</span><span class="sxs-lookup"><span data-stu-id="9e548-152">Icon Format (ICO)</span></span>
-   <span data-ttu-id="9e548-153">JPEG</span><span class="sxs-lookup"><span data-stu-id="9e548-153">JPEG</span></span>
-   <span data-ttu-id="9e548-154">PNG</span><span class="sxs-lookup"><span data-stu-id="9e548-154">PNG</span></span>
-   <span data-ttu-id="9e548-155">TIFF</span><span class="sxs-lookup"><span data-stu-id="9e548-155">TIFF</span></span>
-   <span data-ttu-id="9e548-156">Formato de foto do Windows Media</span><span class="sxs-lookup"><span data-stu-id="9e548-156">Windows Media Photo format</span></span>

<span data-ttu-id="9e548-157">Para obter mais informações sobre os codecs WIC e WIC, consulte [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="9e548-157">For more information about WIC and WIC codecs, see [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)</span></span>

## <a name="programmatically-launching-the-photo-print-wizard"></a><span data-ttu-id="9e548-158">Iniciando o assistente de impressão de fotos programaticamente</span><span class="sxs-lookup"><span data-stu-id="9e548-158">Programmatically Launching the Photo Print Wizard</span></span>

<span data-ttu-id="9e548-159">Para invocar o assistente de impressão de fotos, chame a interface [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) com o seguinte CLSID (identificador de classe):</span><span class="sxs-lookup"><span data-stu-id="9e548-159">To invoke the Photo Printing Wizard, call the [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface with the following class identifier (CLSID):</span></span>


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



<span data-ttu-id="9e548-160">Os arquivos a serem processados pelo assistente de impressão de fotos são especificados em um objeto [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="9e548-160">The files to be processed by the Photo Printing Wizard are specified in an [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) object.</span></span>

<span data-ttu-id="9e548-161">O exemplo de código a seguir demonstra como invocar o assistente de impressão de fotos.</span><span class="sxs-lookup"><span data-stu-id="9e548-161">The following code example demonstrates how to invoke the Photo Printing Wizard.</span></span>


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



 

 