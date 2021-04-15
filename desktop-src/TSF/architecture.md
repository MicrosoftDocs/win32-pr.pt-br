---
title: Arquitetura (estrutura de serviços de texto)
description: Arquitetura
ms.assetid: 6ef6ba1f-fcbb-4ede-bc6f-3da66135ea69
keywords:
- TSF (estrutura de serviços de texto), arquitetura
- TSF (estrutura de serviços de texto), arquitetura
- serviços de texto, arquitetura
- Aplicativos habilitados para TSF, arquitetura
- TSF (estrutura de serviços de texto), componentes
- TSF (estrutura de serviços de texto), componentes
- serviços de texto, componentes
- Aplicativos habilitados para TSF, componentes
- TSF (estrutura de serviços de texto), aplicativos
- TSF (estrutura de serviços de texto), aplicativos
- serviços de texto, aplicativos
- Aplicativos habilitados para TSF, sobre
- TSF (estrutura de serviços de texto), serviços de texto
- TSF (estrutura de serviços de texto), serviços de texto
- serviços de texto, sobre
- Aplicativos habilitados para TSF, serviços de texto
- TSF (estrutura de serviços de texto), Gerenciador de TSF
- TSF (estrutura de serviços de texto), Gerenciador de TSF
- serviços de texto, Gerenciador de TSF
- Aplicativos habilitados para TSF, Gerenciador de TSF
- Gerenciador de TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0a300307b3099b4a28a883d5c830c4078cd0bb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104569707"
---
# <a name="architecture-text-services-framework"></a>Arquitetura (estrutura de serviços de texto)

A estrutura de serviços de texto inclui três componentes principais:

-   **Aplicativos:** As operações de aplicativo normalmente incluem exibição, edição direta e armazenamento de texto. Um aplicativo fornece acesso ao texto implementando um servidor COM que dá suporte a determinadas interfaces e se comunica com o TSF usando interfaces que o Gerenciador TSF expõe. Em toda esta documentação, o termo, aplicativo, se refere a um aplicativo habilitado para TSF, a menos que especificado de outra forma.
-   **Serviços de texto:** Um serviço de texto funciona como um provedor de texto para um aplicativo. Um serviço de texto pode obter texto de e gravar texto em um aplicativo. Um serviço de texto também pode associar dados e propriedades com um bloco de texto. Um serviço de texto é implementado como um servidor em processo COM que se registra no TSF. Quando registrado, o usuário interage com o serviço de texto usando a barra de idiomas ou os atalhos de teclado. Vários serviços de texto podem ser instalados.
-   **Gerenciador de TSF:** O Gerenciador de TSF funciona como um mediador entre um aplicativo e um ou mais serviços de texto. Um serviço de texto nunca interage diretamente com um aplicativo. Toda a comunicação passa pelo Gerenciador de TSF. O Gerenciador de TSF é implementado pelo sistema operacional e não pode ser substituído. Ao longo desta documentação, o termo, gerente, refere-se ao Gerenciador do TSF, a menos que especificado de outra forma.

A ilustração a seguir mostra os principais elementos de arquitetura do TSF.

![arquitetura da estrutura de serviços de texto](images/tsf-arch.gif)

Com essa arquitetura, o Gerenciador do TSF fornece uma camada de abstração entre aplicativos e serviços de texto. Essa camada de abstração permite que um aplicativo e um ou mais serviços de texto compartilhem texto e permite que o Gerenciador do TSF gerencie serviços de texto.

 

 




