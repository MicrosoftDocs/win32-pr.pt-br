---
title: Códigos de controle de e/s de dispositivo
description: Códigos de controle de e/s de dispositivo
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Windows Media Player, códigos de controle de e/s de dispositivo
- Windows Media Player, códigos de controle
- Gerenciador de Dispositivos de mídia do Windows
- códigos de controle de e/s de dispositivo
- códigos de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c00e235ce0f0e68e98f4f0e37221eac0903682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105770508"
---
# <a name="device-io-control-codes"></a>Códigos de controle de e/s de dispositivo

O Windows Media Player 10 ou posterior define códigos de controle de e/s de dispositivo do Windows Media Gerenciador de Dispositivos. A tabela a seguir contém os códigos de controle e suas descrições.



| Código de controle de e/s                      | Valor      | Descrição                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **viagem de ida e volta de metadados do WMP do IOCTL \_ \_ \_ \_** | 0x31504d57 | Gerencia a transferência de informações sobre as alterações ocorridas nos valores de metadados. Consulte [extensões de dispositivo para transferência de metadados acelerada](device-extensions-for-accelerated-metadata-transfer.md).                                                                                                                                                                          |
| **o \_ dispositivo WMP do IOCTL \_ \_ pode ser \_ sincronizado**     | 0x32504d57 | Indica se um dispositivo portátil dá suporte à sincronização automática. O Windows Media Player 10 ou posterior não fornece nenhum buffer de entrada. O buffer de saída deve retornar um valor **DWORD** . Um valor de 1 significa que o dispositivo dá suporte à sincronização. Um valor de 0 significa que o dispositivo não oferece suporte à sincronização automática.<br/> Consulte comentários para obter mais informações.<br/> |



 

## <a name="remarks"></a>Comentários

Esses códigos de controle são definidos em wmpdevices. h.

Se o dispositivo não der suporte ao **IOCTL WMP, o \_ \_ dispositivo \_ pode ser \_ sincronizado**, o Windows Media Player 10 ou posterior pressupõe que o dispositivo oferece suporte à sincronização automática. Observe que embora esse valor possa não permitir a sincronização automática, há critérios adicionais usados para determinar se o dispositivo dá suporte à sincronização automática.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Extensões de dispositivo para transferência de metadados acelerada**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 





