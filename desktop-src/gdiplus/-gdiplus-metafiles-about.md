---
description: O Windows GDI+ fornece a classe Metafile para que você possa gravar e exibir os metaarquivos.
ms.assetid: a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077
title: Metaarquivos (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae75c2185670563f9a9e624d868da5b0e299cbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296330"
---
# <a name="metafiles-gdi"></a><span data-ttu-id="05f0c-103">Metaarquivos (GDI+)</span><span class="sxs-lookup"><span data-stu-id="05f0c-103">Metafiles (GDI+)</span></span>

<span data-ttu-id="05f0c-104">O Windows GDI+ fornece a classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) para que você possa gravar e exibir os metaarquivos.</span><span class="sxs-lookup"><span data-stu-id="05f0c-104">Windows GDI+ provides the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class so that you can record and display metafiles.</span></span> <span data-ttu-id="05f0c-105">Um metarquivo, também chamado de uma imagem de vetor, é uma imagem que é armazenada como uma sequência de comandos e configurações de desenho.</span><span class="sxs-lookup"><span data-stu-id="05f0c-105">A metafile, also called a vector image, is an image that is stored as a sequence of drawing commands and settings.</span></span> <span data-ttu-id="05f0c-106">Os comandos e as configurações registrados em um objeto de **metarquivo** podem ser armazenados na memória ou salvos em um arquivo ou fluxo.</span><span class="sxs-lookup"><span data-stu-id="05f0c-106">The commands and settings recorded in a **Metafile** object can be stored in memory or saved to a file or stream.</span></span>

<span data-ttu-id="05f0c-107">O GDI+ pode exibir os metaarquivos que foram armazenados nos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="05f0c-107">GDI+ can display metafiles that have been stored in the following formats:</span></span>

-   <span data-ttu-id="05f0c-108">Formato WMF (WMF)</span><span class="sxs-lookup"><span data-stu-id="05f0c-108">Windows Metafile Format (WMF)</span></span>
-   <span data-ttu-id="05f0c-109">EMF (Metarquivo Avançado)</span><span class="sxs-lookup"><span data-stu-id="05f0c-109">Enhanced Metafile (EMF)</span></span>
-   <span data-ttu-id="05f0c-110">EMF+</span><span class="sxs-lookup"><span data-stu-id="05f0c-110">EMF+</span></span>

<span data-ttu-id="05f0c-111">O GDI+ pode registrar os metarquivos nos formatos EMF e EMF +, mas não no formato WMF.</span><span class="sxs-lookup"><span data-stu-id="05f0c-111">GDI+ can record metafiles in the EMF and EMF+ formats, but not in the WMF format.</span></span>

<span data-ttu-id="05f0c-112">EMF + é uma extensão do EMF que permite que os registros de GDI+ sejam armazenados.</span><span class="sxs-lookup"><span data-stu-id="05f0c-112">EMF+ is an extension to EMF that allows GDI+ records to be stored.</span></span> <span data-ttu-id="05f0c-113">Há duas variações no formato EMF+: Apenas EMF+ e EMF+ Duplo.</span><span class="sxs-lookup"><span data-stu-id="05f0c-113">There are two variations on the EMF+ format: EMF+ Only and EMF+ Dual.</span></span> <span data-ttu-id="05f0c-114">Os metaarquivos EMF + somente contêm registros GDI+.</span><span class="sxs-lookup"><span data-stu-id="05f0c-114">EMF+ Only metafiles contain only GDI+ records.</span></span> <span data-ttu-id="05f0c-115">Esses metaarquivos podem ser exibidos por GDI+, mas não pelo Windows Graphics Device Interface (GDI).</span><span class="sxs-lookup"><span data-stu-id="05f0c-115">Such metafiles can be displayed by GDI+ but not by Windows Graphics Device Interface (GDI).</span></span> <span data-ttu-id="05f0c-116">Os metaarquivos EMF e dual contêm registros GDI+ e GDI.</span><span class="sxs-lookup"><span data-stu-id="05f0c-116">EMF+ Dual metafiles contain GDI+ and GDI records.</span></span> <span data-ttu-id="05f0c-117">Cada registro de GDI+ em um metarquivo EMF + duplo é emparelhado com um registro GDI alternativo.</span><span class="sxs-lookup"><span data-stu-id="05f0c-117">Each GDI+ record in an EMF+ Dual metafile is paired with an alternate GDI record.</span></span> <span data-ttu-id="05f0c-118">Esses metaarquivos podem ser exibidos por GDI+ ou por GDI.</span><span class="sxs-lookup"><span data-stu-id="05f0c-118">Such metafiles can be displayed by GDI+ or by GDI.</span></span>

<span data-ttu-id="05f0c-119">O exemplo a seguir registra uma configuração e um comando de desenho em um arquivo de disco.</span><span class="sxs-lookup"><span data-stu-id="05f0c-119">The following example records one setting and one drawing command in a disk file.</span></span> <span data-ttu-id="05f0c-120">Observe que o exemplo cria um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e que o construtor do objeto **Graphics** recebe o endereço de um objeto de [**metarquivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) como um argumento.</span><span class="sxs-lookup"><span data-stu-id="05f0c-120">Note that the example creates a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and that the constructor for the **Graphics** object receives the address of a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object as an argument.</span></span>


```
myMetafile = new Metafile(L"MyDiskFile.emf", hdc);
myGraphics = new Graphics(myMetafile);
   myPen = new Pen(Color(255, 0, 0, 200));
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->DrawLine(myPen, 0, 0, 60, 40);
delete myGraphics;
delete myPen;
delete myMetafile;
```



<span data-ttu-id="05f0c-121">Como mostra o exemplo anterior, a classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) é a chave para gravar instruções e configurações em um objeto de [**metarquivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="05f0c-121">As the preceding example shows, the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is the key to recording instructions and settings in a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="05f0c-122">Qualquer chamada feita a um método de um objeto de **gráfico** pode ser registrada em um objeto de **metarquivo** .</span><span class="sxs-lookup"><span data-stu-id="05f0c-122">Any call made to a method of a **Graphics** object can be recorded in a **Metafile** object.</span></span> <span data-ttu-id="05f0c-123">Da mesma forma, você pode definir qualquer propriedade de um objeto de **gráfico** e registrar essa configuração em um objeto de **metarquivo** .</span><span class="sxs-lookup"><span data-stu-id="05f0c-123">Likewise, you can set any property of a **Graphics** object and record that setting in a **Metafile** object.</span></span> <span data-ttu-id="05f0c-124">A gravação termina quando o objeto de **gráficos** é excluído ou sai do escopo.</span><span class="sxs-lookup"><span data-stu-id="05f0c-124">The recording ends when the **Graphics** object is deleted or goes out of scope.</span></span>

<span data-ttu-id="05f0c-125">O exemplo a seguir exibe o metarquivo criado no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="05f0c-125">The following example displays the metafile created in the preceding example.</span></span> <span data-ttu-id="05f0c-126">O metarquivo é exibido com seu canto superior esquerdo em (100, 100).</span><span class="sxs-lookup"><span data-stu-id="05f0c-126">The metafile is displayed with its upper-left corner at (100, 100).</span></span>


```
Graphics myGraphics(hdc);
Image myImage(L"MyDiskFile.emf");
myGraphics.DrawImage(&myImage, 100, 100);
```



<span data-ttu-id="05f0c-127">O exemplo a seguir registra várias configurações de propriedade (região de recorte, transformação mundial e modo de suavização) em um objeto de [**metarquivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="05f0c-127">The following example records several property settings (clipping region, world transformation, and smoothing mode) in a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="05f0c-128">Em seguida, o código registra várias instruções de desenho.</span><span class="sxs-lookup"><span data-stu-id="05f0c-128">Then the code records several drawing instructions.</span></span> <span data-ttu-id="05f0c-129">As instruções e configurações são salvas em um arquivo de disco.</span><span class="sxs-lookup"><span data-stu-id="05f0c-129">The instructions and settings are saved in a disk file.</span></span>


```
myMetafile = new Metafile(L"MyDiskFile2.emf", hdc); 
myGraphics = new Graphics(myMetafile);
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->RotateTransform(30);

   // Create an elliptical clipping region.
   GraphicsPath myPath;
   myPath.AddEllipse(0, 0, 200, 100);
   Region myRegion(&myPath);
   myGraphics->SetClip(&myRegion);

   Pen myPen(Color(255, 0, 0, 255));
   myGraphics->DrawPath(&myPen, &myPath);

   for(INT j = 0; j <= 300; j += 10)
   {
      myGraphics->DrawLine(&myPen, 0, 0, 300 - j, j);
   }
delete myGraphics;
delete myMetafile;
```



<span data-ttu-id="05f0c-130">O exemplo a seguir exibe a imagem de metarquivo criada no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="05f0c-130">The following example displays the metafile image created in the preceding example.</span></span>


```
myGraphics = new Graphics(hdc);
myMetafile = new Metafile(L"MyDiskFile.emf");
myGraphics->DrawImage(myMetafile, 10, 10);
```



<span data-ttu-id="05f0c-131">A ilustração a seguir mostra a saída do código anterior.</span><span class="sxs-lookup"><span data-stu-id="05f0c-131">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="05f0c-132">Observe a suavização, a região de recorte elíptico e a rotação de 30 graus.</span><span class="sxs-lookup"><span data-stu-id="05f0c-132">Note the antialiasing, the elliptical clipping region, and the 30-degree rotation.</span></span>

![captura de tela de uma janela que contém uma elipse preenchida com linhas originadas em um ponto fora da elipse](images/aboutgdip05-art00.png)

 

 



