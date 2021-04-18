---
title: Uso de estruturas no WCS 1.0
description: A maioria das estruturas usadas pelo WCS 1,0 é muito simples e requer pouca explicação. Eles são documentados na seção de referência do WCS 1,0, estruturas denominadas.
ms.assetid: 8d3682e2-38fd-4a33-b386-ab0716bb6972
keywords:
- WCS (sistema de cores do Windows), estruturas
- WCS (sistema de cores do Windows), estruturas
- gerenciamento de cores de imagem, estruturas
- gerenciamento de cores, estruturas
- cores, estruturas
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d6e434ccfa6d96aa815f0c1997dc7f34178a32
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105780767"
---
# <a name="using-structures-in-wcs-10"></a><span data-ttu-id="2d5d5-109">Uso de estruturas no WCS 1.0</span><span class="sxs-lookup"><span data-stu-id="2d5d5-109">Using Structures in WCS 1.0</span></span>

<span data-ttu-id="2d5d5-110">A maioria das estruturas usadas pelo WCS 1,0 é muito simples e requer pouca explicação.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-110">Most of the structures used by WCS 1.0 are very straightforward and require little explanation.</span></span> <span data-ttu-id="2d5d5-111">Eles são documentados na seção de referência do WCS 1,0, [estruturas](structures.md)denominadas.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-111">They are documented in the WCS 1.0 Reference section entitled [Structures](structures.md).</span></span>

<span data-ttu-id="2d5d5-112">As exceções são a estrutura [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw) usada pela função [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) e as seguintes estruturas do Windows definidas em WinGDI. h:</span><span class="sxs-lookup"><span data-stu-id="2d5d5-112">Exceptions are the [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw) structure used by the [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) function, and the following Windows structures defined in Wingdi.h:</span></span>

-   [<span data-ttu-id="2d5d5-113">BITMAPV5HEADER</span><span class="sxs-lookup"><span data-stu-id="2d5d5-113">BITMAPV5HEADER</span></span>](#windows-bitmap-header-structures)
-   [<span data-ttu-id="2d5d5-114">**LOGCOLORSPACE**</span><span class="sxs-lookup"><span data-stu-id="2d5d5-114">**LOGCOLORSPACE**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)
-   [<span data-ttu-id="2d5d5-115">**CIEXYZ**</span><span class="sxs-lookup"><span data-stu-id="2d5d5-115">**CIEXYZ**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-tagciexyz)
-   [<span data-ttu-id="2d5d5-116">**CIEXYZTRIPLE**</span><span class="sxs-lookup"><span data-stu-id="2d5d5-116">**CIEXYZTRIPLE**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-tagicexyztriple)

<span data-ttu-id="2d5d5-117">Os tópicos a seguir são discutidos em maior tamanho:</span><span class="sxs-lookup"><span data-stu-id="2d5d5-117">The following topics are discussed at greater length:</span></span>

-   [<span data-ttu-id="2d5d5-118">Estruturas de cabeçalho de bitmap do Windows</span><span class="sxs-lookup"><span data-stu-id="2d5d5-118">Windows Bitmap Header Structures</span></span>](#windows-bitmap-header-structures)
-   [<span data-ttu-id="2d5d5-119">Diferenças entre os cabeçalhos v4 e V5</span><span class="sxs-lookup"><span data-stu-id="2d5d5-119">Differences Between V4 and V5 Headers</span></span>](#differences-between-v4-and-v5-headers)
-   [<span data-ttu-id="2d5d5-120">Bitmap.exe: um utilitário de Command-Line para converter cabeçalhos de bitmap</span><span class="sxs-lookup"><span data-stu-id="2d5d5-120">Bitmap.exe: a Command-Line Utility for Converting Bitmap Headers</span></span>](#bitmapexe-a-command-line-utility-for-converting-bitmap-headers)

## <a name="windows-bitmap-header-structures"></a><span data-ttu-id="2d5d5-121">Estruturas de cabeçalho de bitmap do Windows</span><span class="sxs-lookup"><span data-stu-id="2d5d5-121">Windows Bitmap Header Structures</span></span>

<span data-ttu-id="2d5d5-122">O WCS 1,0 permite que perfis de cores ICC sejam vinculados ou inseridos em bitmaps independentes de dispositivo (DIBs).</span><span class="sxs-lookup"><span data-stu-id="2d5d5-122">WCS 1.0 allows ICC color profiles to be linked or embedded in device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="2d5d5-123">Isso permite que as cores de DIB sejam caracterizadas de forma mais precisa do que era possível usando o WCS no Windows 95.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-123">This allows DIB colors to be characterized more accurately than was possible using WCS in Windows 95.</span></span> <span data-ttu-id="2d5d5-124">[BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , a nova estrutura de cabeçalho de bitmap, é definida em WinGDI. h na versão do Windows 98.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-124">[BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , the new bitmap header structure, is defined in Wingdi.h in the release of Windows 98.</span></span> <span data-ttu-id="2d5d5-125">Para fins de desenvolvimento, ele também está incluído no arquivo ICM. h com a referência deste programador.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-125">For development purposes, it is also included in the file Icm.h with this Programmer's Reference.</span></span> <span data-ttu-id="2d5d5-126">A estrutura **BITMAPV5HEADER** é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="2d5d5-126">The **BITMAPV5HEADER** structure is as follows:</span></span>


```C++
typedef struct {
    DWORD        bV5Size;
    LONG         bV5Width;
    LONG         bV5Height;
    WORD         bV5Planes;
    WORD         bV5BitCount;
    DWORD        bV5Compression;
    DWORD        bV5SizeImage;
    LONG         bV5XPelsPerMeter;
    LONG         bV5YPelsPerMeter;
    DWORD        bV5ClrUsed;
    DWORD        bV5ClrImportant;
    DWORD        bV5RedMask;
    DWORD        bV5GreenMask;
    DWORD        bV5BlueMask;
    DWORD        bV5AlphaMask;
    DWORD        bV5CSType;
    CIEXYZTRIPLE bV5Endpoints;
    DWORD        bV5GammaRed;
    DWORD        bV5GammaGreen;
    DWORD        bV5GammaBlue;
    DWORD        bV5Intent;         // Rendering intent for bitmap 
    DWORD        bV5ProfileData;    // Offset to profile data 
    DWORD        bV5ProfileSize;    // Size of embedded profile data 
    DWORD        bV5Reserved;       // Should be zero 
} BITMAPV5HEADER, FAR *LPBITMAPV5HEADER, *PBITMAPV5HEADER;
```



<span data-ttu-id="2d5d5-127">O membro **bV5CSType** pode ter o perfil de valores \_ inserido ou perfil \_ vinculado para especificar se um perfil é inserido ou vinculado com o DIB.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-127">The member **bV5CSType** can have the values PROFILE\_EMBEDDED or PROFILE\_LINKED to specify whether a profile is embedded or linked with the DIB.</span></span> <span data-ttu-id="2d5d5-128">O membro **bV5ProfileData** é o deslocamento em bytes do início da estrutura **BITMAPV5HEADER** até o início dos dados do perfil.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-128">The member **bV5ProfileData** is the offset in bytes from the beginning of the **BITMAPV5HEADER** structure to the start of the profile data.</span></span> <span data-ttu-id="2d5d5-129">Se o perfil for inserido, os dados do perfil serão o perfil real e, se estiverem vinculados, os dados do perfil serão o nome do arquivo de término nulo do perfil.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-129">If the profile is embedded, profile data is the actual profile, and if it is linked, the profile data is the null-terminated file name of the profile.</span></span> <span data-ttu-id="2d5d5-130">Não pode ser uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-130">This cannot be a Unicode string.</span></span> <span data-ttu-id="2d5d5-131">Ele deve ser composto exclusivamente de caracteres do conjunto de caracteres do Windows (página de código 1252).</span><span class="sxs-lookup"><span data-stu-id="2d5d5-131">It must be composed exclusively of characters from the Windows character set (code page 1252).</span></span>

<span data-ttu-id="2d5d5-132">Quando um DIB é carregado na memória, os dados do perfil (se presente) devem seguir a tabela de cores e **bV5ProfileData** devem dar o deslocamento dos dados do perfil do início da estrutura **BITMAPV5HEADER** .</span><span class="sxs-lookup"><span data-stu-id="2d5d5-132">When a DIB is loaded into memory, the profile data (if present) should follow the color table, and **bV5ProfileData** should give the offset of the profile data from the beginning of the **BITMAPV5HEADER** structure.</span></span> <span data-ttu-id="2d5d5-133">O valor desse membro será diferente agora, pois os bits de bitmap não seguem a tabela de cores na memória.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-133">The value of this member will be different now, as the bitmap bits do not follow the color table in memory.</span></span> <span data-ttu-id="2d5d5-134">Os aplicativos devem modificar o membro **bV5ProfileData** depois de carregar o DIB na memória.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-134">Applications should modify the **bV5ProfileData** member after loading the DIB into memory.</span></span>

<span data-ttu-id="2d5d5-135">Para DIBs embalado, os dados de perfil devem seguir os bits de bitmap semelhantes ao formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-135">For packed DIBs, the profile data should follow the bitmap bits similar to the file format.</span></span> <span data-ttu-id="2d5d5-136">O membro **bV5ProfileData** ainda deve fornecer o deslocamento dos dados do perfil do início da estrutura **BITMAPV5HEADER** .</span><span class="sxs-lookup"><span data-stu-id="2d5d5-136">The **bV5ProfileData** member should still give the offset of the profile data from the beginning of the **BITMAPV5HEADER** structure.</span></span>

<span data-ttu-id="2d5d5-137">Os aplicativos devem acessar os dados do perfil somente quando **bV5Size**  ==  **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** for perfil \_ incorporado ou \_ vinculado.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-137">Applications should access the profile data only when **bV5Size** == **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** is PROFILE\_EMBEDDED or PROFILE\_LINKED.</span></span>

<span data-ttu-id="2d5d5-138">Se um perfil estiver vinculado, o caminho do perfil poderá ser qualquer nome totalmente qualificado (incluindo um caminho de rede) que pode ser aberto usando a função **CreateFile** Win32.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-138">If a profile is linked, the path of the profile can be any fully qualified name (including a network path) that can be opened using the Win32 **CreateFile** function.</span></span>

## <a name="differences-between-v4-and-v5-headers"></a><span data-ttu-id="2d5d5-139">Diferenças entre os cabeçalhos v4 e V5</span><span class="sxs-lookup"><span data-stu-id="2d5d5-139">Differences Between V4 and V5 Headers</span></span>

<span data-ttu-id="2d5d5-140">Ao trabalhar com a nova estrutura de bitmap, é útil reconhecer diferenças em como as estruturas **BITMAPV4HEADER** e **BITMAPV5HEADER** são configuradas:</span><span class="sxs-lookup"><span data-stu-id="2d5d5-140">In working with the new bitmap structure, it is useful to recognize differences in how **BITMAPV4HEADER** and **BITMAPV5HEADER** structures are set up:</span></span>



| <span data-ttu-id="2d5d5-141">Cabeçalho v4</span><span class="sxs-lookup"><span data-stu-id="2d5d5-141">V4 Header</span></span>     | <span data-ttu-id="2d5d5-142">Significado</span><span class="sxs-lookup"><span data-stu-id="2d5d5-142">Meaning</span></span>                                                                                                                              |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d5d5-143">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="2d5d5-143">**bV4CSType**</span></span> | <span data-ttu-id="2d5d5-144">LCS \_ calibraram o \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-144">LCS\_CALIBRATED\_RGB.</span></span> <span data-ttu-id="2d5d5-145">Esse valor implica que os pontos de extremidade e os gamas são fornecidos nos campos apropriados.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-145">This value implies that end points and gammas are given in the appropriate fields.</span></span> <span data-ttu-id="2d5d5-146">Valores falsos causam problemas.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-146">Bogus values cause trouble.</span></span> |
| <span data-ttu-id="2d5d5-147">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="2d5d5-147">**bV4CSType**</span></span> | <span data-ttu-id="2d5d5-148">LCS \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-148">LCS\_sRGB.</span></span> <span data-ttu-id="2d5d5-149">Esse valor indica que o bitmap está no espaço de cores sRGB (gamas e pontos de extremidade ignorados).</span><span class="sxs-lookup"><span data-stu-id="2d5d5-149">This value implies that the bitmap is in sRGB color space (gammas and endpoints ignored).</span></span>                                 |
| <span data-ttu-id="2d5d5-150">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="2d5d5-150">**bV4CSType**</span></span> | <span data-ttu-id="2d5d5-151">espaço de cores do Windows do LCS \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2d5d5-151">LCS\_WINDOWS\_COLOR\_SPACE.</span></span> <span data-ttu-id="2d5d5-152">Esse valor implica que o bitmap está no espaço de cores padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-152">This value implies that the bitmap is in Windows default color space.</span></span>                                    |



 



| <span data-ttu-id="2d5d5-153">Cabeçalho V5</span><span class="sxs-lookup"><span data-stu-id="2d5d5-153">V5 Header</span></span>     | <span data-ttu-id="2d5d5-154">Significado</span><span class="sxs-lookup"><span data-stu-id="2d5d5-154">Meaning</span></span>                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d5d5-155">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="2d5d5-155">**bV5CSType**</span></span> | <span data-ttu-id="2d5d5-156">LCS \_ calibraram o \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-156">LCS\_CALIBRATED\_RGB.</span></span> <span data-ttu-id="2d5d5-157">Esse valor implica que os pontos de extremidade e os gamas são fornecidos nos campos apropriados.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-157">This value implies that end points and gammas are given in the appropriate fields.</span></span> <span data-ttu-id="2d5d5-158">Valores falsos causam problemas.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-158">Bogus values cause trouble.</span></span>                         |
| <span data-ttu-id="2d5d5-159">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="2d5d5-159">**bV5CSType**</span></span> | <span data-ttu-id="2d5d5-160">LCS \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-160">LCS\_sRGB.</span></span> <span data-ttu-id="2d5d5-161">Esse valor indica que o bitmap está no espaço de cores sRGB (gamas e pontos de extremidade ignorados).</span><span class="sxs-lookup"><span data-stu-id="2d5d5-161">This value implies that the bitmap is in sRGB color space (gammas and endpoints ignored).</span></span>                                                         |
| <span data-ttu-id="2d5d5-162">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="2d5d5-162">**bV5CSType**</span></span> | <span data-ttu-id="2d5d5-163">Perfil \_ inserido.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-163">PROFILE\_EMBEDDED.</span></span> <span data-ttu-id="2d5d5-164">Esse valor implica que **bV5ProfileData** aponta para um buffer de memória que contém o perfil a ser usado (os gamas e os pontos de extremidade são ignorados).</span><span class="sxs-lookup"><span data-stu-id="2d5d5-164">This value implies that **bV5ProfileData** points to a memory buffer that contains the profile to use (gammas and endpoints are ignored).</span></span> |
| <span data-ttu-id="2d5d5-165">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="2d5d5-165">**bV5CSType**</span></span> | <span data-ttu-id="2d5d5-166">Perfil \_ vinculado.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-166">PROFILE\_LINKED.</span></span> <span data-ttu-id="2d5d5-167">Esse valor implica que **bV5ProfileData** aponta para o nome de arquivo do perfil a ser usado (os gamas e os pontos de extremidade são ignorados).</span><span class="sxs-lookup"><span data-stu-id="2d5d5-167">This value implies that **bV5ProfileData** points to the file name of the profile to use (gammas and endpoints are ignored).</span></span>                |
| <span data-ttu-id="2d5d5-168">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="2d5d5-168">**bV5CSType**</span></span> | <span data-ttu-id="2d5d5-169">espaço de cores do Windows do LCS \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2d5d5-169">LCS\_WINDOWS\_COLOR\_SPACE.</span></span> <span data-ttu-id="2d5d5-170">Esse valor implica que o bitmap está no espaço de cores padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-170">This value implies that the bitmap is in Windows default color space.</span></span>                                                            |



 

<span data-ttu-id="2d5d5-171">Para converter bitmaps mais antigos de e para a nova estrutura **BITMAPV5HEADER** , um arquivo do utilitário de conversão de linha de comando chamado Bitmap.exe está incluído na referência do programador do WCS 1,0.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-171">In order to convert older bitmaps to and from the new **BITMAPV5HEADER** structure, a command-line conversion utility file named Bitmap.exe is included in the WCS 1.0 Programmer's Reference.</span></span>

## <a name="bitmapexe-a-command-line-utility-for-converting-bitmap-headers"></a><span data-ttu-id="2d5d5-172">BitMap.exe: um utilitário de Command-Line para converter cabeçalhos de bitmap</span><span class="sxs-lookup"><span data-stu-id="2d5d5-172">BitMap.exe: a Command-Line Utility for Converting Bitmap Headers</span></span>

<span data-ttu-id="2d5d5-173">Bitmap.exe é um utilitário de linha de comando localizado na \\ pasta bin sob a pasta de instalação que você especificou.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-173">Bitmap.exe is a command-line utility located in the \\Bin folder under the installation folder that you specified.</span></span> <span data-ttu-id="2d5d5-174">Ele modifica os cabeçalhos de bitmaps do Windows, permitindo que você converta os bitmaps existentes das estruturas de cabeçalho **BITMAPINFOHEADER** e **BITMAPV4HEADER** para a estrutura **BITMAPV5HEADER** mais recente e volte novamente.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-174">It modifies the headers of Windows bitmaps, allowing you to convert existing bitmaps from **BITMAPINFOHEADER** and **BITMAPV4HEADER** header structures to the newer **BITMAPV5HEADER** structure and back again.</span></span> <span data-ttu-id="2d5d5-175">A sintaxe de linha de comando é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="2d5d5-175">The command-line syntax is as follows:</span></span>


```C++
BITMAP [/d] [/1|4|5] [/s] [/f] 
filename
```



<span data-ttu-id="2d5d5-176">As opções de linha de comando têm os seguintes efeitos.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-176">The command-line switches have the following effects.</span></span>



| <span data-ttu-id="2d5d5-177">Comutador</span><span class="sxs-lookup"><span data-stu-id="2d5d5-177">Switch</span></span> | <span data-ttu-id="2d5d5-178">Significado</span><span class="sxs-lookup"><span data-stu-id="2d5d5-178">Meaning</span></span>                                                                  |
|--------|--------------------------------------------------------------------------|
| <span data-ttu-id="2d5d5-179">/d</span><span class="sxs-lookup"><span data-stu-id="2d5d5-179">/d</span></span>     | <span data-ttu-id="2d5d5-180">Os valores padrão são inseridos automaticamente nos cabeçalhos convertidos.</span><span class="sxs-lookup"><span data-stu-id="2d5d5-180">Default values are automatically entered in the converted headers.</span></span>       |
| <span data-ttu-id="2d5d5-181">/1</span><span class="sxs-lookup"><span data-stu-id="2d5d5-181">/1</span></span>     | <span data-ttu-id="2d5d5-182">Converter os bitmaps especificados em **BITMAPINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="2d5d5-182">Convert the specified bitmaps to **BITMAPINFOHEADER**</span></span>                    |
| <span data-ttu-id="2d5d5-183">/4</span><span class="sxs-lookup"><span data-stu-id="2d5d5-183">/4</span></span>     | <span data-ttu-id="2d5d5-184">Converter os bitmaps especificados em **BITMAPV4HEADER**</span><span class="sxs-lookup"><span data-stu-id="2d5d5-184">Convert the specified bitmaps to **BITMAPV4HEADER**</span></span>                      |
| <span data-ttu-id="2d5d5-185">/5</span><span class="sxs-lookup"><span data-stu-id="2d5d5-185">/5</span></span>     | <span data-ttu-id="2d5d5-186">Converter os bitmaps especificados em **BITMAPV5HEADER**</span><span class="sxs-lookup"><span data-stu-id="2d5d5-186">Convert the specified bitmaps to **BITMAPV5HEADER**</span></span>                      |
| <span data-ttu-id="2d5d5-187">/f</span><span class="sxs-lookup"><span data-stu-id="2d5d5-187">/f</span></span>     | <span data-ttu-id="2d5d5-188">Força a conversão, mesmo que o bitmap já tenha o cabeçalho direito</span><span class="sxs-lookup"><span data-stu-id="2d5d5-188">Forces conversion, even if the bitmap already has the right header</span></span>       |
| <span data-ttu-id="2d5d5-189">/s</span><span class="sxs-lookup"><span data-stu-id="2d5d5-189">/s</span></span>     | <span data-ttu-id="2d5d5-190">Converte os bitmaps na pasta especificada e em todos os subdiretórios contidos nele</span><span class="sxs-lookup"><span data-stu-id="2d5d5-190">Converts bitmaps in the specified folder and all subdirectories under it</span></span> |



 

 

 