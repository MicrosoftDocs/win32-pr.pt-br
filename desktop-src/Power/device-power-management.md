---
description: A API de energia do dispositivo facilita a determinação de quais dispositivos são capazes de ativar o sistema de um estado de suspensão e quais Estados de suspensão os dispositivos dão suporte à ativação do. Para obter mais informações sobre os Estados de suspensão, consulte Estados de energia do sistema.
ms.assetid: aaa776e5-3fc2-41bd-a805-6c09ef73807b
title: Gerenciamento de energia do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0982b7de23f7b7d8cf39686c854d64f284d1ce2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921727"
---
# <a name="device-power-management"></a>Gerenciamento de energia do dispositivo

A API de energia do dispositivo facilita a determinação de quais dispositivos são capazes de ativar o sistema de um estado de suspensão e quais Estados de suspensão os dispositivos dão suporte à ativação do. Para obter mais informações sobre os Estados de suspensão, consulte [Estados de energia do sistema](system-power-states.md).

A função [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) pode ser usada para pesquisar a lista de dispositivos que correspondem aos critérios especificados. Os critérios podem incluir a capacidade do dispositivo de dar suporte a um estado do sistema ou despertar com base nesse estado. Os sinalizadores com suporte no momento podem ser encontrados em WinNT. h e DevPower. h.

A função [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) habilita ou desabilita um dispositivo especificado de ativar o sistema de um estado de suspensão.

A API de energia do dispositivo permite aos desenvolvedores criar uma melhor experiência do usuário, fornecendo ao usuário mais informações sobre o que o sistema está fazendo e mais controle sobre os dispositivos no sistema. A energia do dispositivo é útil em situações em que o consumo de energia é crítico, como em dispositivos portáteis em execução em baterias. Por exemplo, o esquema de gerenciamento de energia usado em um computador desktop pode não ser o esquema ideal para um computador laptop, de modo que o usuário talvez queira desabilitar a ativação de determinados dispositivos pelo sistema. Isso pode conservar energia porque os dispositivos desabilitados não desenharão energia enquanto o sistema estiver no modo de suspensão.

Para obter um exemplo, consulte [usando a API de energia do dispositivo](using-the-device-power-api.md).

 

 



