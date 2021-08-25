---
description: Você não pode usar as funções de backup e restauração do Certadm.dll para fazer backup das chaves privadas dos serviços de certificados.
ms.assetid: 27ee8caa-8f5e-46dc-b55d-afde5471507e
title: Fazendo backup e restaurando a chave privada dos serviços de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65b8c25e627e516d92b8dc8219db9c7933bd8d9902b1f75bea204d723edd61f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879776"
---
# <a name="backing-up-and-restoring-the-certificate-services-private-key"></a>Fazendo backup e restaurando a chave privada dos serviços de certificados

Você não pode usar as funções de backup e restauração do Certadm.dll para fazer backup das [*chaves privadas*](../secgloss/p-gly.md)dos serviços de certificados. Não é possível fazer backup das chaves privadas por essas funções porque essas funções têm o objetivo de fazer backup e restaurar o banco de dados de serviços de certificados (e arquivos relacionados) e esse banco de dados não contém nenhuma chave privada (mesmo para certificados emitidos automaticamente).

Para fazer backup de uma chave privada dos serviços de certificados, use o snap-in do MMC da autoridade de certificação ou o comando certutil (com-backup ou-BackupKey especificado). Fazer backup da chave privada com o snap-in MMC da autoridade de certificação ou certutil resulta na gravação da chave privada no \# arquivo PKCS 12. Embora esse arquivo PKCS \# 12 seja protegido por senha, ele deve ser considerado extremamente confidencial e deve ser armazenado com segurança; a senha para o arquivo PKCS \# 12 também deve ser protegida contra pessoas não autorizadas.

Da mesma forma, as chaves privadas não podem ser restauradas pelas funções de backup e restauração dos serviços de certificados. Uma chave de backup dos serviços de certificados contida em um \# arquivo PKCS 12 pode ser restaurada pelo snap-in do MMC da autoridade de certificação ou pelo comando certutil (especificando os verbos-Restore ou-restorekey); Observe que a pessoa que executa a operação de restauração precisará saber a senha do \# arquivo PKCS 12.

Há apenas dois casos em que é necessário fazer backup de uma chave privada dos serviços de certificados. O primeiro caso é após a instalação dos serviços de certificados. O segundo caso é após qualquer operação de renovação do certificado de serviços de certificados.

 

 
