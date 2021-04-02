---
description: Os módulos de política são programas que recebem solicitações dos serviços de certificados, avaliam essas solicitações e especificam Propriedades opcionais dos certificados que são criados para preencher essas solicitações.
ms.assetid: 23d920ea-af62-42ce-ad48-c7a03ab55fc9
title: Módulos de política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6781a88ab714c402ea1670ac8c18ae4d80eb776e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922616"
---
# <a name="policy-modules"></a>Módulos de política

Os módulos de política são programas que recebem solicitações dos serviços de certificados, avaliam essas solicitações e especificam Propriedades opcionais dos certificados que são criados para preencher essas solicitações. Um módulo de política é implementado como uma dll ( [*biblioteca de vínculo dinâmico*](../secgloss/d-gly.md) ). Um módulo de política pode usar a interface [ICertServerPolicy](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) para se comunicar com os serviços de certificados. Os serviços de certificados se comunicam com um módulo de política por meio de chamadas COM diretas ou, se o módulo não oferecer suporte a chamadas COM diretas, por meio de automação.

Um módulo de política pode exibir as propriedades e extensões de certificado existentes e também pode exibir atributos e propriedades de solicitação. Além disso, um módulo de política pode definir ou modificar extensões de certificado e propriedades "não antes" e "não após", bem como o RDN ( [*nome distinto relativo*](../secgloss/r-gly.md) ) de uma entidade de certificado, sujeito a determinadas restrições. Em última instância, um módulo de política emite ou nega a [*solicitação de certificado*](../secgloss/c-gly.md) ou a mantém pendente.

Antes de gravar um módulo de política personalizada, considere usar um dos módulos de política padrão. A CA (autoridade de [*certificação*](../secgloss/c-gly.md) ) corporativa dos serviços de certificados e a AC autônoma são entregues com um módulo de política padrão apropriado. Os módulos de política padrão empresarial e autônoma emitem solicitações de certificado (embora a política padrão autônoma seja manter o certificado pendente até que seja emitido manualmente por um administrador). Uma autoridade de certificação corporativa deve usar apenas o módulo de política corporativa fornecido pela Microsoft.

A autoridade de certificação corporativa requer Active Directory. Recursos adicionais de seu módulo de política padrão incluem modelos de certificado, segurança de ACL ( [*lista de controle de acesso*](../secgloss/a-gly.md) ) nos modelos de certificado para garantir que as solicitações sejam emitidas somente para as extensões autorizadas e predefinidas adicionadas ao certificado emitido e suporte para certificados de logon de domínio de cartão inteligente.

O módulo de política de autoridade de certificação autônoma padrão não oferece suporte a muitos dos recursos do módulo Enterprise padrão, mas oferece suporte à emissão de certificados de cartão inteligente. Para obter detalhes específicos, bem como os recursos mais atuais do módulo de política padrão, consulte a documentação do produto.

Para instalações em que o módulo de política padrão é inaceitável, os serviços de certificados permitem módulos de política personalizada. Para obter mais informações, consulte [escrevendo módulos de política personalizada](writing-custom-modules.md).

 

 
