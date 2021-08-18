---
title: Nomes de dispositivo
description: Nomes de dispositivo
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85183a1b23817352ba9e45e8dbb2aaa70493430cd092f357e1eaa8e9bf179d65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497266"
---
# <a name="device-names"></a>Nomes de dispositivo

Para cada tipo de dispositivo, pode haver vários drivers MCI que compartilham o conjunto de comandos, mas operam em formatos de dados diferentes. Para identificar exclusivamente um driver MCI, a MCI usa *nomes de dispositivo*.

Os nomes de dispositivo são identificados na seção mci do arquivo SYSTEM.INI ou na \[ \] parte apropriada do Registro. Essas informações identificam todos os drivers MCI a Windows. As entradas na seção \[ mci \] usam o seguinte formulário:

*nome \_ do dispositivo nome* do driver  =  *\_ filename.extension*

O exemplo a seguir mostra uma seção \[ mci \] típica SYSTEM.INI:


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



Se um driver MCI for instalado usando um nome de dispositivo que já existe no SYSTEM.INI ou no Registro, o sistema anexa um inteiro ao nome do dispositivo do novo driver, criando um nome de dispositivo exclusivo. No exemplo anterior, um driver adicional instalado usando o nome do dispositivo "cdaudio" seria atribuído ao nome do dispositivo "cdaudio1".

 

 




