---
title: Multipath I/O agora dá suporte a blocos de solicitação de armazenamento estendido
description: Multipath I/O agora dá suporte a blocos de solicitação de armazenamento estendido
ms.assetid: 5373D9ED-34AF-4D66-8888-49F1EBF768F4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b3a5ce3050bf7fddc2bd77da30e766c7b9cd67a8c4f49c753da5302b104c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932206"
---
# <a name="multipath-io-now-supports-extended-storage-request-blocks"></a>Multipath I/O agora dá suporte a blocos de solicitação de armazenamento estendido

## <a name="platforms"></a>Plataformas

**Servidores** – Windows Server 2012 

## <a name="description"></a>Descrição

No Windows Server 2012, uma nova estrutura, o BLOCO DE SOLICITAÇÃO DE ARMAZENAMENTO (SRB estendido) substitui o BLOCO DE SOLICITAÇÃO \_ \_ SCSI \_ (SRB herdada) na pilha de armazenamento \_ principal. Os SRBs estendidos replicam a funcionalidade dos SRBs herdáveis, mas também são extensíveis e escalonáveis.

Multipath I/O (MPIO) dá suporte a SRBs estendidos e permite que DSMs (Módulos Específicos do Dispositivo) especifiquem também o suporte estendido a SRB. No entanto, para que a pilha de armazenamento de um dispositivo multicaminho use SRBs estendidos, todos os componentes na pilha devem dar suporte a SRBs estendidos, incluindo **o DSM**. Observe que o DSM in-box da Microsoft, MSDSM, dá suporte a SRBs estendidos.

A estrutura SCSI PASS THROUGH EX não faz parte da estrutura de passagem do MPIO estendida, pois a passagem SCSI estendida pode ser de um tamanho variável, dependendo do \_ \_ CDB (depurador de linha \_ de comando). Em vez disso, a passagem mpIO estendida tem um campo que descreve o deslocamento do início da estrutura de passagem do MPIO estendido para a estrutura SCSI \_ PASS \_ THROUGH \_ EX. O chamador deve certificar-se de alocar um buffer do tamanho apropriado e definir o deslocamento de passagem SCSI corretamente. Desde que o chamador siga as regras para passões SCSI estendidas, não deve haver nenhum trabalho extra para que ele use a passagem estendida do MPIO.

> [!Note]  
> Se o DSM não dá suporte a SRBs estendidos, o MPIO falhará nas solicitações de passagem estendidas do MPIO que têm o sinalizador MPIO \_ IOCTL \_ \_ INVOLVE \_ DSM definido.

 

## <a name="manifestation"></a>Manifestação

Se qualquer parte da pilha de armazenamento do dispositivo, incluindo o DSM, não dá suporte a SRBs estendidos, a pilha de armazenamento será revertida para o uso de SRBs herdado.

## <a name="solution"></a>Solução

Há apenas dois requisitos de MPIO para um DSM dar suporte a BLOCOS DE \_ SOLICITAÇÃO \_ DE ARMAZENAMENTO:

-   O DSM deve relatar seu tipo como DsmType6
-   O DSM deve fornecer a função COM SUPORTE DO TIPO DE ENDEREÇO DSM \_ \_ \_

Se o DSM não relatar DsmType6 ou se ele relatar DsmType6, mas não fornecer a função DSM ADDRESS TYPE SUPPORTED, o MPIO assumirá que o DSM não dá suporte a \_ \_ SRBs \_ estendidos.

A função DSM \_ ADDRESS \_ TYPE \_ SUPPORTED aceita dois parâmetros, um dos quais é um tipo de endereço. Esse tipo de endereço deve ser um dos valores DE \_ TIPO DE ENDEREÇO DE ARMAZENAMENTO \_ \_ \* definidos em srb.h. O DSM deverá retornar TRUE se ele for compatível com o tipo de endereço determinado e FALSE se não o fizer. A definição de "suporte" é, em última análise, até o DSM. O MPIO usa essa função para garantir que o DSM não se comportará inde forma se receber um SRB estendido com uma estrutura STOR \_ ADDRESS do tipo determinado. Assim, o MPIO geralmente chama essa função quando um dispositivo multicaminho está sendo enumerado, mas a função pode ser chamada a qualquer momento.

Se um DSM nunca tocar no ENDEREÇO STOR de um SRB estendido, ele poderá retornar TRUE para qualquer \_ valor válido de TIPO DE ENDEREÇO DE \_ \_ \_ \* ARMAZENAMENTO. Revise o DSM de exemplo no WDK.

**Outras observações importantes**

-   Os DSMs que suportam SRBs estendidos devem ser capazes de lidar com estruturas SCSI REQUEST BLOCK e \_ \_ estruturas STORAGE \_ REQUEST \_ BLOCK. Apenas porque um DSM informa que ele dá suporte a SRBs estendidos não significa que ele receberá exclusivamente SRBs estendidos. Ele ainda pode receber qualquer número de SRBs herdados além de SRBs estendidos e, portanto, deve ser capaz de lidar com ambos.
-   Fornecemos um arquivo de título no WDK chamado srbhelper.h que contém funções em linha para ajudar os drivers que devem lidar com SRBs estendidos e herdados. Nosso DSM de exemplo usa esse header para que você possa usá-lo como um exemplo de como usar essas funções.
-   Um DSM que não dá suporte a SRBs estendidos nunca terá que lidar com SRBs estendidos.
-   É possível que um MPIO faça com que a pilha de armazenamento faça fall-back em SRBs herdado caso o DSM não seja compatível com um determinado TIPO de ENDEREÇO DE ARMAZENAMENTO (mas, caso contrário, dá suporte a \_ \_ \_ \* SRBs estendidos).
-   "BTL8" é o único TIPO \_ DE ENDEREÇO DE ARMAZENAMENTO atualmente definido para \_ \_ \* Windows Server 2012.

 

 




