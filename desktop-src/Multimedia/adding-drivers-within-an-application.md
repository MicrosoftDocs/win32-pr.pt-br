---
title: Adicionando drivers dentro de um aplicativo
description: Adicionando drivers dentro de um aplicativo
ms.assetid: cd9bd0a8-652b-440b-a197-81e20a9d71f1
keywords:
- Gerenciador de compactação de áudio (ACM), adicionando drivers
- ACM (Gerenciador de compactação de áudio), adicionando drivers
- Exemplos do ACM, adicionando drivers
- adicionando drivers
- função acmDriverAdd
- drivers globais
- drivers locais
- Gerenciador de compactação de áudio (ACM), drivers globais
- ACM (Gerenciador de compactação de áudio), drivers globais
- Gerenciador de compactação de áudio (ACM), drivers locais
- ACM (Gerenciador de compactação de áudio), drivers locais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c4cce1310a487e772ac6f65680221f065335951d7d1d6c6dd22c4178c0d985f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692326"
---
# <a name="adding-drivers-within-an-application"></a>Adicionando drivers dentro de um aplicativo

Se você precisar que seu aplicativo implemente suas próprias rotinas de compactação internamente, o aplicativo poderá adicionar drivers ao ACM chamando a função [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) . O aplicativo implementa o driver fornecendo uma função que está de acordo com o protótipo do [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) . Depois que o aplicativo tiver adicionado o driver, o aplicativo poderá usar o driver por meio do ACM, pois ele usaria qualquer outro driver.

O ACM trata os drivers como global ou local. Um aplicativo especifica se um driver deve ser adicionado como global ou local quando chama **acmDriverAdd**. Há duas diferenças entre os drivers globais e locais:

-   Drivers adicionados como drivers globais não são compartilhados com outros aplicativos.
-   Um aplicativo pode alterar diretamente a prioridade de um driver global (mas não de um driver local) chamando a função [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) . O ACM realiza uma pesquisa priorizada ao procurar um driver apropriado para fornecer uma implementação de uma chamada de função. O ACM sempre fornece aos drivers locais prioridade mais alta do que os drivers globais. O driver local adicionado mais recentemente tem a prioridade mais alta.

 

 




