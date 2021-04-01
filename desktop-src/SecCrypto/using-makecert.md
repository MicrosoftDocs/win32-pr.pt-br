---
description: Use comandos MakeCert para criar certificados de teste usando as opções disponíveis com o Internet Explorer versão 4,0 ou posterior.
ms.assetid: 5dbcc8d0-ffd1-4418-adf6-a9805280ee6d
title: Usando MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 068b10d5ce50141ff657379f9c5106cf2733d969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647636"
---
# <a name="using-makecert"></a>Usando MakeCert

Os exemplos a seguir usam comandos [MakeCert](makecert.md) para criar certificados de teste usando opções disponíveis com o Internet Explorer versão 4,0 ou posterior.

-   Faça um certificado emitido pela raiz de teste padrão. Salve o certificado em um arquivo.

    **MakeCert** *MyNew. cer*

-   Faça um certificado emitido pela raiz de teste padrão. Salve-o em um repositório de certificados.

    **MakeCert-SS** *MyNewStore*

-   Faça um certificado emitido pela raiz de teste padrão. Crie um contêiner de chave e salve o certificado em um repositório e em um arquivo.

    **Makecert-sk** *MyNewKey* **-SS** *MyNewStore* *MyNew. cer*

-   Faça um certificado emitido pela raiz de teste padrão. Crie um arquivo de chave privada e salve o certificado em um repositório e em um arquivo.

    **MakeCert-VA** *mykeyfile* **-SS** *MyNewStore* *MyNew. cer*

-   Faça um certificado emitido pela raiz de teste padrão. Crie um contêiner de chave, salve o certificado em um repositório e em um arquivo e torne a chave privada exportável.

    **Makecert-sk** *MyNewKey* **-SS** *MyNewStore* *MyNew. cer* **-PE**

-   Faça um certificado usando a raiz de teste padrão. Salve o certificado em um repositório. Em seguida, faça outro certificado emitido pelo certificado recém-criado. Salve o segundo certificado em outro repositório.

    **Makecert-sk** *MyNewKey* **-SS** *MyNewStore* **MakeCert-is** *MyNewStore* **-SS** *AnotherStore*

-   Faça um certificado usando a raiz de teste padrão. Salve o certificado no meu repositório. Em seguida, faça outro certificado usando o certificado recém-criado. Se houver mais de um certificado no meu repositório, o certificado deverá ser identificado usando seu nome comum.

    **Makecert-sk** *MyNewKey* **-n "CN = XXZZYY"-SS meu MakeCert-is my-in "XXZZYY"-SS** *AnotherStore*

-   Faça um certificado usando a raiz de teste padrão. Salve o certificado no meu repositório e em um arquivo. Em seguida, faça outro certificado usando o certificado *MyNew* recém-criado. Se houver mais de um certificado no meu repositório, identifique exclusivamente o primeiro certificado usando o nome do arquivo de certificado.

    **Makecert-sk** *MyNewKey* **-n "CN = XXZZYY"-SS meu** *MyNew. cer* **MakeCert-is my-IC** *MyNew. cer* **-SS** *AnotherStore*

 

 



