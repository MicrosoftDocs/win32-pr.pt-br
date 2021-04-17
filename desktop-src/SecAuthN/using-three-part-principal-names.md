---
description: Ao criar um pacote de segurança do SSP (provedor de suporte de segurança), você não deve permitir que o cliente ingressado no domínio se autentique em um controlador de domínio usando um SPN (nome do provedor de serviços) de duas partes do formulário a seguir.
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: Usando nomes principais de três partes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8760ba740843c62c39a98e7e4683d25410a94ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754512"
---
# <a name="using-three-part-principal-names"></a>Usando nomes principais de três partes

Ao criar um pacote de segurança do SSP (provedor de suporte de segurança), você não deve permitir que o cliente ingressado no domínio se autentique em um controlador de domínio usando um SPN (nome do provedor de serviços) de duas partes do formulário a seguir.

-   <*protocolo* >/< do *nome do host*>

Um cliente sempre deve ser autenticado especificando o domínio.

-   <*protocolo* >/< do *nome* >/< do host *nome de domínio*>

Um cliente ingressado no domínio que faz logon com um SPN de duas partes pode ser capaz de representar o controlador de domínio. Se você permitir dois SPNs de parte, deverá criar uma entrada de log que contenha informações suficientes para permitir que o administrador identifique o chamador.

 

 



