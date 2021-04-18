---
description: Os administradores podem controlar a quantidade de dados que cada usuário pode armazenar em um volume do sistema de arquivos NTFS.
ms.assetid: 42efbd5b-6455-4319-a76e-cdb666fc36b8
title: Gerenciando cotas de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5231d7683f0af40e7006193be8d5ff9390e21b65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812957"
---
# <a name="managing-disk-quotas"></a>Gerenciando cotas de disco

O sistema de arquivos NTFS dá suporte a *cotas de disco*, que permitem que os administradores controlem a quantidade de dados que cada usuário pode armazenar em um volume do sistema de arquivos NTFS. Opcionalmente, os administradores podem configurar o sistema para registrar um evento quando os usuários estão próximos de sua cota e para negar mais espaço em disco aos usuários que excederem sua cota. Os administradores também podem gerar relatórios e usar o monitor de eventos para rastrear problemas de cota.

Você pode determinar se um sistema de arquivos dá suporte a cotas de disco chamando a função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) e examinando o sinalizador de bit de **\_ \_ cotas de volume de arquivo** .

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                   | Descrição                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Administração em nível de usuário de cotas de disco](user-level-administration-of-disk-quotas.md)<br/>     | Como obter mais espaço livre em disco depois de exceder a concessão de cota.<br/>                                                                  |
| [Administração em nível de sistema de cotas de disco](system-level-administration-of-disk-quotas.md)<br/> | O administrador do sistema pode definir cotas para usuários específicos em um volume. O administrador também pode definir as cotas padrão para o volume.<br/> |
| [Limites de cota de disco](disk-quota-limits.md)<br/>                                                   | Descreve dois tipos de limites de cota de disco e como os limites de cota de disco são medidos.<br/>                                                      |
| [Interfaces de cota de disco](disk-quota-interfaces.md)<br/>                                           | Interfaces usadas com cotas de disco.<br/>                                                                                                     |



 

 

 




