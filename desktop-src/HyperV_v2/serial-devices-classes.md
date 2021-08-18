---
description: Os dispositivos seriais em uma máquina virtual consistem em controladores seriais e portas seriais. Cada máquina virtual tem exatamente um controlador serial e cada controlador serial tem exatamente duas portas seriais.
ms.assetid: BA24BD74-D80C-4C5C-891F-5F17CDED2EC6
title: Classes de dispositivos seriais
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1b95a2baaf4bc3dacfddf0e18f6acd88379f958e49fc1ccbd5d6ee5cf49a11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746097"
---
# <a name="serial-devices-classes"></a>Classes de dispositivos seriais

Os dispositivos seriais em uma máquina virtual consistem em controladores seriais e portas seriais. Cada máquina virtual tem exatamente um controlador serial e cada controlador serial tem exatamente duas portas seriais.

As configurações do controlador serial não são configuráveis; portanto, não há nenhuma instância de dados de configuração associada a ela. Além disso, você não pode adicionar ou remover controladores seriais ou portas seriais de uma máquina virtual. Portanto, não há instâncias de pool de recursos para dispositivos seriais.

A seguir estão as classes WMI de virtualização relacionadas a dispositivos seriais.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                      | Descrição                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**Msvm \_ SerialController**](msvm-serialcontroller.md)<br/>                         | Representa os recursos e o gerenciamento do controlador serial.<br/> |
| [**Msvm \_ SerialPort**](msvm-serialport.md)<br/>                                     | Representa uma porta serial associada ao controlador serial.<br/>      |
| [**Msvm \_ SerialPortOnSerialController**](msvm-serialportonserialcontroller.md)<br/> | Associa uma porta serial a um controlador serial.<br/>                   |



 

 

 




