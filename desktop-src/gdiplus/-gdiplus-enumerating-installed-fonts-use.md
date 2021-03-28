---
description: A classe InstalledFontCollection herda da classe base de FontCollection abstrata.
ms.assetid: 59598f66-4241-4766-a2f0-5de736de959e
title: Enumeração de fontes instaladas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f41242522c2575ffb08e53f7100380ac9a849d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165463"
---
# <a name="enumerating-installed-fonts"></a><span data-ttu-id="68244-103">Enumeração de fontes instaladas</span><span class="sxs-lookup"><span data-stu-id="68244-103">Enumerating Installed Fonts</span></span>

<span data-ttu-id="68244-104">A classe [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection) herda da classe base de [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) abstrata.</span><span class="sxs-lookup"><span data-stu-id="68244-104">The [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection) class inherits from the [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) abstract base class.</span></span> <span data-ttu-id="68244-105">Você pode usar um objeto **InstalledFontCollection** para enumerar as fontes instaladas no computador.</span><span class="sxs-lookup"><span data-stu-id="68244-105">You can use an **InstalledFontCollection** object to enumerate the fonts installed on the computer.</span></span> <span data-ttu-id="68244-106">O método [**FontCollection:: getfamílias**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) de um objeto **InstalledFontCollection** retorna uma matriz de objetos [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="68244-106">The [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) method of an **InstalledFontCollection** object returns an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span> <span data-ttu-id="68244-107">Antes de chamar **FontCollection:: getfamílias**, você deve alocar um buffer grande o suficiente para manter essa matriz.</span><span class="sxs-lookup"><span data-stu-id="68244-107">Before you call **FontCollection::GetFamilies**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="68244-108">Para determinar o tamanho do buffer necessário, chame o método [**FontCollection:: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) e multiplique o valor de retorno por **sizeof**(**FontFamily**).</span><span class="sxs-lookup"><span data-stu-id="68244-108">To determine the size of the required buffer, call the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method and multiply the return value by **sizeof**(**FontFamily**).</span></span>

<span data-ttu-id="68244-109">O exemplo a seguir lista os nomes de todas as famílias de fontes instaladas no computador.</span><span class="sxs-lookup"><span data-stu-id="68244-109">The following example lists the names of all the font families installed on the computer.</span></span> <span data-ttu-id="68244-110">O código recupera os nomes de família de fontes chamando o método [**FontFamily:: Getfamilyname**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getfamilyname) de cada objeto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) na matriz retornada por [**FontCollection:: getfamílias**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies).</span><span class="sxs-lookup"><span data-stu-id="68244-110">The code retrieves the font family names by calling the [**FontFamily::GetFamilyName**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getfamilyname) method of each [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object in the array returned by [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies).</span></span> <span data-ttu-id="68244-111">À medida que os nomes de família são recuperados, eles são concatenados para formar uma lista separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="68244-111">As the family names are retrieved, they are concatenated to form a comma-separated list.</span></span> <span data-ttu-id="68244-112">Em seguida, o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) desenha a lista separada por vírgulas em um retângulo.</span><span class="sxs-lookup"><span data-stu-id="68244-112">Then the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class draws the comma-separated list in a rectangle.</span></span>


```
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 8, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 500.0f, 500.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 0));

INT          count = 0;
INT          found = 0;
WCHAR        familyName[LF_FACESIZE];  // enough space for one family name
WCHAR*       familyList = NULL;
FontFamily*  pFontFamily = NULL;

InstalledFontCollection installedFontCollection;

// How many font families are installed?
count = installedFontCollection.GetFamilyCount();

// Allocate a buffer to hold the array of FontFamily
// objects returned by GetFamilies.
pFontFamily = new FontFamily[count];

// Get the array of FontFamily objects.
installedFontCollection.GetFamilies(count, pFontFamily, &found);

// The loop below creates a large string that is a comma-separated
// list of all font family names.
// Allocate a buffer large enough to hold that string.
familyList = new WCHAR[count*(sizeof(familyName)+ 3)];
StringCchCopy(familyList, 1, L"");

for(INT j = 0; j < count; ++j)
{
   pFontFamily[j].GetFamilyName(familyName);  
   StringCchCatW(familyList, count*(sizeof(familyName)+ 3), familyName);
   StringCchCatW(familyList, count*(sizeof(familyName)+ 3), L",  ");
}

// Draw the large string (list of all families) in a rectangle.
graphics.DrawString(
   familyList, -1, &font, rectF, NULL, &solidBrush);

delete [] pFontFamily;
delete [] familyList;
            
```



<span data-ttu-id="68244-113">A ilustração a seguir mostra uma possível saída do código anterior.</span><span class="sxs-lookup"><span data-stu-id="68244-113">The following illustration shows a possible output of the preceding code.</span></span> <span data-ttu-id="68244-114">Se você executar o código, a saída poderá ser diferente, dependendo das fontes instaladas no computador.</span><span class="sxs-lookup"><span data-stu-id="68244-114">If you run the code, the output might be different, depending on the fonts installed on your computer.</span></span>

![captura de tela de uma janela que contém uma lista separada por vírgulas de famílias de fontes instaladas](images/fontstext6.png)

 

 



