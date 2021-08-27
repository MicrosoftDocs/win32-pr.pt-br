---
description: Deve existir uma relação de confiança entre o destinatário de uma mensagem assinada e o signatário da mensagem.
ms.assetid: 770e4674-8896-4062-a93a-a17bd30a9129
title: Verificação de confiança de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9f88d9c944de8f1c6c40e7657c463740fa94fb94a55a8b9bb0f6e33c69d81f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126816"
---
# <a name="certificate-trust-verification"></a>Verificação de confiança de certificado

Deve existir uma relação de confiança entre o destinatário de uma mensagem assinada e o signatário da mensagem. Um método de estabelecer essa confiança é por meio de um [*certificado*](../secgloss/c-gly.md), um documento eletrônico que verifica se as entidades ou as pessoas são quem afirma ser. Um certificado é emitido para uma entidade por terceiros que é confiável para ambas as partes. Portanto, cada destinatário de uma mensagem assinada decide se o emissor do certificado do signatário é confiável. O [*CryptoAPI*](../secgloss/c-gly.md) implementou uma metodologia para permitir que os desenvolvedores de aplicativos criem aplicativos que verificam automaticamente os certificados em relação a uma lista predefinida de certificados ou [*raízes*](../secgloss/r-gly.md)confiáveis. Essa lista de entidades confiáveis (chamadas de entidades) é chamada de [*lista de certificados confiáveis*](../secgloss/c-gly.md) (CTL).

O exemplo a seguir de como usar uma CTL envolve um administrador de intranet (rede intra-empresa) que deseja controlar apenas quais fontes externas são confiáveis. Nesse caso, o administrador pode criar uma lista de certificados ou raízes confiáveis, assinar e tornar a lista disponível para todos os clientes na rede na forma de uma CTL. Um aplicativo criado para usar essa funcionalidade de CryptoAPI aceitará apenas mensagens assinadas ou um software baixado que foi assinado por entidades na lista.

Para obter uma lista dessas funções, consulte [funções de verificação de certificado](cryptography-functions.md).

 

 
