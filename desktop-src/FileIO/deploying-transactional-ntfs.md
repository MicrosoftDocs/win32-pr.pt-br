---
description: Controle de cache em NTFS Transacional.
ms.assetid: 0fd272ee-cf5f-4ba9-b8aa-ff0016f51d4b
title: Implantando o NTFS Transacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7c44e0ad3b83854e56d18171072a7cb4615d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921336"
---
# <a name="deploying-transactional-ntfs"></a>Implantando o NTFS Transacional

O NTFS Transacional (TxF), como a maioria dos mecanismos de transação, depende da ordenação correta de gravações de dados. Garantir a ordenação adequada de gravação requer um controle explícito do cache de dados. Para atender a esse requisito, o TxF requer que as unidades de disco implementem os mecanismos de controle de cache que fazem parte das interfaces de unidade padronizadas, como SCSI, SATA e ATA.

O mecanismo de controle de cache usado pelo TxF é um sinalizador conhecido como a função de acesso à unidade de força (FUA). Esse sinalizador especifica que a unidade deve gravar os dados no armazenamento de mídia estável antes da conclusão da sinalização. Em certos pontos críticos em uma transação, o TxF precisa emitir um FUA para garantir que alguns dados de controle necessários para reverter com êxito uma transação não sejam perdidos se ocorrer uma falha de energia.

As unidades de disco de classe de servidor (SCSI e Fiber Channel) geralmente dão suporte ao sinalizador FUA. A partir do vista, o Windows dá suporte ao sinalizador FUA somente para discos de canal de fibra e SCSI.

Em unidades de mercadoria (ATA/SATA/USB), o TxF tem períodos de vulnerabilidade durante os quais uma falha de energia de unidade pode fazer com que o TxF não consiga reverter corretamente a transação, deixando dados em um estado inconsistente, a menos que o cache de gravação da unidade esteja desabilitado.

Alguns adaptadores de barramento de host (HBAs) e controladores de armazenamento (por exemplo, sistemas RAID) têm caches com suporte de bateria interna. Como esses dispositivos preservam os dados armazenados em cache se ocorrer uma falha de energia, os discos conectados a eles não serão necessários para honrar o sinalizador FUA. Além disso, um disco cuja fonte de alimentação é protegida por uma fonte de alimentação ininterrupta (UPS) não precisa respeitar o sinalizador FUA. Isso ocorre porque o no-break manterá a energia longa o suficiente para que o disco libere seu cache para a mídia.

Desabilitar o cache de gravação de uma unidade elimina o requisito para que a unidade obedeça o sinalizador FUA. Você pode desabilitar o cache de gravação de um disco emitindo o código de controle de informações do cache do conjunto de discos do IOCTL para o disco. [**\_ \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_set_cache_information) O estado do cache de gravação (ligar/desligar) será preservado entre reinicializações do sistema. A emissão desse código de controle terá consequências de desempenho muito significativas para todas as e/s emitidas para esse disco, o que provavelmente será uma degradação de desempenho perceptível. O uso desse código de controle deve ser cuidadosamente considerado antes da implantação.

> [!Note]  
> Para que o TxF seja capaz de proteger consistentemente a integridade dos dados por meio de falhas de energia, o sistema deve atender a pelo menos um dos seguintes critérios:
>
> -   Usar discos de classe de servidor (SCSI, Fiber Channel).
> -   Verifique se os discos estão conectados a um HBA de cache com suporte de bateria.
> -   Use um controlador de armazenamento (por exemplo, o sistema RAID) como o dispositivo de armazenamento.
> -   Verifique se a energia do disco está protegida por um UPS.
> -   Verifique se o recurso de cache de gravação do disco está desabilitado.

 

 

 



