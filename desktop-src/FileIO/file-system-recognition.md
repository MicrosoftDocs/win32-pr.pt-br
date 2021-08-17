---
description: o objetivo do reconhecimento do sistema de arquivos é permitir que o sistema operacional Windows tenha uma opção adicional para um sistema de arquivos válido, mas não reconhecido, diferente de &\# 0034;&bruto \# 0034;.
ms.assetid: a5b1e97c-f22a-4d90-a3f4-1589ad9d1cc3
title: Reconhecimento do sistema de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cf33e8a6e3378ad5b9f0123cb78fa228b5b780e7440a2981b10982e76d187a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996953"
---
# <a name="file-system-recognition"></a>Reconhecimento do sistema de arquivos

a meta do reconhecimento do sistema de arquivos é permitir que o sistema operacional Windows tenha uma opção adicional para um sistema de arquivos válido, mas não reconhecido, diferente de "RAW". para fazer isso, começando com Windows 7 e Windows Server 2008 R2, o sistema define um tipo de estrutura de dados fixo que pode ser gravado na mídia na qual uma tecnologia habilitada que altera o formato do sistema de arquivos está ativa. Essa estrutura de dados, se presente no setor de disco lógico zero, seria reconhecida pelo sistema operacional e notificaria o usuário de que a mídia contém um sistema de arquivos válido, mas não reconhecido, e não será um volume bruto se os drivers do sistema de arquivos não estiverem instalados.

## <a name="file-system-recognition-features-and-use"></a>Recursos e uso do reconhecimento do sistema de arquivos

várias tecnologias de armazenamento recentes alteraram o formato do sistema de arquivos em disco, de modo que a mídia na qual essas tecnologias estão habilitadas se torne irreconhecível para versões anteriores do Windows devido aos drivers do sistema de arquivos não existentes quando uma versão anterior do Windows foi liberada. O comportamento padrão anterior neste cenário foi o seguinte. quando a mídia de armazenamento não é um sistema de arquivos conhecido, ela é identificada como bruta e propagada para o Shell de Windows, em que a reprodução automática solicita a interface do usuário de formato (iu). O reconhecimento do sistema de arquivos pode resolver isso se os autores do novo sistema de arquivos gravarem corretamente a [**estrutura de dados**](file-system-recognition-structure.md) apropriada no disco.

O reconhecimento do sistema de arquivos usa os seguintes recursos e camadas no sistema operacional para atingir suas metas:

-   Armazenamento mídia, em que uma estrutura de dados fixa reside como uma sequência de bytes organizados internamente em uma estrutura predefinida chamada de estrutura de dados da [**estrutura de reconhecimento do sistema de arquivos \_ \_ \_**](file-system-recognition-structure.md) . É responsabilidade do desenvolvedor do sistema de arquivos criar essa estrutura no disco corretamente.
-   Reconhecimento do sistema de arquivos no nível do aplicativo, obtido por meio do uso do código de controle de e/s do dispositivo de [**reconhecimento de sistema de arquivos do fsctl \_ Query \_ \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition) . Para obter um exemplo de como usar esse código de controle, consulte [obtendo informações de reconhecimento do sistema de arquivos](obtaining-file-system-recognition-information.md).
-   Código de validação da soma de verificação, armazenado na estrutura de dados da [**estrutura de reconhecimento do sistema de arquivos \_ \_ \_**](file-system-recognition-structure.md) . Para obter um exemplo de como computar essa soma de verificação, consulte [calculando uma soma de verificação de reconhecimento do sistema de arquivos](computing-a-file-system-recognition-checksum.md).
-   a interface do usuário do Windows Shell usa os recursos listados anteriormente para fornecer reprodução automática mais flexível e robusta e suporte relacionado a sistemas de arquivos não reconhecidos, mas só poderá funcionar se a estrutura de dados da estrutura de reconhecimento do sistema de arquivos existir no setor de disco lógico zero. [**\_ \_ \_**](file-system-recognition-structure.md) Os desenvolvedores que implementam novos sistemas de arquivos devem utilizar esse sistema para garantir que seu sistema de arquivos não seja considerado erroneamente como sendo do tipo "RAW".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Calculando uma soma de verificação de reconhecimento do sistema de arquivos](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[Obtendo informações de reconhecimento do sistema de arquivos](obtaining-file-system-recognition-information.md)
</dt> <dt>

[Obtendo informações de volume](obtaining-volume-information.md)
</dt> </dl>

 

 
