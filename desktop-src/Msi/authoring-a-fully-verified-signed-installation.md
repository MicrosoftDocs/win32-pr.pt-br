---
description: Use estas diretrizes para abranger uma instalação de Windows Installer inteira por uma assinatura digital.
ms.assetid: e70eab94-4615-4a73-bccc-e16bd24551f6
title: Criando uma instalação assinada totalmente verificada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d105b06e3f063d8cbeb1fac579beb12258b20062bf5cbae2cc6d08e9be6e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066176"
---
# <a name="authoring-a-fully-verified-signed-installation"></a>Criando uma instalação assinada totalmente verificada

você pode usar essas diretrizes para cobrir toda a instalação do Windows Installer por uma assinatura digital.

os autores de instalações Windows Installer devem aderir ao seguinte para garantir que todas as partes da instalação sejam cobertas por uma assinatura digital:

-   Use arquivos de gabinete internos ou use arquivos de gabinete externo assinados e crie corretamente a [tabela MsiDigitalSignature](msidigitalsignature-table.md) e a [tabela MsiDigitalCertificate](msidigitalcertificate-table.md).
-   Use apenas ações personalizadas armazenadas no pacote ou instaladas com o pacote.
-   Assine o pacote de instalação.
-   Inclua uma [tabela MsiPatchCertificate](msipatchcertificate-table.md) no pacote. Para habilitar a [aplicação de patches do UAC (controle de conta de usuário)](user-account-control--uac--patching.md), essa tabela deve conter informações usadas para identificar os certificados de signatário usados para assinar digitalmente os patches. A aplicação de patches do UAC permite que o autor do pacote de instalação identifique patches assinados digitalmente que podem ser aplicados no futuro por usuários não administradores.

Para obter um exemplo que mostra como criar uma instalação assinada usando a automação, consulte [criando uma instalação assinada totalmente verificada usando a automação](authoring-a-fully-verified-signed-installation-using-automation.md).

 

 



