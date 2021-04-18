---
description: A preparação de recursos para um aplicativo MUI dá suporte aos modelos Win32 PE e não Win32 PE.
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: Preparando recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ca7655535318fa7a385993e6a55f9e7b6110ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105800048"
---
# <a name="preparing-resources"></a>Preparando recursos

A preparação de recursos para um aplicativo MUI dá suporte aos modelos Win32 PE e não Win32 PE. Os recursos do Win32 PE são fornecidos em arquivos baseados em PE, como arquivos. dll,. exe ou. sys. Os recursos do PE não Win32 são fornecidos em um módulo personalizado de sua escolha.

> [!Note]  
> É altamente recomendável que você use recursos do Win32 PE para aplicativos MUI do Win32, pois esses recursos têm suporte completo da tecnologia de recursos do MUI. Arquivos de recurso PE não Win32 podem ser localizados chamando a função [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) conforme descrito em [localizando recursos não Win32 PE](locating-non-win32-pe-resources.md), mas o aplicativo deve fornecer sua própria funcionalidade para localizar e carregar os recursos necessários.

 

Esta seção contém os seguintes tópicos:

-   [Criando o arquivo de recurso de idioma base](creating-the-base-language-resource-file.md)
-   [Usando o redirecionamento de cadeia de caracteres do registro](using-registry-string-redirection.md)
-   [Preparando um arquivo de configuração de recurso](preparing-a-resource-configuration-file.md)

 

 



