---
description: Windows O instalador pode usar assinaturas digitais para detectar recursos corrompidos.
ms.assetid: 49f1c1f9-d342-47e0-8888-2eadc5dbd000
title: Assinaturas digitais e arquivos de gabinete externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40edd8527eb93a6b970b3a8ce18fec8cc81f4688804a4e18f7ec5cdd748f3eca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947449"
---
# <a name="digital-signatures-and-external-cabinet-files"></a>Assinaturas digitais e arquivos de gabinete externos

Windows O instalador pode usar assinaturas digitais para detectar recursos corrompidos. Ao instalar um recurso externo, o certificado de signante que pertence ao recurso pode ser verificado em relação a um certificado de signante de referência autor no pacote. O instalador não pode verificar assinaturas para gabinetes internos. Ele só pode verificar assinaturas digitais usando a [tabela MsiDigitalSignature](msidigitalsignature-table.md) e a [tabela MsiDigitalCertificate](msidigitalcertificate-table.md).

Windows O instalador faz o seguinte ao instalar um arquivo armazenado em um gabinete externo:

-   O instalador verifica se a entrada de mídia para esse gabinete externo está listada na [tabela MsiDigitalSignature](msidigitalsignature-table.md). Um arquivo armazenado em um gabinete externo é identificado por [](media-table.md) ter uma entrada na coluna Gabinete da tabela Mídia que não é prefixada por um \# caractere ' ' .
-   Antes de abrir o gabinete externo, o instalador chama WinVerifyTrust para extrair o certificado atual e as informações de hash. Se houver uma incompatibilidade entre as informações de assinatura atuais no gabinete e as informações de assinatura do pacote, a instalação falhará. A instalação falha porque o gabinete pode ter sido comprometido e não pode ser confiável.

Para obter mais informações sobre o uso de assinaturas digitais, certificados [](https://msdn.microsoft.com/library/cc527452.aspx) digitais e [**WinVerifyTrust,**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust)consulte a seção Segurança do Microsoft Windows Software Development Kit (SDK).

Para obter mais informações, consulte [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), [tabela MsiDigitalCertificate](msidigitalcertificate-table.md)e [tabela MsiDigitalSignature](msidigitalsignature-table.md).

 

 
