---
description: A correlação afeta o conjunto de classes retornadas do SMIR.
ms.assetid: 799a0866-e7a0-492f-956e-b13bf591babe
ms.tgt_platform: multiple
title: Correlação de classes SNMP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc0ca4740c90563fce05e1b6352ef33b0e3ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165319"
---
# <a name="wmi-snmp-class-correlation"></a>Correlação de classes SNMP WMI

A correlação afeta o conjunto de classes retornadas do SMIR. As classes correlacionadas são aquelas em que um determinado dispositivo SNMP é conhecido por dar suporte no momento em que a enumeração ocorre. A enumeração não correlacionada retorna todas as classes presentes no SMIR, independentemente de o dispositivo dar suporte a elas. A correlação é um recurso do provedor SNMP WMI e pode ser desativada ou ativada (padrão).

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

A correlação pode impedi-lo de ver todas as classes que são realmente suportadas por um dispositivo. Se você souber que uma classe específica tem suporte, mas ela não aparece no SMIR, isso pode ser devido a vários motivos, um dos quais é a correlação. Considere a possibilidade de desativar a correlação antes de gravar no dispositivo em questão. No entanto, a desativação da correlação resulta na probabilidade de que muitas classes sem suporte do dispositivo apareçam no SMIR. Além disso, há um custo de desempenho no uso da correlação porque o dispositivo é consultado para ver quais classes ele suporta. Quando a correlação é ativada, o provedor SNMP causa uma enumeração de classes com suporte a dispositivos semelhantes ao resultado da execução de uma ferramenta de *passagem MIB* .

Por exemplo, um Gerenciador de rede quer saber várias partes importantes de dados sobre todos os hubs gerenciados em uma rede específica. Já existe um banco de dados dos dispositivos atuais e seus MIBs com suporte. portanto, não há necessidade de contar com a função de correlação do dispositivo para fornecer os elementos de dados com suporte. Nesse caso, a correlação pode ser desativada.

O exemplo a seguir mostra como desativar a correlação.


```VB
set objNamedValueSet = CreateObject( _
    "WbemScripting.SWbemNamedValueSet") 
objNamedValueSet.Add "Correlate", FALSE, 0
```



Por outro lado, outro gerenciador de rede pode querer monitorar todas as unidades de disco de máquina UNIX na rede, mas não está familiarizado com os dados da MIB nesses computadores. Nesse caso, a correlação seria ativada.

 

 



