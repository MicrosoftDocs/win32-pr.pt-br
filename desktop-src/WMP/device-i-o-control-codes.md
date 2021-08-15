---
title: Códigos de controle de E/S do dispositivo
description: Códigos de controle de E/S do dispositivo
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Windows Media Player,códigos de controle de E/S do dispositivo
- Windows Media Player, códigos de controle
- Windows Mídia Gerenciador de Dispositivos
- códigos de controle de E/S do dispositivo
- códigos de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d610b396125cf190764b53106ca6535a214e2c8166f4e69de884c113fd77ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935845"
---
# <a name="device-io-control-codes"></a>Códigos de controle de E/S do dispositivo

Windows Media Player 10 ou posterior define Windows de controle Gerenciador de Dispositivos de E/S do dispositivo. A tabela a seguir contém os códigos de controle e suas descrições.



| Código de controle de E/S                      | Valor      | Descrição                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IOCTL \_ WMP \_ METADATA \_ ROUND \_ TRIP** | 0x31504d57 | Gerencia a transferência de informações sobre alterações que ocorreram em valores de metadados. Consulte [Extensões de dispositivo para transferência de metadados acelerada.](device-extensions-for-accelerated-metadata-transfer.md)                                                                                                                                                                          |
| **O DISPOSITIVO WMP IOCTL \_ \_ PODE SER \_ \_ SINCRONIZADO**     | 0x32504d57 | Indica se um dispositivo portátil dá suporte à sincronização automática. Windows Media Player 10 ou posterior não fornece nenhum buffer de entrada. O buffer de saída deve retornar um **valor DWORD.** Um valor de 1 significa que o dispositivo dá suporte à sincronização. Um valor de 0 significa que o dispositivo não dá suporte à sincronização automática.<br/> Consulte Comentários para obter mais informações.<br/> |



 

## <a name="remarks"></a>Comentários

Esses códigos de controle são definidos em wmpdevices.h.

Se o dispositivo não for compatível **com IOCTL \_ WMP \_ DEVICE CAN \_ \_ SYNC**, o Windows Media Player 10 ou posterior assumirá que o dispositivo dá suporte à sincronização automática. Observe que, embora esse valor possa não permitir a sincronização automática, há critérios adicionais usados para determinar se o dispositivo dá suporte à sincronização automática.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Extensões de dispositivo para transferência de metadados aceleradas**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 





