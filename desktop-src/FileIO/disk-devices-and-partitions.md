---
description: Descreve um disco rígido, particionamento e o Registro mestre de inicialização.
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: Dispositivos de disco e partições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758454c9fc9e684e918646bf99869c7544b3b02c0201eb2ba507f8ffbdc303d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015365"
---
# <a name="disk-devices-and-partitions"></a>Dispositivos de disco e partições

Um disco rígido consiste em um conjunto de bandejas empilhadas, cada uma delas com dados armazenados de forma estaticamente em círculos concêntricos ou *rastreia*. Cada placa tem duas caras, uma em cada lado da placa, que lê ou grava dados conforme o disco gira. Uma *unidade de disco* rígido controla o posicionamento, a leitura e a escrita do disco rígido. Observe que os cabeceamentos de todos os discos são posicionados como uma unidade.

A menor unidade que pode ser abordada de uma faixa é um *setor*. Um *cilindro* é definido como o conjunto de faixas que aparecem no mesmo local em cada placa. Por exemplo, o diagrama a seguir mostra um disco rígido com quatro bandejas. O cilindro X consiste em oito faixas (faixa X de cada lado de cada placa).

![disco rígido, incluindo faixas, setores e bandejas](images/diskdevice.png)

Um disco rígido pode conter uma ou mais regiões lógicas chamadas *partições*. As partições são criadas quando o usuário formatada um disco rígido como um *disco básico.* Windows também dá suporte *a discos dinâmicos*, que não são discutidos neste tópico. Para obter mais informações sobre discos básicos e discos dinâmicos, consulte [Basic e Dynamic Disks](basic-and-dynamic-disks.md).

A criação de várias partições em um disco permite a aparência de ter discos rígidos separados. Por exemplo, um sistema com um disco rígido que tem uma partição contém um único volume, designado pelo sistema como unidade C. Um sistema com um disco rígido com duas partições normalmente contém as unidades C e D. Ter várias partições em um disco rígido pode facilitar o gerenciamento do sistema, por exemplo, organizar arquivos ou dar suporte a vários usuários.

O primeiro setor físico em um disco básico contém uma estrutura de dados conhecida como MBR (Registro mestre de inicialização). O MBR contém o seguinte:

-   Um programa de inicialização (até 442 bytes de tamanho)
-   Uma assinatura de disco (um número de 4 byte exclusivo)
-   Uma tabela de partição (até quatro entradas)
-   Um marcador de fim de MBR (sempre 0x55AA)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Gerenciamento de Volume](about-volume-management.md)
</dt> <dt>

[Discos básicos e dinâmicos](basic-and-dynamic-disks.md)
</dt> </dl>

 

 



