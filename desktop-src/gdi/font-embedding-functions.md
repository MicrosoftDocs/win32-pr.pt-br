---
description: As funções a seguir são usadas com fontes do Microsoft OpenType inseridas.
ms.assetid: 8f47d7a5-db45-4a41-8af2-9fc6b373a531
title: Funções de incorporação de fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ece5b413be5489bf51df38fd92b6f3167823506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988821"
---
# <a name="font-embedding-functions"></a>Funções de incorporação de fontes

As funções a seguir são usadas com fontes do Microsoft OpenType inseridas.



| Função                                                                   | Descrição                                                                                                                                              |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*CFP \_ ALLOCPROC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_allocproc)                                      | Função de alocação de memória fornecida pelo aplicativo para CreateFontPackage e MergeFontPackage.                                                              |
| [*CFP \_ FREEPROC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_freeproc)                                        | Função de desalocação de memória fornecida pelo aplicativo para CreateFontPackage e MergeFontPackage.                                                            |
| [*CFP \_ REALLOCPROC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_reallocproc)                                  | Função de realocação de memória fornecida pelo aplicativo para CreateFontPackage e MergeFontPackage.                                                            |
| [**CreateFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage)                             | Cria uma versão mais compacta de uma fonte TrueType especificada, a fim de passá-la para uma impressora. A fonte resultante pode ser subdividida, compactada ou ambas. |
| [**MergeFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage)                               | Mescla as fontes de subconjuntos criadas por CreateFontPackage.                                                                                                        |
| [*READEMBEDPROC*](/previous-versions//dd162894(v=vs.85))                                       | Função de retorno de chamada fornecida pelo cliente para ler o conteúdo do fluxo de um buffer.                                                                                 |
| [**TTCharToUnicode**](/windows/desktop/api/T2embapi/nf-t2embapi-ttchartounicode)                                 | Converte uma matriz de valores de código de caractere de 8 bits em valores Unicode de 16 bits.                                                                               |
| [**TTDeleteEmbeddedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttdeleteembeddedfont)                       | Libera a memória usada por uma fonte inserida.                                                                                                                |
| [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont)                                         | Cria uma estrutura de fonte que contém uma fonte de caracteres largos (16 bits) subdividida, usando um contexto de dispositivo como fonte de informações de incorporação de fonte.           |
| [**TTEmbedFontEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontex)                                     | Cria uma estrutura de fontes que contém a fonte subdividida de caracteres UCS-4 (32 bits), usando um contexto de dispositivo como fonte de informações de incorporação de fonte.        |
| [**TTEmbedFontFromFileA**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontfromfilea)                       | Cria uma estrutura de fontes que contém uma fonte subdividida de caracteres largos (16 bits), usando um arquivo como fonte de informações de incorporação de fonte.                     |
| [**TTEnableEmbeddingForFacename**](/windows/desktop/api/T2embapi/nf-t2embapi-ttenableembeddingforfacename)       | Adiciona ou remove FaceNames da lista de exclusão de tipos.                                                                                              |
| [**TTGetEmbeddedFontInfo**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetembeddedfontinfo)                     | Recupera informações sobre uma fonte inserida.                                                                                                            |
| [**TTGetEmbeddingType**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetembeddingtype)                           | Retorna os privilégios de inserção de uma fonte.                                                                                                                  |
| [**TTGetNewFontName**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetnewfontname)                               | Cria um novo nome para uma fonte inserida instalada.                                                                                                       |
| [**TTIsEmbeddingEnabled**](/windows/desktop/api/T2embapi/nf-t2embapi-ttisembeddingenabled)                       | Determina se a lista de exclusão de tipos contém uma fonte especificada.                                                                                     |
| [**TTIsEmbeddingEnabledForFacename**](/windows/desktop/api/T2embapi/nf-t2embapi-ttisembeddingenabledforfacename) | Determina se a inserção está habilitada para uma fonte especificada.                                                                                            |
| [**TTLoadEmbeddedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttloadembeddedfont)                           | Lê a fonte inserida do fluxo do documento e a instala. Também permite que um cliente restrinja ainda mais os privilégios de incorporação da fonte.             |
| [**TTRunValidationTests**](/windows/desktop/api/T2embapi/nf-t2embapi-ttrunvalidationtests)                       | Valida a parte ou todos os dados de glifo de uma fonte de caractere largo (16 bits), no intervalo de tamanho especificado.                                                         |
| [**TTRunValidationTestsEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttrunvalidationtestsex)                   | A versão UCS-4 do TTRunValidationTests.                                                                                                                   |
| [*WRITEEMBEDPROC*](/previous-versions//dd145225(v=vs.85))                                     | Função de retorno de chamada fornecida pelo cliente para gravar o conteúdo do fluxo em um buffer.                                                                                  |



 

 

 
