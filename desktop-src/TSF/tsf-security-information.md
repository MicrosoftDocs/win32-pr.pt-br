---
title: Estrutura de serviços de texto de considerações sobre segurança
description: Estrutura de serviços de texto de considerações sobre segurança
ms.assetid: c1250ca0-3887-4519-888f-2ed436a39917
keywords:
- TSF (estrutura de serviços de texto), segurança
- TSF (estrutura de serviços de texto), segurança
- serviços de texto, segurança
- Aplicativos habilitados para TSF, segurança
- segurança para TSF
- TSF (estrutura de serviços de texto), práticas recomendadas
- TSF (estrutura de serviços de texto), práticas recomendadas
- Aplicativos habilitados para TSF, práticas recomendadas
- serviços de texto, práticas recomendadas
- práticas recomendadas para TSF
- TSF (estrutura de serviços de texto), verificação de erros
- TSF (estrutura de serviços de texto), verificação de erros
- Aplicativos habilitados para TSF, verificação de erros
- serviços de texto, verificação de erros
- verificação de erros
- TSF (estrutura de serviços de texto), assinaturas digitais
- TSF (estrutura de serviços de texto), assinaturas digitais
- serviços de texto, assinaturas digitais
- Aplicativos habilitados para TSF, assinaturas digitais
- assinaturas digitais
- TSF (estrutura de serviços de texto), chamadas LoadLibrary
- TSF (estrutura de serviços de texto), chamadas LoadLibrary
- serviços de texto, chamadas LoadLibrary
- Aplicativos habilitados para TSF, chamadas LoadLibrary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 432418fbcb6221082083d6595aa374939bc2f4d5cf5aad145cac87444e75bdc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118873571"
---
# <a name="security-considerations-text-services-framework"></a>Considerações de segurança: estrutura de serviços de texto

## <a name="best-practices-for-developing-with-tsf"></a>Práticas recomendadas para o desenvolvimento com o TSF

-   **Assinaturas digitais:** Os provedores de serviço de texto devem fornecer assinaturas digitais com seus executáveis binários. Um serviço de texto registrado tem acesso a threads do sistema e pode expor informações que, de outra forma, não seriam acessíveis. Para ajudar a garantir uma operação estável e segura, o usuário deve verificar a assinatura digital de um serviço de texto antes que o serviço de texto tenha permissão para ser carregado. Consulte [introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) para obter o procedimento adequado para criar uma assinatura digital.
-   **Verificação de erro:** Cada método ou chamada de função deve ser verificada em busca de sucesso. Em caso de falha, o método ou as chamadas de função restantes devem ser ignorados. A maioria dos exemplos de código nesta documentação tem verificação de erro limitada, ou nenhum, para evitar o disfarce do ponto a ser ilustrado. Você não deve colar exemplos da documentação diretamente no código de produção; em vez disso, você deve aprimorar os exemplos adicionando sua própria verificação de erro.

-   **Chamadas LoadLibrary:** Para obter um ponteiro para qualquer uma das [funções de TSF](text-services-framework-functions.md), você precisará usar [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). No entanto, é importante seguir os procedimentos para formatar o nome do caminho da DLL, conforme fornecido na documentação **LoadLibrary** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Práticas recomendadas de segurança](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
</dt> <dt>

[Funções de TSF](text-services-framework-functions.md)
</dt> <dt>

[LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 