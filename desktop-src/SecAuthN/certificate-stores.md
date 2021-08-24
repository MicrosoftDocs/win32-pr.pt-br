---
description: Os certificados de cliente e servidor devem ser armazenados em um armazenamento de certificados acessível pelo processo do aplicativo.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Repositórios de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64451ea7f568bb5e86289d5d9f1587d98b65aa1d53c14a4a251a5e61fe72b21d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883486"
---
# <a name="certificate-stores"></a>Repositórios de certificados

Os [*certificados*](/windows/desktop/SecGloss/c-gly) de cliente e servidor devem ser [*armazenados*](/windows/desktop/SecGloss/s-gly) em um armazenamento [*de certificados acessível*](/windows/desktop/SecGloss/c-gly) pelo processo do aplicativo. Normalmente, essa é a Minha loja, também conhecida como o armazenamento pessoal. Aplicativos cliente como Internet Explorer normalmente usam a Minha loja do usuário atual enquanto servidores como Serviços de Informações da Internet (IIS) usam o sistema Minha loja do computador local.

O armazenamento raiz e o armazenamento da AC [*(autoridade*](/windows/desktop/SecGloss/c-gly) de certificação) são usados quando o Schannel ou um aplicativo cria uma cadeia de certificados a ser enviada ao computador remoto. Esses armazenamentos são usados para validar uma cadeia de certificados recebida. Para obter mais informações, consulte [Executando a autenticação usando o Schannel.](performing-authentication-using-schannel.md)

 

 
