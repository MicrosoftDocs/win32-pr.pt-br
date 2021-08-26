---
description: A preparação de recursos para um aplicativo MUI dá suporte a modelos Win32 PE e não Win32 PE.
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: Preparando recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef40453ca6db40bed1c07bad80f7e21cb7adaa7ea48ae8ee5ce2a2a5c657ba2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040666"
---
# <a name="preparing-resources"></a>Preparando recursos

A preparação de recursos para um aplicativo MUI dá suporte a modelos Win32 PE e não Win32 PE. Os recursos do Win32 PE são fornecidos em arquivos baseados em PE, como .dll, .exe ou .sys arquivos. Recursos não Win32 PE são fornecidos em um módulo personalizado de sua escolha.

> [!Note]  
> É altamente recomendável usar recursos do Win32 PE para aplicativos win32 MUI, pois esses recursos têm suporte completo pela tecnologia de recursos da MUI. Arquivos de recurso não Win32 PE podem ser localizados chamando a função [**GetFileMUIPath,**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) conforme descrito em Localizando recursos pe não [Win32](locating-non-win32-pe-resources.md), mas o aplicativo deve fornecer sua própria funcionalidade para localizar e carregar os recursos necessários.

 

Esta seção contém os seguintes tópicos:

-   [Criando o arquivo de recurso de linguagem base](creating-the-base-language-resource-file.md)
-   [Usando o redirecionamento de cadeia de caracteres do Registro](using-registry-string-redirection.md)
-   [Preparando um arquivo de configuração de recurso](preparing-a-resource-configuration-file.md)

 

 



