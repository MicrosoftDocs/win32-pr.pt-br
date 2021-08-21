---
description: Configurando aplicativos de biblioteca
ms.assetid: db375e0f-74ca-44df-918a-b0e48742a594
title: Configurando aplicativos de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8ea0018d74070828384db25d76c73e7b5b3dba8a7dfc7d091c94e38aa0c3bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047494"
---
# <a name="configuring-library-applications"></a>Configurando aplicativos de biblioteca

Como os aplicativos de biblioteca COM+ são executados no processo do cliente, os elementos configuráveis para aplicativos de biblioteca são consideravelmente diferentes dos aplicativos de servidor. Você não pode configurar qualquer aspecto do aplicativo que é determinado pelo processo de hospedagem.

No nível do aplicativo, várias configurações são limitadas ou não disponíveis para aplicativos de biblioteca. Essas restrições são descritas na tabela a seguir:



| Atributo                                       | Descrição                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nível de segurança<br/>                       | Você deve escolher as verificações de acesso no nível do componente. O aplicativo de biblioteca não pode influenciar as verificações de acesso no nível do processo. Consulte [definindo um nível de segurança para verificações de acesso](setting-a-security-level-for-access-checks.md).<br/>             |
| Habilitando ou desabilitando a autenticação<br/> | Você pode indicar se o aplicativo de biblioteca participará da autenticação executada pelo processo de host. Consulte [habilitando a autenticação para um aplicativo de biblioteca](enabling-authentication-for-a-library-application.md).<br/> |
| Nível de representação<br/>                  | Indisponível. A configuração do processo de host é usada. <br/>                                                                                                                                                                             |
| Identidade de segurança<br/>                    | Indisponível. O aplicativo é executado sob a identidade do processo do host.<br/>                                                                                                                                                          |
| Desligamento de processo do servidor<br/>              | Indisponível.<br/>                                                                                                                                                                                                                       |
| Habilitar suporte a 3 GB<br/>                  | Indisponível.<br/>                                                                                                                                                                                                                       |
| Iniciar no depurador<br/>                   | Indisponível.<br/>                                                                                                                                                                                                                       |
| Habilitar CRM<br/>                           | Indisponível.<br/>                                                                                                                                                                                                                       |
| Serviço<br/>                              | Indisponível.<br/>                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do aplicativo COM+](com--application-overview.md)
</dt> </dl>

 

 




