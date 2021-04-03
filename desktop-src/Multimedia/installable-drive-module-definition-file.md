---
title: Arquivo de Module-Definition de unidade instalável
description: Arquivo de Module-Definition de unidade instalável
ms.assetid: d8d8d32e-18ac-47a5-a923-48b94b75e11d
keywords:
- drivers instaláveis, arquivos de definição de módulo
- drivers instaláveis, arquivos DEF
- drivers nstallable, função DriverProc
- Função DriverProc
- arquivos de definição de módulo
- arquivos DEF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700931c91bfb3c17a36a1e3a1bbc4833097b4b38
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007437"
---
# <a name="installable-drive-module-definition-file"></a>Arquivo de Module-Definition de unidade instalável

A definição de módulo (. DEF) de um driver instalável nomeia o driver, exporta a função [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) e define uma descrição do driver. O exemplo a seguir mostra um arquivo de definição de módulo típico para um driver instalável:


```C++
LIBRARY OSCI 
DESCRIPTION 'FREQ,AMPL:Oscilloscope frequency and amplitude drivers.'
EXPORTS
    DriverProc
 
```



Alguns aplicativos de instalação podem abrir o driver e recuperar a linha de descrição a ser usada ao instalar o driver. Para permanecer compatível com esses aplicativos de instalação, a linha de descrição deve ter este formulário:

  *Alias* \[ de descrição,*alias* \] ... **:* * * texto*

O *alias* especifica um nome exclusivo para o driver que os aplicativos podem usar para abrir o driver. O alias também serve como o nome do valor associado ao driver no registro. Vários aliases são separados por vírgulas. O *texto* descreve a finalidade do driver.

 

 