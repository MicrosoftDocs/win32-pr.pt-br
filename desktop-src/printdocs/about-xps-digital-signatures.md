---
description: Esta seção fornece uma visão geral da API de assinatura digital do XPS.
ms.assetid: 895974df-d5e8-4974-b057-ec7e5e59d805
title: Sobre a API de assinatura digital do XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba2bad4ef10d8800e9a4cb59289fccb75cc2d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091597"
---
# <a name="about-xps-digital-signature-api"></a>Sobre a API de assinatura digital do XPS

Os documentos XPS podem ter assinaturas digitais para permitir que os usuários assinem um documento, verifiquem a identidade do signatário e indiquem se um documento XPS foi alterado desde que foi assinado. Um aplicativo nativo do Windows pode usar as interfaces da API de assinatura digital XPS para executar operações de assinatura digital em um documento XPS. Esta seção fornece uma visão geral da API de assinatura digital do XPS.

A interface [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) gerencia as operações de assinatura digital em um documento XPS. Antes que um aplicativo possa acessar as assinaturas digitais de um documento XPS, o aplicativo deve chamar [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar um **IXpsSignatureManager** e, em seguida, chamar [**IXpsSignatureManager:: loadpackagefile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) ou [**IXpsSignatureManager:: LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) para carregar o documento XPS. Para obter mais informações sobre esse processo de inicialização, consulte [inicializar o Gerenciador de assinatura](initialize-the-signature-manager.md).

Depois que um documento XPS tiver sido carregado em uma interface [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) , um aplicativo poderá acessar as assinaturas digitais do documento e as solicitações de assinatura digital. Você pode acessar as assinaturas digitais usando uma interface [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) da interface [**IXpsSignatureCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection) do Gerenciador de assinatura. Um aplicativo também pode adicionar e remover interfaces **IXpsSignature** da coleção. As solicitações de assinatura são acessadas usando [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) que são coletadas em uma interface [**IXpsSignatureRequestCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection) . O **IXpsSignatureRequestCollection** faz parte de uma interface [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) que é coletada no [**IXpsSignatureBlockCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection) do Gerenciador de assinatura.

Os aplicativos podem usar o [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) do Gerenciador de assinatura para acessar e definir opções de assinatura digital.

Para obter exemplos de como acessar as assinaturas digitais de um documento XPS, consulte [tarefas comuns de programação de assinatura digital](basic-digital-signature-programming-tasks.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Uso da API de assinatura digital do XPS](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[Referência da API de assinatura digital do XPS](xps-digital-signatures-programming-reference.md)
</dt> <dt>

[Empacotamento](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Standard ECMA-376, formatos de arquivo XML abertos do Office](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
