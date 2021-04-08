---
description: Os certificados de cliente e de servidor devem ser armazenados em um repositório de certificados acessível pelo processo do aplicativo.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Repositórios de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba46318f095c78e7813ed962e066fd7e4650126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010773"
---
# <a name="certificate-stores"></a>Repositórios de certificados

Os certificados de [*cliente*](/windows/desktop/SecGloss/c-gly) e de [*servidor*](/windows/desktop/SecGloss/s-gly) devem ser armazenados em um [*repositório de certificados*](/windows/desktop/SecGloss/c-gly) acessível pelo processo do aplicativo. Normalmente, essa é a minha loja, também conhecida como o armazenamento pessoal. Aplicativos cliente, como o Internet Explorer, normalmente usam o repositório My do usuário atual, enquanto os servidores como o Serviços de Informações da Internet (IIS) usam o meu repositório do sistema do computador local.

O repositório raiz e o armazenamento de [*autoridade de certificação*](/windows/desktop/SecGloss/c-gly) (CA) são usados quando o Schannel ou um aplicativo cria uma cadeia de certificados para ser enviada ao computador remoto. Esses armazenamentos são usados para validar uma cadeia de certificados recebida. Para obter mais informações, consulte [executando a autenticação usando Schannel](performing-authentication-using-schannel.md).

 

 
