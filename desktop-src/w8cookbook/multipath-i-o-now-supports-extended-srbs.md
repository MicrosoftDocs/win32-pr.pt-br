---
title: O Multipath I/O agora dá suporte a blocos de solicitação de armazenamento estendidos
description: O Multipath I/O agora dá suporte a blocos de solicitação de armazenamento estendidos
ms.assetid: 5373D9ED-34AF-4D66-8888-49F1EBF768F4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f558f8088b5066b51447c5f2ea23edd5154d5c10
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "104294567"
---
# <a name="multipath-io-now-supports-extended-storage-request-blocks"></a>O Multipath I/O agora dá suporte a blocos de solicitação de armazenamento estendidos

## <a name="platforms"></a>Plataformas

**Servidores** – Windows Server 2012 

## <a name="description"></a>Descrição

No Windows Server 2012, uma nova estrutura, o bloco de solicitação de armazenamento \_ \_ (SRB estendido) substitui o \_ bloco de solicitação SCSI \_ (SRB herdado) na pilha de armazenamento principal. O SRBs estendido Replica a funcionalidade do SRBs herdado, mas também é extensível e escalonável.

O Multipath I/O (MPIO) dá suporte a SRBs estendidos e permite que DSMs (módulos específicos de dispositivo) especifiquem suporte SRB estendido também. No entanto, para que uma pilha de armazenamento do dispositivo de vários caminhos use SRBs estendidos, **todos os componentes na pilha devem oferecer suporte a SRBs estendida, incluindo o DSM**. Observe que o DSM in-box da Microsoft, o MSDSm, oferece suporte ao SRBs estendido.

A \_ estrutura ex de passagem SCSI \_ \_ não faz parte da estrutura estendida de passagem do MPIO, uma vez que a passagem SCSI estendida pode ser de um tamanho variável, dependendo do CDB (depurador de linha de comando). Em vez disso, a passagem MPIO estendida tem um campo que descreve o deslocamento do início da estrutura de passagem do MPIO estendida para a estrutura de passagem do SCSI \_ \_ \_ . O chamador deve certificar-se de alocar um buffer do tamanho apropriado e definir o deslocamento do SCSI de passagem corretamente. Desde que o chamador siga as regras de passagem SCSI estendida, não deve haver nenhum trabalho extra para usar a passagem do MPIO estendida.

> [!Note]  
> Se o DSM não oferecer suporte a SRBs estendida, o MPIO falhará ao estender solicitações de passagem do MPIO que têm o sinalizador de IOCTL do MPIO \_ \_ envolvendo o sinalizador de \_ \_ DSM definido.

 

## <a name="manifestation"></a>Manifestação

Se qualquer parte da pilha de armazenamento do dispositivo, incluindo o DSM, não oferecer suporte a SRBs estendida, a pilha de armazenamento será revertida para usar o SRBs herdado.

## <a name="solution"></a>Solução

Há apenas dois requisitos de MPIO para um DSM dar suporte a \_ blocos de solicitação de armazenamento \_ :

-   O DSM deve relatar seu tipo como DsmType6
-   O DSM deve fornecer a \_ \_ \_ função com suporte de tipo de endereço do DSM

Se o DSM não relatar DsmType6 ou se reportar DsmType6, mas não fornecer a função de tipo de endereço de DSM \_ \_ \_ com suporte, o MPIO assumirá que o DSM não oferece suporte a SRBs estendidos.

A \_ \_ \_ função com suporte de tipo de endereço do DSM aceita dois parâmetros, um dos quais é um tipo de endereço. Esse tipo de endereço deve ser um dos valores de tipo de endereço de armazenamento \_ \_ \_ \* definidos em SRB. h. O DSM deve retornar TRUE se ele der suporte ao tipo de endereço fornecido e FALSE se não. A definição de "suporte" é, em última análise, o DSM. O MPIO usa essa função para garantir que o DSM não se comporte se for entregue um SRB estendido com uma \_ estrutura de endereço arma do tipo fornecido. Dessa forma, o MPIO geralmente chama essa função quando um dispositivo de vários caminhos está sendo enumerado, mas a função pode ser chamada a qualquer momento.

Se um DSM nunca tocar em um endereço arma de SRB estendido \_ , ele poderá retornar true para qualquer valor de tipo de endereço de armazenamento válido \_ \_ \_ \* . Examine o DSM de exemplo no WDK.

**Outras observações importantes**

-   DSMs que dão suporte ao SRBs estendido devem ser capazes de lidar com \_ \_ estruturas de bloco de solicitação SCSI e estruturas de bloco de solicitação de armazenamento \_ \_ . Só porque um DSM relata que dá suporte a SRBs estendida não significa que ele receberá exclusivamente SRBs estendido. Ele ainda pode receber qualquer número de SRBs herdadas, além de SRBs estendidos, e, portanto, deve ser capaz de lidar com ambos.
-   Fornecemos um arquivo de cabeçalho no WDK chamado srbhelper. h que contém funções embutidas para ajudar drivers que devem lidar com SRBs estendidos e herdados. Nosso DSM de exemplo usa esse cabeçalho para que você possa usá-lo como um exemplo de como usar essas funções.
-   Um DSM que não dá suporte a SRBs estendida nunca terá que lidar com SRBs estendidos.
-   É possível que um MPIO faça com que a pilha de armazenamento retorne no SRBs herdado no caso de o DSM não oferecer suporte a um determinado \_ tipo de endereço de armazenamento \_ \_ \* (mas, de outra forma, dá suporte a SRBs estendido).
-   "BTL8" é o único \_ tipo de endereço \_ de armazenamento \_ \* definido atualmente para o Windows Server 2012.

 

 




