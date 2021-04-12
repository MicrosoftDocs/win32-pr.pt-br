---
title: Glossário de acesso ao dispositivo
description: Veja a seguir os termos usados em toda a documentação da API de acesso ao dispositivo.
Robots: noindex, nofollow
ms.assetid: A6311538-D7CC-4A23-A145-14AF3BBFC4C4
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 8406c41a2666f9014bac27452572c6f88b84e6bf
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365513"
---
# <a name="device-access-glossary"></a>Glossário de acesso ao dispositivo

Veja a seguir os termos usados em toda a documentação da API de acesso ao dispositivo.

<dl> <dt>

**Contêiner**
</dt> <dd>

Um ambiente de execução altamente restrito no qual um processo é executado com um subconjunto reduzido dos privilégios do usuário. Um processo em execução em um AppContainer é chamado de processo de AppContainer. Um processo do AppContainer é isolado de outros processos do AppContainer e do perfil do usuário. Ele tem acesso limitado a um subconjunto muito pequeno de recursos do sistema, como arquivos, dispositivos, chaves do registro, pontos de extremidade de RPC (chamada de procedimento) e recursos de rede de IPC (comunicação entre processos).

</dd> <dt>

**Associação**
</dt> <dd>

Associar um objeto de acesso de dispositivo a uma interface de dispositivo específica. Se a associação for bem-sucedida, os aplicativos da Windows Store poderão usar o objeto de acesso ao dispositivo como um agente para se comunicar com o driver de dispositivo.

</dd> <dt>

**Agente**
</dt> <dd>

Um componente que fornece acesso a um recurso que não é concedido por padrão.

</dd> <dt>

**Aplicativo privilegiado**
</dt> <dd>

Um aplicativo que é identificado em metadados de um dispositivo específico como associado a esse dispositivo, para que ele possa se comunicar com a interface restrita do driver de dispositivo. Um exemplo desse aplicativo pode ser um aplicativo de reprodução de música proprietário que tem permissão exclusiva para sincronizar com um player portátil de música, quando os aplicativos de concorrentes não podem. Para obter mais informações sobre como definir os metadados de um dispositivo ou como restringir um driver a aplicativos com privilégios, consulte [aplicativos de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).

</dd> </dl>
