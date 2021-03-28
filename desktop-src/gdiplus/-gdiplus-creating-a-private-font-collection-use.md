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
# <a name="creating-a-private-font-collection"></a>Criar uma coleções de fontes privadas

A classe [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) herda da classe base de [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) abstrata. Você pode usar um objeto **PrivateFontCollection** para manter um conjunto de fontes especificamente para seu aplicativo.

Uma coleção de fontes privada pode incluir fontes do sistema instalado, bem como as fontes que não foram instaladas no computador. Para adicionar um arquivo de fonte a uma coleção de fontes privada, chame o método [**PrivateFontCollection:: AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) de um objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) .

> [!Note]  
> Ao usar a API GDI+, você nunca deve permitir que seu aplicativo Baixe fontes arbitrárias de fontes não confiáveis. O sistema operacional requer privilégios elevados para garantir que todas as fontes instaladas sejam confiáveis.

 

O método [**FontCollection:: getfamílias**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) de um objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) retorna uma matriz de objetos [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) . Antes de chamar **FontCollection:: getfamílias**, você deve alocar um buffer grande o suficiente para manter essa matriz. Para determinar o tamanho do buffer necessário, chame o método [**FontCollection:: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) e multiplique o valor de retorno por **sizeof**(**FontFamily**).

A quantidade de famílias de fonte em uma coleção de fontes privada não é necessariamente a mesma que a quantidade de arquivos de fonte que foram adicionados à coleção. Por exemplo, suponha que os arquivos ArialBd.tff, Times.tff e TimesBd.tff foram adicionados a uma coleção. Haverá três arquivos, mas somente duas famílias na coleção, pois Times.tff e TimesBd.tff pertencem à mesma família.

O exemplo a seguir adiciona os três arquivos de fonte a seguir a um objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) :

-   C: \\ \\ fontes WinNT \\ Arial. tff (Arial, regular)
-   C: \\ WinNT \\ fonts \\ CourBI. tff (Courier New, negrito itálico)
-   C: \\ WinNT \\ fonts \\ TimesBd. tff (Times New Roman, negrito)

O código chama o método [**FontCollection:: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) do objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) para determinar o número de famílias na coleção particular e, em seguida, chama [**FontCollection:: getfamílias**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) para recuperar uma matriz de objetos [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .

Para cada objeto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) na coleção, o código chama o método [**FontFamily:: IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) para determinar se vários estilos (regular, negrito, itálico, negrito itálico, sublinhado e riscado) estão disponíveis. Os argumentos passados para o método **FontFamily:: IsStyleAvailable** são membros da enumeração [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , que é declarada em Gdiplusenums. h.

Se uma combinação de família/estilo específica estiver disponível, um objeto de [**fonte**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) será construído usando essa família e estilo. O primeiro argumento passado para o construtor **Font** é o nome da família de fontes (não um objeto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) como é o caso para outras variações do construtor **Font** ) e o argumento final é o endereço do objeto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) . Depois que o objeto **Font** é construído, seu endereço é passado para o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para exibir o nome da família junto com o nome do estilo.


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



A ilustração a seguir mostra a saída do código anterior.

![captura de tela de uma janela que lista nove nomes de fonte, cada um deles demonstra a fonte nomeada](images/fontstext7.png)

Arial. tff (que foi adicionado à coleção de fontes privadas no exemplo de código anterior) é o arquivo de fonte para o estilo Arial regular. No entanto, observe que a saída de programa mostra vários estilos disponíveis além de regular para família de fonte Arial. Isso ocorre porque o Windows GDI+ pode simular os estilos de negrito, itálico e negrito itálico do estilo regular. A GDI+ também pode produzir sublinhados e riscados a partir do estilo regular.

Da mesma forma, o GDI+ pode simular o estilo negrito em itálico do estilo negrito ou itálico. A saída do programa mostra que o estilo negrito e itálico está disponível para a família Times, embora TimesBd.tff (Times New Roman, negrito) seja o único arquivo Times na coleção.

Esta tabela especifica as fontes que não são do sistema que o GDI+ suporta.



|                     | GDI | GDI+ no Windows 7 | GDI+ no Windows 8 | DirectWrite |
|---------------------|-----|-------------------|-------------------|-------------|
| . FON                | sim | não                | não                | não          |
| . FNT                | sim | não                | não                | não          |
| . TTF                | sim | sim               | sim               | sim         |
| . OTF com TrueType  | sim | sim               | sim               | sim         |
| . OTF com o CFF da Adobe | sim | não                | sim               | sim         |
| Adobe tipo 1        | sim | não                | não                | não          |



 

 

 



