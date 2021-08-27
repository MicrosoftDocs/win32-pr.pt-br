---
description: Ao criar um pacote de segurança do SSP (provedor de suporte de segurança), você não deve permitir que o cliente ingressado no domínio se autentique em um controlador de domínio usando um SPN (nome do provedor de serviços) de duas partes do formulário a seguir.
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: Usando nomes principais de três partes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ddc9ce552e71d97c5e795b7405e97803991133a96e7b3fac3e1a81bc45d5ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915178"
---
# <a name="using-three-part-principal-names"></a>Usando nomes principais de três partes

Ao criar um pacote de segurança do SSP (provedor de suporte de segurança), você não deve permitir que o cliente ingressado no domínio se autentique em um controlador de domínio usando um SPN (nome do provedor de serviços) de duas partes do formulário a seguir.

-   <*protocolo* >/< do *nome do host*>

Um cliente sempre deve ser autenticado especificando o domínio.

-   <*protocolo* >/< do *nome* >/< do host *nome de domínio*>

Um cliente ingressado no domínio que faz logon com um SPN de duas partes pode ser capaz de representar o controlador de domínio. Se você permitir dois SPNs de parte, deverá criar uma entrada de log que contenha informações suficientes para permitir que o administrador identifique o chamador.

 

 



