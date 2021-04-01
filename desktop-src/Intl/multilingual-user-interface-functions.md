---
description: As funções a seguir são usadas com MUI (Multilingual User interface).
ms.assetid: 918d1f04-78fe-4b60-bee7-08d2f131437e
title: Funções de interface do usuário multilíngüe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f082115b0b12bdf6d26923ed8fc941b89887723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090949"
---
# <a name="multilingual-user-interface-functions"></a>Funções de interface do usuário multilíngüe

As funções a seguir são usadas com MUI (Multilingual User interface).



| Função                                                                 | Descrição                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa)                               | Enumera os idiomas da interface do usuário que estão disponíveis no sistema operacional.                                     |
| [**EnumUILanguagesProc**](/windows/win32/api/winnls/nc-winnls-uilanguage_enumproca)                       | Uma função definida pelo aplicativo usada com a função [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) .                      |
| [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary)                                 | Decrementa a contagem de referência de um módulo de recurso carregado por [ **LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)                  |
| [**GetFileMUIInfo**](/windows/desktop/api/Winnls/nf-winnls-getfilemuiinfo)                                 | Recupera informações relacionadas a recursos sobre um arquivo.                                                                    |
| [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)                                 | Recupera o caminho para um arquivo de recurso específico de idioma associado ao arquivo LN fornecido.                           |
| [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages) | Recupera os idiomas de interface do usuário preferenciais do processo.                                                                           |
| [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)         | Recupera o identificador de idioma do idioma da interface do usuário padrão do sistema, conhecido como "idioma de instalação" no Windows Vista. |
| [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)   | Recupera os idiomas de interface do usuário preferenciais do sistema.                                                                            |
| [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)   | Recupera os idiomas da interface do usuário preferencial do thread para o thread atual.                                                     |
| [**GetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getthreaduilanguage)                       | Retorna o identificador de idioma do primeiro idioma da interface do usuário para o thread atual.                            |
| [**GetUILanguageFallbackList**](/windows/desktop/api/Muiload/nf-muiload-getuilanguagefallbacklist)           | Obtém uma lista de fallback de idiomas de interface do usuário representados como nomes de idioma.                                         |
| [**GetUILanguageInfo**](/windows/desktop/api/Winnls/nf-winnls-getuilanguageinfo)                           | Recupera uma variedade de informações sobre um idioma de interface do usuário.                                                     |
| [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage)             | Retorna o identificador de idioma para o idioma da interface do usuário do usuário atual.                                          |
| [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)       | Recupera os idiomas de interface do usuário preferenciais.                                                                              |
| [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)                                 | Retorna um identificador para os recursos específicos do idioma associados a um arquivo de idioma específico (LN).            |
| [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) | Define os idiomas de interface do usuário preferenciais do processo para o processo do aplicativo.                                                    |
| [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)   | Define os idiomas de interface do usuário preferenciais do thread.                                                                                 |
| [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage)                       | Define o idioma preferencial da interface do usuário para o thread atual.                                                      |



 

 

 
