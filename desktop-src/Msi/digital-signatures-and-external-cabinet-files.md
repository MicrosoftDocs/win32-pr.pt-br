---
description: Windows Installer pode usar assinaturas digitais para detectar recursos corrompidos.
ms.assetid: 49f1c1f9-d342-47e0-8888-2eadc5dbd000
title: Assinaturas digitais e arquivos de gabinete externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f10e921b324a43a919a417f47953c0a44e4777ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828999"
---
# <a name="digital-signatures-and-external-cabinet-files"></a>Assinaturas digitais e arquivos de gabinete externo

Windows Installer pode usar assinaturas digitais para detectar recursos corrompidos. Ao instalar um recurso externo, o certificado de signatário pertencente ao recurso pode ser verificado em relação a um certificado de signatário de referência criado no pacote. O instalador não pode verificar assinaturas para gabinetes internos. Ele só pode verificar assinaturas digitais usando a [tabela MsiDigitalSignature](msidigitalsignature-table.md) e a [tabela MsiDigitalCertificate](msidigitalcertificate-table.md).

Windows Installer faz o seguinte ao instalar um arquivo armazenado em um gabinete externo:

-   O instalador verifica se a entrada de mídia para esse gabinete externo está listada na [tabela MsiDigitalSignature](msidigitalsignature-table.md). Um arquivo armazenado em um gabinete externo é identificado por ter uma entrada na coluna de gabinete da [tabela de mídia](media-table.md) que não é prefixada por um \# caractere ' '.
-   Antes de abrir o gabinete externo, o instalador chama WinVerifyTrust para extrair o certificado atual e as informações de hash. Se houver uma incompatibilidade entre as informações de assinatura atuais no gabinete e as informações de assinatura criadas no pacote, a instalação falhará. A instalação falha porque o gabinete pode ter sido comprometido e não pode ser confiável.

Para obter mais informações sobre o uso de assinaturas digitais, certificados digitais e [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), consulte a seção [segurança](https://msdn.microsoft.com/library/cc527452.aspx) do SDK (Software Development Kit) do Microsoft Windows.

Para obter mais informações, consulte [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), [MsiDigitalCertificate Table](msidigitalcertificate-table.md)e [MsiDigitalSignature Table](msidigitalsignature-table.md).

 

 
