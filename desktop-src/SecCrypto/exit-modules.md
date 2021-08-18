---
description: Os módulos de saída recebem notificações do mecanismo de servidor quando ocorrem operações como a emissão de um certificado.
ms.assetid: 5e7ee1f4-7e07-4a08-8e72-89b449804bc2
title: Módulos de saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38ba8d821900ece1a4ce3eb3fcb2cc805d87274b451a3d5c8948d1e86ebf3547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140749"
---
# <a name="exit-modules"></a>Módulos de saída

Os módulos de saída recebem notificações do mecanismo de servidor quando ocorrem operações como a emissão de um certificado. Um módulo de saída é implementado como uma DLL [*(biblioteca de vínculo*](../secgloss/d-gly.md) dinâmico). Uma operação típica para um módulo de saída é publicar um certificado concluído em um local especificado (o módulo de saída da autoridade de certificação corporativa padrão, por exemplo, publica certificados de usuário e CRLs [*(listas*](../secgloss/c-gly.md) de certificados revogados) no Active Directory). Um módulo de saída pode usar a interface [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) para se comunicar com os Serviços de Certificados. Os Serviços de Certificados se comunicam com um módulo de saída por meio de chamadas COM diretas ou, se o módulo não dá suporte a chamadas COM diretas, por meio da Automação.

Um módulo de saída pode exibir propriedades e extensões de certificado existentes e também pode exibir atributos e propriedades de solicitação. No entanto, um módulo de saída não pode modificar nenhuma propriedade.

Os Serviços de Certificados fornece um módulo de saída padrão, mas você também pode criar módulos de saída personalizados para atender às necessidades especiais. No entanto, antes de escrever um módulo de saída personalizado, considere usar o módulo de saída padrão. Além disso, para uma autoridade de certificação corporativa, o módulo de saída padrão sempre deve ser usado, mesmo que você possa adicionar módulos de saída personalizados adicionais. Para obter mais informações, consulte [Escrevendo módulos de saída personalizados.](writing-custom-exit-modules.md)

 

 
