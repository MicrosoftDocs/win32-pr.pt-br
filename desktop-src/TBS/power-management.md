---
title: Gerenciamento de energia (serviços base do TPM)
description: O TBS recebe eventos de gerenciamento de energia.
ms.assetid: 21f76bea-a313-46b7-99b3-422f17376a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e21f2c6a2292b7d49fae3b15691703fa34667a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/11/2019
ms.locfileid: "105756343"
---
# <a name="power-management-tpm-base-services"></a>Gerenciamento de energia (serviços base do TPM)

O TBS recebe eventos de gerenciamento de energia. Quando é recebida uma indicação de que o TPM ou outras partes da plataforma estão prestes a entrar em um estado de energia no qual a execução será interrompida ou o estado do TPM será perdido, o TBS verificará se o comando em execução no momento provavelmente será concluído antes de o sistema ser desligado. Em geral, o TBS permite que os comandos de duração curta e média sejam concluídos, mas cancela comandos de duração longa. Depois que o comando for retornado, o TBS interromperá o envio de novos comandos para o TPM e se preparará para hibernação. Quando a energia é restaurada, o TBS retorna o resultado do comando para o chamador e, em seguida, prossegue com o processamento de comandos TBS pendentes. O código de gerenciamento de energia TBS é executado de forma assíncrona, portanto, ele pode lidar com solicitações de gerenciamento de energia, mesmo que o TPM esteja processando um comando longo.

Quando um computador entra nos Estados de suspensão, incluindo S3 (suspensão) e S4 (hibernação), o TPM é desligado. Assim, todos os Estados de TPM não persistentes são perdidos. Antes de entrar nesses Estados, espera-se que o software de aplicativo se prepare para a perda de Estados do TPM volátil. Quando o sistema retorna de um estado de suspensão, o TBS sincroniza com o TPM para que o estado TBS seja consistente com o estado do TPM. O software de aplicativo pode precisar emitir comandos que foram interrompidos.

 

 




