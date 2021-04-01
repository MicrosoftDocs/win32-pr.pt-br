---
description: O BIOS virtual é uma imagem de software que é carregada na RAM para configurar alguns dos aspectos básicos do e a inicialização de um sistema de computador. Há um elemento BIOS por sistema de computador e esse elemento não pode ser substituído ou removido.
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: Classes do BIOS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e725910bbeb1032f876b5e4fcf08da4a6ea60bc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921785"
---
# <a name="bios-classes"></a>Classes do BIOS

O BIOS virtual é uma imagem de software que é carregada na RAM para configurar alguns dos aspectos básicos do e a inicialização de um sistema de computador. Há um elemento BIOS por sistema de computador e esse elemento não pode ser substituído ou removido. Portanto, não há nenhum pool de recursos para adicionar novos elementos BIOS à máquina virtual. O elemento BIOS também não tem sua própria classe SettingData para descrever as configurações do BIOS. As configurações do BIOS, como números de série, ordem de inicialização e estado de bloqueio num, são encontradas na classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) .

Veja a seguir as classes WMI de virtualização relacionadas ao BIOS. Essas classes estão no \\ \\ . \\ \\Namespace de virtualização de raiz.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                    | Descrição                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**\_Bioselement Msvm**](msvm-bioselement.md)<br/> | Representa o software de nível baixo que é carregado na RAM para configurar e iniciar o sistema.<br/> |
| [**Msvm \_ SystemBIOS**](msvm-systembios.md)<br/>   | Usado para associar uma máquina virtual a seu BIOS.<br/>                                           |



 

 

 




