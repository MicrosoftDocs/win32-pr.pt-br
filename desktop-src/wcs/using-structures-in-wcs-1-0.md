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
# <a name="using-structures-in-wcs-10"></a>Uso de estruturas no WCS 1.0

A maioria das estruturas usadas pelo WCS 1,0 é muito simples e requer pouca explicação. Eles são documentados na seção de referência do WCS 1,0, [estruturas](structures.md)denominadas.

As exceções são a estrutura [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw) usada pela função [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) e as seguintes estruturas do Windows definidas em WinGDI. h:

-   [BITMAPV5HEADER](#windows-bitmap-header-structures)
-   [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)
-   [**CIEXYZ**](/windows/desktop/api/Wingdi/ns-wingdi-tagciexyz)
-   [**CIEXYZTRIPLE**](/windows/desktop/api/Wingdi/ns-wingdi-tagicexyztriple)

Os tópicos a seguir são discutidos em maior tamanho:

-   [Estruturas de cabeçalho de bitmap do Windows](#windows-bitmap-header-structures)
-   [Diferenças entre os cabeçalhos v4 e V5](#differences-between-v4-and-v5-headers)
-   [Bitmap.exe: um utilitário de Command-Line para converter cabeçalhos de bitmap](#bitmapexe-a-command-line-utility-for-converting-bitmap-headers)

## <a name="windows-bitmap-header-structures"></a>Estruturas de cabeçalho de bitmap do Windows

O WCS 1,0 permite que perfis de cores ICC sejam vinculados ou inseridos em bitmaps independentes de dispositivo (DIBs). Isso permite que as cores de DIB sejam caracterizadas de forma mais precisa do que era possível usando o WCS no Windows 95. [BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , a nova estrutura de cabeçalho de bitmap, é definida em WinGDI. h na versão do Windows 98. Para fins de desenvolvimento, ele também está incluído no arquivo ICM. h com a referência deste programador. A estrutura **BITMAPV5HEADER** é a seguinte:


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



O membro **bV5CSType** pode ter o perfil de valores \_ inserido ou perfil \_ vinculado para especificar se um perfil é inserido ou vinculado com o DIB. O membro **bV5ProfileData** é o deslocamento em bytes do início da estrutura **BITMAPV5HEADER** até o início dos dados do perfil. Se o perfil for inserido, os dados do perfil serão o perfil real e, se estiverem vinculados, os dados do perfil serão o nome do arquivo de término nulo do perfil. Não pode ser uma cadeia de caracteres Unicode. Ele deve ser composto exclusivamente de caracteres do conjunto de caracteres do Windows (página de código 1252).

Quando um DIB é carregado na memória, os dados do perfil (se presente) devem seguir a tabela de cores e **bV5ProfileData** devem dar o deslocamento dos dados do perfil do início da estrutura **BITMAPV5HEADER** . O valor desse membro será diferente agora, pois os bits de bitmap não seguem a tabela de cores na memória. Os aplicativos devem modificar o membro **bV5ProfileData** depois de carregar o DIB na memória.

Para DIBs embalado, os dados de perfil devem seguir os bits de bitmap semelhantes ao formato de arquivo. O membro **bV5ProfileData** ainda deve fornecer o deslocamento dos dados do perfil do início da estrutura **BITMAPV5HEADER** .

Os aplicativos devem acessar os dados do perfil somente quando **bV5Size**  ==  **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** for perfil \_ incorporado ou \_ vinculado.

Se um perfil estiver vinculado, o caminho do perfil poderá ser qualquer nome totalmente qualificado (incluindo um caminho de rede) que pode ser aberto usando a função **CreateFile** Win32.

## <a name="differences-between-v4-and-v5-headers"></a>Diferenças entre os cabeçalhos v4 e V5

Ao trabalhar com a nova estrutura de bitmap, é útil reconhecer diferenças em como as estruturas **BITMAPV4HEADER** e **BITMAPV5HEADER** são configuradas:



| Cabeçalho v4     | Significado                                                                                                                              |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **bV4CSType** | LCS \_ calibraram o \_ RGB. Esse valor implica que os pontos de extremidade e os gamas são fornecidos nos campos apropriados. Valores falsos causam problemas. |
| **bV4CSType** | LCS \_ sRGB. Esse valor indica que o bitmap está no espaço de cores sRGB (gamas e pontos de extremidade ignorados).                                 |
| **bV4CSType** | espaço de cores do Windows do LCS \_ \_ \_ . Esse valor implica que o bitmap está no espaço de cores padrão do Windows.                                    |



 



| Cabeçalho V5     | Significado                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bV5CSType** | LCS \_ calibraram o \_ RGB. Esse valor implica que os pontos de extremidade e os gamas são fornecidos nos campos apropriados. Valores falsos causam problemas.                         |
| **bV5CSType** | LCS \_ sRGB. Esse valor indica que o bitmap está no espaço de cores sRGB (gamas e pontos de extremidade ignorados).                                                         |
| **bV5CSType** | Perfil \_ inserido. Esse valor implica que **bV5ProfileData** aponta para um buffer de memória que contém o perfil a ser usado (os gamas e os pontos de extremidade são ignorados). |
| **bV5CSType** | Perfil \_ vinculado. Esse valor implica que **bV5ProfileData** aponta para o nome de arquivo do perfil a ser usado (os gamas e os pontos de extremidade são ignorados).                |
| **bV5CSType** | espaço de cores do Windows do LCS \_ \_ \_ . Esse valor implica que o bitmap está no espaço de cores padrão do Windows.                                                            |



 

Para converter bitmaps mais antigos de e para a nova estrutura **BITMAPV5HEADER** , um arquivo do utilitário de conversão de linha de comando chamado Bitmap.exe está incluído na referência do programador do WCS 1,0.

## <a name="bitmapexe-a-command-line-utility-for-converting-bitmap-headers"></a>BitMap.exe: um utilitário de Command-Line para converter cabeçalhos de bitmap

Bitmap.exe é um utilitário de linha de comando localizado na \\ pasta bin sob a pasta de instalação que você especificou. Ele modifica os cabeçalhos de bitmaps do Windows, permitindo que você converta os bitmaps existentes das estruturas de cabeçalho **BITMAPINFOHEADER** e **BITMAPV4HEADER** para a estrutura **BITMAPV5HEADER** mais recente e volte novamente. A sintaxe de linha de comando é a seguinte:


```C++
BITMAP [/d] [/1|4|5] [/s] [/f] 
filename
```



As opções de linha de comando têm os seguintes efeitos.



| Comutador | Significado                                                                  |
|--------|--------------------------------------------------------------------------|
| /d     | Os valores padrão são inseridos automaticamente nos cabeçalhos convertidos.       |
| /1     | Converter os bitmaps especificados em **BITMAPINFOHEADER**                    |
| /4     | Converter os bitmaps especificados em **BITMAPV4HEADER**                      |
| /5     | Converter os bitmaps especificados em **BITMAPV5HEADER**                      |
| /f     | Força a conversão, mesmo que o bitmap já tenha o cabeçalho direito       |
| /s     | Converte os bitmaps na pasta especificada e em todos os subdiretórios contidos nele |



 

 

 