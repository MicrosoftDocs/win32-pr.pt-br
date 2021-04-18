---
description: Descreve um disco rígido, particionamento e o registro mestre de inicialização.
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: Partições e dispositivos de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063b943d33118a45cb6ab4c304569094af2c32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557046"
---
# <a name="disk-devices-and-partitions"></a>Partições e dispositivos de disco

Um disco rígido consiste em um conjunto de platters empilhados, cada um dos quais tem dados armazenados de forma eletromagnética em círculos concêntricos ou *faixas*. Cada platter tem dois cabeçotes, um em cada lado do platter, que lê ou grava dados conforme o disco gira. Uma *unidade de disco rígido* controla o posicionamento, a leitura e a gravação do disco rígido. Observe que os cabeçotes de todos os Platters são posicionados como uma unidade.

A menor unidade endereçável de uma faixa é um *setor*. Um *cilindro* é definido como o conjunto de faixas que aparecem no mesmo local em cada platter. Por exemplo, o diagrama a seguir mostra um disco rígido com quatro Platters. O cilindro X consiste em oito trilhas (Track X de cada lado de cada platter).

![disco rígido, incluindo faixas, setores e platters](images/diskdevice.png)

Um disco rígido pode conter uma ou mais regiões lógicas chamadas *partições*. As partições são criadas quando o usuário formata um disco rígido como um *disco básico*. O Windows também dá suporte a *discos dinâmicos*, que não são discutidos neste tópico. Para obter mais informações sobre discos básicos e discos dinâmicos, consulte [discos básicos e dinâmicos](basic-and-dynamic-disks.md).

A criação de várias partições em um disco permite a aparência de discos rígidos separados. Por exemplo, um sistema com um disco rígido que tem uma partição contém um único volume, designado pelo sistema como a unidade C. Um sistema com um disco rígido com duas partições normalmente contém as unidades C e D. Ter várias partições em um disco rígido pode facilitar o gerenciamento do sistema, por exemplo, para organizar arquivos ou dar suporte a vários usuários.

O primeiro setor físico em um disco básico contém uma estrutura de dados conhecida como MBR (registro mestre de inicialização). O MBR contém o seguinte:

-   Um programa de inicialização (até 442 bytes de tamanho)
-   Uma assinatura de disco (um número exclusivo de 4 bytes)
-   Uma tabela de partição (até quatro entradas)
-   Um marcador de fim de MBR (sempre 0x55AA)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o gerenciamento de volume](about-volume-management.md)
</dt> <dt>

[Discos básicos e dinâmicos](basic-and-dynamic-disks.md)
</dt> </dl>

 

 



