---
description: Esta seção fornece uma visão geral da API de Assinatura Digital XPS.
ms.assetid: 895974df-d5e8-4974-b057-ec7e5e59d805
title: Sobre a API de Assinatura Digital xps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcfbd6000df56d96afbc86a3cd0111c02a128c3c23c0d0de59717da5f4e9ac6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950936"
---
# <a name="about-xps-digital-signature-api"></a>Sobre a API de Assinatura Digital xps

Os documentos XPS podem ter assinaturas digitais para permitir que os usuários assinem um documento, verifiquem a identidade do signante e indiquem se um documento XPS foi alterado desde que foi assinado. Um aplicativo Windows nativo pode usar as interfaces da API de Assinatura Digital XPS para executar operações de assinatura digital em um documento XPS. Esta seção fornece uma visão geral da API de Assinatura Digital XPS.

A interface [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) gerencia as operações de assinatura digital em um documento XPS. Antes que um aplicativo possa acessar as assinaturas digitais de um documento XPS, o aplicativo deve chamar [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar um **IXpsSignatureManager** e, em seguida, chamar [**IXpsSignatureManager::LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) ou [**IXpsSignatureManager::LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) para carregar o documento XPS. Para obter mais informações sobre esse processo de inicialização, [consulte Inicializar o Gerenciador de Assinaturas.](initialize-the-signature-manager.md)

Depois que um documento XPS tiver sido carregado em uma interface [**IXpsSignatureManager,**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) um aplicativo poderá acessar as assinaturas digitais e as solicitações de assinatura digital do documento. Você pode acessar as assinaturas digitais usando uma interface [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) da interface [**IXpsSignatureCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection) do gerenciador de assinaturas. Um aplicativo também pode adicionar e remover interfaces **IXpsSignature** da coleção. As solicitações de assinatura são acessadas usando [**IXpsSignatureRequest,**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) que são coletadas em uma interface [**IXpsSignatureRequestCollection.**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection) A **IXpsSignatureRequestCollection** faz parte de uma interface [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) que são coletadas no [**IXpsSignatureBlockCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection) do gerenciador de assinaturas.

Os aplicativos podem usar [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) do gerenciador de assinaturas para acessar e definir opções de assinatura digital.

Para exemplos de como acessar as assinaturas digitais de um documento XPS, consulte Tarefas comuns de [programação de assinatura digital.](basic-digital-signature-programming-tasks.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Uso da API de assinatura digital do XPS](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[Referência da API de Assinatura Digital XPS](xps-digital-signatures-programming-reference.md)
</dt> <dt>

[Empacotamento](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[ECMA-376 padrão, Office abrir formatos de arquivo XML](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
