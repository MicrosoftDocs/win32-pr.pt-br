---
description: A classe PrivateFontCollection herda da classe base de FontCollection abstrata. Você pode usar um objeto PrivateFontCollection para manter um conjunto de fontes especificamente para seu aplicativo.
ms.assetid: ae12afcf-12cc-4c84-9aba-de56fc39437b
title: Criar uma coleções de fontes privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084e8a2d6f79f60e0719f04fbabb778b9483bd80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165468"
---
# <a name="creating-a-private-font-collection"></a><span data-ttu-id="0cd81-104">Criar uma coleções de fontes privadas</span><span class="sxs-lookup"><span data-stu-id="0cd81-104">Creating a Private Font Collection</span></span>

<span data-ttu-id="0cd81-105">A classe [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) herda da classe base de [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) abstrata.</span><span class="sxs-lookup"><span data-stu-id="0cd81-105">The [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) class inherits from the [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) abstract base class.</span></span> <span data-ttu-id="0cd81-106">Você pode usar um objeto **PrivateFontCollection** para manter um conjunto de fontes especificamente para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0cd81-106">You can use a **PrivateFontCollection** object to maintain a set of fonts specifically for your application.</span></span>

<span data-ttu-id="0cd81-107">Uma coleção de fontes privada pode incluir fontes do sistema instalado, bem como as fontes que não foram instaladas no computador.</span><span class="sxs-lookup"><span data-stu-id="0cd81-107">A private font collection can include installed system fonts as well as fonts that have not been installed on the computer.</span></span> <span data-ttu-id="0cd81-108">Para adicionar um arquivo de fonte a uma coleção de fontes privada, chame o método [**PrivateFontCollection:: AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) de um objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) .</span><span class="sxs-lookup"><span data-stu-id="0cd81-108">To add a font file to a private font collection, call the [**PrivateFontCollection::AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) method of a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object.</span></span>

> [!Note]  
> <span data-ttu-id="0cd81-109">Ao usar a API GDI+, você nunca deve permitir que seu aplicativo Baixe fontes arbitrárias de fontes não confiáveis.</span><span class="sxs-lookup"><span data-stu-id="0cd81-109">When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources.</span></span> <span data-ttu-id="0cd81-110">O sistema operacional requer privilégios elevados para garantir que todas as fontes instaladas sejam confiáveis.</span><span class="sxs-lookup"><span data-stu-id="0cd81-110">The operating system requires elevated privileges to assure that all installed fonts are trusted.</span></span>

 

<span data-ttu-id="0cd81-111">O método [**FontCollection:: getfamílias**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) de um objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) retorna uma matriz de objetos [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="0cd81-111">The [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) method of a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object returns an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span> <span data-ttu-id="0cd81-112">Antes de chamar **FontCollection:: getfamílias**, você deve alocar um buffer grande o suficiente para manter essa matriz.</span><span class="sxs-lookup"><span data-stu-id="0cd81-112">Before you call **FontCollection::GetFamilies**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="0cd81-113">Para determinar o tamanho do buffer necessário, chame o método [**FontCollection:: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) e multiplique o valor de retorno por **sizeof**(**FontFamily**).</span><span class="sxs-lookup"><span data-stu-id="0cd81-113">To determine the size of the required buffer, call the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method and multiply the return value by **sizeof**(**FontFamily**).</span></span>

<span data-ttu-id="0cd81-114">A quantidade de famílias de fonte em uma coleção de fontes privada não é necessariamente a mesma que a quantidade de arquivos de fonte que foram adicionados à coleção.</span><span class="sxs-lookup"><span data-stu-id="0cd81-114">The number of font families in a private font collection is not necessarily the same as the number of font files that have been added to the collection.</span></span> <span data-ttu-id="0cd81-115">Por exemplo, suponha que os arquivos ArialBd.tff, Times.tff e TimesBd.tff foram adicionados a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="0cd81-115">For example, suppose you add the files ArialBd.tff, Times.tff, and TimesBd.tff to a collection.</span></span> <span data-ttu-id="0cd81-116">Haverá três arquivos, mas somente duas famílias na coleção, pois Times.tff e TimesBd.tff pertencem à mesma família.</span><span class="sxs-lookup"><span data-stu-id="0cd81-116">There will be three files but only two families in the collection because Times.tff and TimesBd.tff belong to the same family.</span></span>

<span data-ttu-id="0cd81-117">O exemplo a seguir adiciona os três arquivos de fonte a seguir a um objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) :</span><span class="sxs-lookup"><span data-stu-id="0cd81-117">The following example adds the following three font files to a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object:</span></span>

-   <span data-ttu-id="0cd81-118">C: \\ \\ fontes WinNT \\ Arial. tff (Arial, regular)</span><span class="sxs-lookup"><span data-stu-id="0cd81-118">C:\\WINNT\\Fonts\\Arial.tff (Arial, regular)</span></span>
-   <span data-ttu-id="0cd81-119">C: \\ WinNT \\ fonts \\ CourBI. tff (Courier New, negrito itálico)</span><span class="sxs-lookup"><span data-stu-id="0cd81-119">C:\\WINNT\\Fonts\\CourBI.tff (Courier New, bold italic)</span></span>
-   <span data-ttu-id="0cd81-120">C: \\ WinNT \\ fonts \\ TimesBd. tff (Times New Roman, negrito)</span><span class="sxs-lookup"><span data-stu-id="0cd81-120">C:\\WINNT\\Fonts\\TimesBd.tff (Times New Roman, bold)</span></span>

<span data-ttu-id="0cd81-121">O código chama o método [**FontCollection:: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) do objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) para determinar o número de famílias na coleção particular e, em seguida, chama [**FontCollection:: getfamílias**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) para recuperar uma matriz de objetos [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="0cd81-121">The code calls the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method of the [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object to determine the number of families in the private collection, and then calls [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) to retrieve an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span>

<span data-ttu-id="0cd81-122">Para cada objeto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) na coleção, o código chama o método [**FontFamily:: IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) para determinar se vários estilos (regular, negrito, itálico, negrito itálico, sublinhado e riscado) estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0cd81-122">For each [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object in the collection, the code calls the [**FontFamily::IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) method to determine whether various styles (regular, bold, italic, bold italic, underline, and strikeout) are available.</span></span> <span data-ttu-id="0cd81-123">Os argumentos passados para o método **FontFamily:: IsStyleAvailable** são membros da enumeração [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , que é declarada em Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="0cd81-123">The arguments passed to the **FontFamily::IsStyleAvailable** method are members of the [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) enumeration, which is declared in Gdiplusenums.h.</span></span>

<span data-ttu-id="0cd81-124">Se uma combinação de família/estilo específica estiver disponível, um objeto de [**fonte**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) será construído usando essa família e estilo.</span><span class="sxs-lookup"><span data-stu-id="0cd81-124">If a particular family/style combination is available, a [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) object is constructed using that family and style.</span></span> <span data-ttu-id="0cd81-125">O primeiro argumento passado para o construtor **Font** é o nome da família de fontes (não um objeto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) como é o caso para outras variações do construtor **Font** ) e o argumento final é o endereço do objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) .</span><span class="sxs-lookup"><span data-stu-id="0cd81-125">The first argument passed to the **Font** constructor is the font family name (not a [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object as is the case for other variations of the **Font** constructor), and the final argument is the address of the [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object.</span></span> <span data-ttu-id="0cd81-126">Depois que o objeto **Font** é construído, seu endereço é passado para o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para exibir o nome da família junto com o nome do estilo.</span><span class="sxs-lookup"><span data-stu-id="0cd81-126">After the **Font** object is constructed, its address is passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to display the family name along with the name of the style.</span></span>


```
#define MAX_STYLE_SIZE 20
#define MAX_FACEANDSTYLE_SIZE (LF_FACESIZE + MAX_STYLE_SIZE + 2)

PointF      pointF(10.0f, 0.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 0));
INT                   count = 0;
INT                   found = 0;
WCHAR                 familyName[LF_FACESIZE];
WCHAR                 familyNameAndStyle[MAX_FACEANDSTYLE_SIZE]; 
FontFamily*           pFontFamily;
PrivateFontCollection privateFontCollection;

// Add three font files to the private collection.
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\Arial.ttf");
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\CourBI.ttf");
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\TimesBd.ttf");

// How many font families are in the private collection?
count = privateFontCollection.GetFamilyCount();

// Allocate a buffer to hold the array of FontFamily
// objects returned by GetFamilies.
pFontFamily = new FontFamily[count];

// Get the array of FontFamily objects.
privateFontCollection.GetFamilies(count, pFontFamily, &found);

// Display the name of each font family in the private collection
// along with the available styles for that font family.
for(INT j = 0; j < count; ++j)
{
   // Get the font family name.
   pFontFamily[j].GetFamilyName(familyName);
   
   // Is the regular style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleRegular))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Regular");

      Font* pFont = new Font(
         familyName, 16, FontStyleRegular, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);      
   }

   // Is the bold style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleBold))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Bold");

      Font* pFont = new Font(
         familyName, 16, FontStyleBold, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Is the italic style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleItalic))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Italic");

      Font* pFont = new Font(
         familyName, 16, FontStyleItalic, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Is the bold italic style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleBoldItalic))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" BoldItalic");

      Font* pFont = new Font(familyName, 16, 
         FontStyleBoldItalic, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
    }

   // Is the underline style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleUnderline))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Underline");

      Font* pFont = new Font(familyName, 16, 
         FontStyleUnderline, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0);
      delete(pFont);
   }
 
   // Is the strikeout style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleStrikeout))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Strikeout");

      Font* pFont = new Font(familyName, 16, 
         FontStyleStrikeout, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Separate the families with white space.
   pointF.Y += 10.0f;

} // for

delete pFontFamily;
            
```



<span data-ttu-id="0cd81-127">A ilustração a seguir mostra a saída do código anterior.</span><span class="sxs-lookup"><span data-stu-id="0cd81-127">The following illustration shows the output of the preceding code.</span></span>

![captura de tela de uma janela que lista nove nomes de fonte, cada um deles demonstra a fonte nomeada](images/fontstext7.png)

<span data-ttu-id="0cd81-129">Arial. tff (que foi adicionado à coleção de fontes privadas no exemplo de código anterior) é o arquivo de fonte para o estilo Arial regular.</span><span class="sxs-lookup"><span data-stu-id="0cd81-129">Arial.tff (which was added to the private font collection in the preceding code example) is the font file for the Arial regular style.</span></span> <span data-ttu-id="0cd81-130">No entanto, observe que a saída de programa mostra vários estilos disponíveis além de regular para família de fonte Arial.</span><span class="sxs-lookup"><span data-stu-id="0cd81-130">Note, however, that the program output shows several available styles other than regular for the Arial font family.</span></span> <span data-ttu-id="0cd81-131">Isso ocorre porque o Windows GDI+ pode simular os estilos de negrito, itálico e negrito itálico do estilo regular.</span><span class="sxs-lookup"><span data-stu-id="0cd81-131">That is because Windows GDI+ can simulate the bold, italic, and bold italic styles from the regular style.</span></span> <span data-ttu-id="0cd81-132">A GDI+ também pode produzir sublinhados e riscados a partir do estilo regular.</span><span class="sxs-lookup"><span data-stu-id="0cd81-132">GDI+ can also produce underlines and strikeouts from the regular style.</span></span>

<span data-ttu-id="0cd81-133">Da mesma forma, o GDI+ pode simular o estilo negrito em itálico do estilo negrito ou itálico.</span><span class="sxs-lookup"><span data-stu-id="0cd81-133">Similarly, GDI+ can simulate the bold italic style from either the bold style or the italic style.</span></span> <span data-ttu-id="0cd81-134">A saída do programa mostra que o estilo negrito e itálico está disponível para a família Times, embora TimesBd.tff (Times New Roman, negrito) seja o único arquivo Times na coleção.</span><span class="sxs-lookup"><span data-stu-id="0cd81-134">The program output shows that the bold italic style is available for the Times family even though TimesBd.tff (Times New Roman, bold) is the only Times file in the collection.</span></span>

<span data-ttu-id="0cd81-135">Esta tabela especifica as fontes que não são do sistema que o GDI+ suporta.</span><span class="sxs-lookup"><span data-stu-id="0cd81-135">This table specifies the non-system fonts that GDI+ supports.</span></span>



|                     | <span data-ttu-id="0cd81-136">GDI</span><span class="sxs-lookup"><span data-stu-id="0cd81-136">GDI</span></span> | <span data-ttu-id="0cd81-137">GDI+ no Windows 7</span><span class="sxs-lookup"><span data-stu-id="0cd81-137">GDI+ on Windows 7</span></span> | <span data-ttu-id="0cd81-138">GDI+ no Windows 8</span><span class="sxs-lookup"><span data-stu-id="0cd81-138">GDI+ on Windows 8</span></span> | <span data-ttu-id="0cd81-139">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="0cd81-139">DirectWrite</span></span> |
|---------------------|-----|-------------------|-------------------|-------------|
| <span data-ttu-id="0cd81-140">. FON</span><span class="sxs-lookup"><span data-stu-id="0cd81-140">.FON</span></span>                | <span data-ttu-id="0cd81-141">sim</span><span class="sxs-lookup"><span data-stu-id="0cd81-141">yes</span></span> | <span data-ttu-id="0cd81-142">não</span><span class="sxs-lookup"><span data-stu-id="0cd81-142">no</span></span>                | <span data-ttu-id="0cd81-143">não</span><span class="sxs-lookup"><span data-stu-id="0cd81-143">no</span></span>                | <span data-ttu-id="0cd81-144">não</span><span class="sxs-lookup"><span data-stu-id="0cd81-144">no</span></span>          |
| <span data-ttu-id="0cd81-145">. FNT</span><span class="sxs-lookup"><span data-stu-id="0cd81-145">.FNT</span></span>                | <span data-ttu-id="0cd81-146">sim</span><span class="sxs-lookup"><span data-stu-id="0cd81-146">yes</span></span> | <span data-ttu-id="0cd81-147">não</span><span class="sxs-lookup"><span data-stu-id="0cd81-147">no</span></span>                | <span data-ttu-id="0cd81-148">não</span><span class="sxs-lookup"><span data-stu-id="0cd81-148">no</span></span>                | <span data-ttu-id="0cd81-149">não</span><span class="sxs-lookup"><span data-stu-id="0cd81-149">no</span></span>          |
| <span data-ttu-id="0cd81-150">. TTF</span><span class="sxs-lookup"><span data-stu-id="0cd81-150">.TTF</span></span>                | <span data-ttu-id="0cd81-151">sim</span><span class="sxs-lookup"><span data-stu-id="0cd81-151">yes</span></span> | <span data-ttu-id="0cd81-152">sim</span><span class="sxs-lookup"><span data-stu-id="0cd81-152">yes</span></span>               | <span data-ttu-id="0cd81-153">sim</span><span class="sxs-lookup"><span data-stu-id="0cd81-153">yes</span></span>               | <span data-ttu-id="0cd81-154">sim</span><span class="sxs-lookup"><span data-stu-id="0cd81-154">yes</span></span>         |
| <span data-ttu-id="0cd81-155">. OTF com TrueType</span><span class="sxs-lookup"><span data-stu-id="0cd81-155">.OTF with TrueType</span></span>  | <span data-ttu-id="0cd81-156">sim</span><span class="sxs-lookup"><span data-stu-id="0cd81-156">yes</span></span> | <span data-ttu-id="0cd81-157">sim</span><span class="sxs-lookup"><span data-stu-id="0cd81-157">yes</span></span>               | <span data-ttu-id="0cd81-158">sim</span><span class="sxs-lookup"><span data-stu-id="0cd81-158">yes</span></span>               | <span data-ttu-id="0cd81-159">sim</span><span class="sxs-lookup"><span data-stu-id="0cd81-159">yes</span></span>         |
| <span data-ttu-id="0cd81-160">. OTF com o CFF da Adobe</span><span class="sxs-lookup"><span data-stu-id="0cd81-160">.OTF with Adobe CFF</span></span> | <span data-ttu-id="0cd81-161">sim</span><span class="sxs-lookup"><span data-stu-id="0cd81-161">yes</span></span> | <span data-ttu-id="0cd81-162">não</span><span class="sxs-lookup"><span data-stu-id="0cd81-162">no</span></span>                | <span data-ttu-id="0cd81-163">sim</span><span class="sxs-lookup"><span data-stu-id="0cd81-163">yes</span></span>               | <span data-ttu-id="0cd81-164">sim</span><span class="sxs-lookup"><span data-stu-id="0cd81-164">yes</span></span>         |
| <span data-ttu-id="0cd81-165">Adobe tipo 1</span><span class="sxs-lookup"><span data-stu-id="0cd81-165">Adobe Type 1</span></span>        | <span data-ttu-id="0cd81-166">sim</span><span class="sxs-lookup"><span data-stu-id="0cd81-166">yes</span></span> | <span data-ttu-id="0cd81-167">não</span><span class="sxs-lookup"><span data-stu-id="0cd81-167">no</span></span>                | <span data-ttu-id="0cd81-168">não</span><span class="sxs-lookup"><span data-stu-id="0cd81-168">no</span></span>                | <span data-ttu-id="0cd81-169">não</span><span class="sxs-lookup"><span data-stu-id="0cd81-169">no</span></span>          |



 

 

 



