---
description: Interromper um bloqueio oportunista é o processo de degradação do bloqueio que um cliente tem em um arquivo para que outro cliente possa abrir o arquivo, com ou sem um bloqueio oportunista.
ms.assetid: 0356c167-2973-4820-85a9-bc14abcbf163
title: Interrompendo bloqueios oportunistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a29b6bd36d8c000b5288ea2408897415547c802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756943"
---
# <a name="breaking-opportunistic-locks"></a>Interrompendo bloqueios oportunistas

Interromper um bloqueio oportunista é o processo de degradação do bloqueio que um cliente tem em um arquivo para que outro cliente possa abrir o arquivo, com ou sem um bloqueio oportunista. Quando o outro cliente solicita a operação de abertura, o servidor atrasa a operação de abertura e notifica o cliente que detém o bloqueio oportunista.

O cliente que mantém o bloqueio executa ações apropriadas para o tipo de bloqueio, por exemplo, abandonar buffers de leitura, fechar o arquivo e assim por diante. Somente quando o cliente que contém o bloqueio oportunista notifica o servidor de que ele está pronto, o servidor abre o arquivo para o cliente que está solicitando a operação aberta. No entanto, quando um bloqueio de nível 2 é interrompido, o servidor relata ao cliente que ele foi interrompido, mas não aguarda nenhuma confirmação, pois não há dados armazenados em cache a serem liberados para o servidor.

Ao confirmar uma interrupção de qualquer bloqueio exclusivo (filtro, nível 1 ou lote), o detentor de um bloqueio interrompido não pode solicitar outro bloqueio exclusivo. Ele pode degradar um bloqueio exclusivo para um bloqueio de nível 2 ou nenhum bloqueio. O detentor normalmente libera o bloqueio e fecha o arquivo quando está prestes a fechar o arquivo mesmo assim.

Os aplicativos são notificados de que um bloqueio oportunista é interrompido usando o membro **hEvent** da estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associada ao arquivo no qual o bloqueio é rompido. Os aplicativos também podem usar funções como [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) e [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).

 

 
