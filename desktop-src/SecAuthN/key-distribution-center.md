---
description: O centro de distribuição de chaves (KDC) é implementado como um serviço de domínio. Ele usa o Active Directory como seu banco de dados de conta e o catálogo global para direcionar referências para KDCs em outros domínios.
ms.assetid: f2a7c87c-9be7-4fd8-8ecd-4edf1f2336ef
title: centro de distribuição de chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f473fc3b84fed05e157fa700e7549f025979a90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011142"
---
# <a name="key-distribution-center"></a>centro de distribuição de chaves

O centro de distribuição de chaves (KDC) é implementado como um serviço de domínio. Ele usa o Active Directory como seu banco de dados de conta e o catálogo global para direcionar referências para KDCs em outros domínios.

Como em outras implementações do [*protocolo Kerberos*](../secgloss/k-gly.md), o KDC é um único processo que fornece dois serviços:

-   Serviço de autenticação (AS)

    Esse serviço emite tíquetes de concessão de tíquetes (TGTs) para conexão com o serviço de concessão de tíquetes em seu próprio domínio ou em qualquer domínio confiável. Antes que um cliente possa solicitar um tíquete para outro computador, ele deve solicitar um TGT do serviço de autenticação no domínio da conta do cliente. O serviço de autenticação retorna um TGT para o serviço de concessão de tíquete no domínio do computador de destino. O TGT pode ser reutilizado até expirar, mas o primeiro acesso a qualquer serviço de concessão de tíquetes de domínio sempre exige uma viagem para o serviço de autenticação no domínio da conta do cliente.

-   Serviço de Ticket-Granting (TGS)

    Esse serviço emite tíquetes para conexão com computadores em seu próprio domínio. Quando os clientes querem acesso a um computador, eles entram em contato com o serviço de concessão de tíquete no domínio do computador de destino, apresentam um TGT e solicitam um tíquete ao computador. O tíquete pode ser reutilizado até que expire, mas o primeiro acesso a qualquer computador sempre requer uma viagem para o serviço de concessão de tíquete no domínio da conta do computador de destino.

O KDC de um domínio está localizado em um controlador de domínio, assim como o Active Directory para o domínio. Ambos os serviços são iniciados automaticamente pela LSA ( [*autoridade de segurança local*](../secgloss/l-gly.md) ) do controlador de domínio e são executados como parte do processo da LSA. Nenhum serviço pode ser interrompido. Se o KDC estiver indisponível para clientes de rede, o Active Directory também estará indisponível — e o controlador de domínio não estará mais controlando o domínio. O sistema garante a disponibilidade desses e de outros serviços de domínio, permitindo que cada domínio tenha vários controladores de domínio, todos os pares. Qualquer controlador de domínio pode aceitar solicitações de autenticação e solicitações de concessão de tíquete endereçadas ao KDC do domínio.

O nome [*principal de segurança*](../secgloss/s-gly.md) usado pelo KDC em qualquer domínio é "krbtgt", conforme especificado pela [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt). Uma conta para essa entidade de segurança é criada automaticamente quando um novo domínio é criado. A conta não pode ser excluída, nem o nome pode ser alterado. Um valor de senha aleatória é atribuído à conta automaticamente pelo sistema durante a criação do domínio. A senha da conta do KDC é usada para derivar uma chave de criptografia para criptografar e descriptografar o TGTs que ele emite. A senha para uma conta de confiança de domínio é usada para derivar uma chave entre territórios para a criptografia de tíquetes de referência.

Todas as instâncias do KDC em um domínio usam a conta de domínio para a entidade de segurança "krbtgt". Os clientes endereçam mensagens para o KDC de um domínio, incluindo o nome principal do serviço, "krbtgt" e o nome do domínio. Os dois itens de informações também são usados em tíquetes para identificar a autoridade emissora. Para obter informações sobre formas de nome e convenções de endereçamento, consulte [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).

 

 
