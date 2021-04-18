---
description: O objetivo do reconhecimento do sistema de arquivos é permitir que o sistema operacional Windows tenha uma opção adicional para um sistema de arquivos válido, mas não reconhecido, diferente de &\# 0034;&bruto \# 0034;.
ms.assetid: a5b1e97c-f22a-4d90-a3f4-1589ad9d1cc3
title: Reconhecimento do sistema de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 457d4146588ba2db2b75d06c7afac10ecb18e87c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785465"
---
# <a name="file-system-recognition"></a>Reconhecimento do sistema de arquivos

A meta do reconhecimento do sistema de arquivos é permitir que o sistema operacional Windows tenha uma opção adicional para um sistema de arquivos válido, mas não reconhecido, diferente de "RAW". Para conseguir isso, começando com o Windows 7 e o Windows Server 2008 R2, o sistema define um tipo de estrutura de dados fixo que pode ser gravado na mídia na qual uma tecnologia habilitada que altera o formato do sistema de arquivos está ativa. Essa estrutura de dados, se presente no setor de disco lógico zero, seria reconhecida pelo sistema operacional e notificaria o usuário de que a mídia contém um sistema de arquivos válido, mas não reconhecido, e não será um volume bruto se os drivers do sistema de arquivos não estiverem instalados.

## <a name="file-system-recognition-features-and-use"></a>Recursos e uso do reconhecimento do sistema de arquivos

Várias tecnologias de armazenamento recentes alteraram o formato do sistema de arquivos em disco, de modo que a mídia na qual essas tecnologias estão habilitadas se torna irreconhecível para versões anteriores do Windows devido aos drivers do sistema de arquivos não existentes quando uma versão anterior do Windows foi lançada. O comportamento padrão anterior neste cenário foi o seguinte. Quando a mídia de armazenamento não é um sistema de arquivos conhecido, ela é identificada como bruta e propagada para o Shell do Windows, em que a reprodução automática solicita a interface do usuário de formato (IU). O reconhecimento do sistema de arquivos pode resolver isso se os autores do novo sistema de arquivos gravarem corretamente a [**estrutura de dados**](file-system-recognition-structure.md) apropriada no disco.

O reconhecimento do sistema de arquivos usa os seguintes recursos e camadas no sistema operacional para atingir suas metas:

-   Mídia de armazenamento, em que uma estrutura de dados fixa reside como uma sequência de bytes organizados internamente em uma estrutura predefinida chamada estrutura de dados da [**estrutura de reconhecimento do sistema de arquivos \_ \_ \_**](file-system-recognition-structure.md) . É responsabilidade do desenvolvedor do sistema de arquivos criar essa estrutura no disco corretamente.
-   Reconhecimento do sistema de arquivos no nível do aplicativo, obtido por meio do uso do código de controle de e/s do dispositivo de [**reconhecimento de sistema de arquivos do fsctl \_ Query \_ \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition) . Para obter um exemplo de como usar esse código de controle, consulte [obtendo informações de reconhecimento do sistema de arquivos](obtaining-file-system-recognition-information.md).
-   Código de validação da soma de verificação, armazenado na estrutura de dados da [**estrutura de reconhecimento do sistema de arquivos \_ \_ \_**](file-system-recognition-structure.md) . Para obter um exemplo de como computar essa soma de verificação, consulte [calculando uma soma de verificação de reconhecimento do sistema de arquivos](computing-a-file-system-recognition-checksum.md).
-   A interface do usuário do shell do Windows usa os recursos listados anteriormente para fornecer reprodução automática mais flexível e robusta e suporte relacionado a sistemas de arquivos não reconhecidos, mas só poderá funcionar se a estrutura de dados da estrutura de reconhecimento do sistema de arquivos existir no setor de disco lógico zero. [**\_ \_ \_**](file-system-recognition-structure.md) Os desenvolvedores que implementam novos sistemas de arquivos devem utilizar esse sistema para garantir que seu sistema de arquivos não seja considerado erroneamente como sendo do tipo "RAW".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Calculando uma soma de verificação de reconhecimento do sistema de arquivos](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[Obtendo informações de reconhecimento do sistema de arquivos](obtaining-file-system-recognition-information.md)
</dt> <dt>

[Obtendo informações de volume](obtaining-volume-information.md)
</dt> </dl>

 

 
