---
description: Os módulos de política são programas que recebem solicitações dos Serviços de Certificados, avaliam essas solicitações e especificam propriedades opcionais dos certificados que são criadas para preencher essas solicitações.
ms.assetid: 23d920ea-af62-42ce-ad48-c7a03ab55fc9
title: Módulos de política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11fd84b91b66e811134bb5878bf3a000363aef7bf9321bbff5a23ad3d25158f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978813"
---
# <a name="policy-modules"></a>Módulos de política

Os módulos de política são programas que recebem solicitações dos Serviços de Certificados, avaliam essas solicitações e especificam propriedades opcionais dos certificados que são criadas para preencher essas solicitações. Um módulo de política é implementado como uma DLL (biblioteca [*de vínculo*](../secgloss/d-gly.md) dinâmico). Um módulo de política pode usar a interface [ICertServerPolicy](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) para se comunicar com os Serviços de Certificados. Os Serviços de Certificados se comunicam com um módulo de política por meio de chamadas COM diretas ou, se o módulo não dá suporte a chamadas COM diretas, por meio da Automação.

Um módulo de política pode exibir propriedades e extensões de certificado existentes e também pode exibir atributos e propriedades de solicitação. Além disso, um módulo de política pode definir ou modificar extensões de certificado e propriedades "NotBefore" e "NotAfter", bem como o RDN [*(nome*](../secgloss/r-gly.md) diferenciado relativo) de uma Pessoa de Certificado, sujeito a determinadas restrições. Um módulo de política, em última análise, emite ou nega [*a solicitação de certificado*](../secgloss/c-gly.md) ou a mantém pendente.

Antes de escrever um módulo de política personalizado, considere o uso de um dos módulos de política padrão. A AC [*(autoridade*](../secgloss/c-gly.md) de certificação) corporativa dos Serviços de Certificados e a AC autônomo são fornecidas com um módulo de política padrão apropriado. Os módulos de política padrão corporativo e autônomo emitam solicitações de certificado (embora a política padrão autônomo seja manter o certificado pendente até que ele seja emitido manualmente por um administrador). Uma autoridade de certificação corporativa deve usar apenas o módulo de política corporativa fornecido pela Microsoft.

A AC corporativa requer o Active Directory. Recursos adicionais de seu módulo de política padrão incluem modelos de [*certificado,*](../secgloss/a-gly.md) segurança de ACL (lista de controle de acesso) nos modelos de certificado para garantir que as solicitações sejam emitidas apenas para as extensões autorizadas predefinida adicionadas ao certificado emitido e suporte para certificados de logon de domínio de cartão inteligente.

O módulo de política de AC autônomo padrão não dá suporte a muitos dos recursos do módulo empresarial padrão, mas dá suporte à emissão de certificados de cartão inteligente. Para obter detalhes específicos, bem como os recursos mais atuais do módulo de política padrão, consulte a documentação do produto.

Para instalações em que o módulo de política padrão é inaceitável, os Serviços de Certificados permitem módulos de política personalizados. Para obter mais informações, consulte [Escrevendo módulos de política personalizados.](writing-custom-modules.md)

 

 
