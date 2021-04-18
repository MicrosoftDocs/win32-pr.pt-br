---
description: Os dispositivos seriais em uma máquina virtual consistem em controladores seriais e portas seriais. Cada máquina virtual tem exatamente um controlador serial e cada controlador serial tem exatamente duas portas seriais.
ms.assetid: BA24BD74-D80C-4C5C-891F-5F17CDED2EC6
title: Classes de dispositivos seriais
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ae796b86837372d60bba83e51e0190b9c7d3f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785445"
---
# <a name="serial-devices-classes"></a>Classes de dispositivos seriais

Os dispositivos seriais em uma máquina virtual consistem em controladores seriais e portas seriais. Cada máquina virtual tem exatamente um controlador serial e cada controlador serial tem exatamente duas portas seriais.

As configurações para o controlador serial não são configuráveis; Portanto, não há nenhuma instância de dados de configuração associada a ela. Além disso, você não pode adicionar ou remover controladores seriais ou portas seriais de uma máquina virtual. Portanto, não há nenhuma instância do pool de recursos para dispositivos seriais.

Veja a seguir as classes WMI de virtualização relacionadas a dispositivos seriais.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                      | Descrição                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**Msvm \_ SerialController**](msvm-serialcontroller.md)<br/>                         | Representa os recursos e o gerenciamento do controlador serial.<br/> |
| [**\_SerialPort Msvm**](msvm-serialport.md)<br/>                                     | Representa uma porta serial associada ao controlador serial.<br/>      |
| [**Msvm \_ SerialPortOnSerialController**](msvm-serialportonserialcontroller.md)<br/> | Associa uma porta serial a um controlador serial.<br/>                   |



 

 

 




