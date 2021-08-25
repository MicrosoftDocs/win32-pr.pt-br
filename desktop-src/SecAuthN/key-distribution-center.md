---
description: O centro de distribuição de chaves (KDC) é implementado como um serviço de domínio. Ele usa o Active Directory como seu banco de dados de conta e o Catálogo Global para direcionar indicações para KDCs em outros domínios.
ms.assetid: f2a7c87c-9be7-4fd8-8ecd-4edf1f2336ef
title: centro de distribuição de chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eef410ccb9289d30507708dc35000e1c15d5d4c9998b28b33a2e51d1a15b1e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013336"
---
# <a name="key-distribution-center"></a>centro de distribuição de chaves

O centro de distribuição de chaves (KDC) é implementado como um serviço de domínio. Ele usa o Active Directory como seu banco de dados de conta e o Catálogo Global para direcionar indicações para KDCs em outros domínios.

Assim como em outras implementações do [*protocolo Kerberos,*](../secgloss/k-gly.md)o KDC é um único processo que fornece dois serviços:

-   AS (Serviço de Autenticação)

    Esse serviço emite TGTs (tíquetes de concessão de tíquete) para conexão com o serviço de concessão de tíquetes em seu próprio domínio ou em qualquer domínio confiável. Antes que um cliente possa solicitar um tíquete para outro computador, ele deve solicitar um TGT do serviço de autenticação no domínio da conta do cliente. O serviço de autenticação retorna um TGT para o serviço de concessão de tíquetes no domínio do computador de destino. O TGT pode ser reutilizado até expirar, mas o primeiro acesso ao serviço de concessão de tíquetes de qualquer domínio sempre requer uma viagem ao serviço de autenticação no domínio da conta do cliente.

-   Ticket-Granting Serviço de Ticket-Granting (TGS)

    Esse serviço emite tíquetes para conexão com computadores em seu próprio domínio. Quando os clientes querem acesso a um computador, eles contatarão o serviço de concessão de tíquete no domínio do computador de destino, apresentarão um TGT e solicitarão um tíquete para o computador. O tíquete pode ser reutilizado até expirar, mas o primeiro acesso a qualquer computador sempre requer uma viagem ao serviço de concessão de tíquetes no domínio da conta do computador de destino.

O KDC para um domínio está localizado em um controlador de domínio, assim como o Active Directory para o domínio. Ambos os serviços são iniciados automaticamente pela LSA (Autoridade de Segurança [*Local)*](../secgloss/l-gly.md) do controlador de domínio e executados como parte do processo da LSA. Nenhum serviço pode ser interrompido. Se o KDC não estiver disponível para clientes de rede, o Active Directory também estará indisponível e o controlador de domínio não controlará mais o domínio. O sistema garante a disponibilidade desses e de outros serviços de domínio, permitindo que cada domínio tenha vários controladores de domínio, todos os pares. Qualquer controlador de domínio pode aceitar solicitações de autenticação e solicitações de concessão de tíquete endereçadas ao KDC do domínio.

O [*nome da entidade*](../secgloss/s-gly.md) de segurança usado pelo KDC em qualquer domínio é "krbtgt", conforme especificado pelo [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt). Uma conta para essa entidade de segurança é criada automaticamente quando um novo domínio é criado. A conta não pode ser excluída, nem o nome pode ser alterado. Um valor de senha aleatória é atribuído à conta automaticamente pelo sistema durante a criação do domínio. A senha da conta do KDC é usada para derivar uma chave de criptografia para criptografar e descriptografar os TGTs que ele emite. A senha de uma conta de confiança de domínio é usada para derivar uma chave entre realms para criptografar tíquetes de indicação.

Todas as instâncias do KDC em um domínio usam a conta de domínio para a entidade de segurança "krbtgt". Os clientes abordam mensagens para o KDC de um domínio, incluindo o nome da entidade de serviço, "krbtgt" e o nome do domínio. Ambos os itens de informações também são usados em tíquetes para identificar a autoridade de emissão. Para obter informações sobre formulários de nome e convenções de [endereçamento, consulte RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).

 

 
