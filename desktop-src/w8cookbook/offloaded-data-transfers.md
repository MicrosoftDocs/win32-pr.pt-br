---
title: Transferências de dados descarregadas
description: Transferências de dados descarregadas
ms.assetid: 91EBE6D6-2DA7-48DA-AEB7-3FAFCA8341F5
keywords:
- ODX
- descarregamento de cópia
- carregado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1057ed27347fefc7ebc6a171eb7273da4341b024
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "105788643"
---
# <a name="offloaded-data-transfers"></a>Transferências de dados descarregadas

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

Para avançar a movimentação de dados de armazenamento, a Microsoft desenvolveu uma nova tecnologia de transferência de dados – transferência de dados descarregada (ODX). Em vez de usar operações de gravação armazenadas em buffer e de leitura em buffer, o Windows ODX inicia a operação de cópia com uma leitura de descarregamento e recupera um token que representa os dados do dispositivo de armazenamento e, em seguida, usa um comando de gravação de descarregamento com o token para solicitar a movimentação de dados do disco de origem para o disco de destino. O Gerenciador de cópia dos dispositivos de armazenamento executa a movimentação de dados de acordo com o token. No Windows 8, o gerente de ti e o administrador de armazenamento podem usar o recurso ODX do Windows para interagir com o dispositivo de armazenamento para mover arquivos ou dados grandes por meio da rede de armazenamento de alta velocidade. O Windows ODX reduzirá significativamente o tráfego de rede do servidor cliente e o uso de tempo de CPU durante transferências de dados grandes, pois toda a movimentação de dados está na rede de armazenamento de back-end. O ODX pode ser usado na implantação de máquinas virtuais, na migração maciça de dados e no suporte a dispositivos de armazenamento em camadas e pode reduzir o custo da implantação de hardware físico por meio dos recursos de armazenamento de provisionamento dinâmico e ODX.

> [!Note]  
> Este recurso só funcionará em dispositivos de armazenamento com a implementação de especificação SPC4 e SBC3.

 

## <a name="functional-details"></a>Detalhes funcionais

-   O recurso ODX do Windows é inserido no mecanismo de cópia do sistema operacional Windows; durante a enumeração de armazenamento, o Windows consultará o recurso ODX do dispositivo de armazenamento
-   Copiar dispositivo de armazenamento de origem e copiar o dispositivo de armazenamento de destino deve ser gerenciado no mesmo Gerenciador de cópia para suporte de descarregamento de cópia
-   Se uma operação de descarregamento de cópia falhar, o Gerenciador de cópia do dispositivo de armazenamento deverá retornar os dados de detecção adicionais apropriados para o tratamento de erros dos aplicativos
-   O mecanismo de cópia do Windows voltará para a operação de cópia tradicional se a operação de descarregamento de cópia falhar

## <a name="using-odx"></a>Usando ODX

-   O aplicativo de transferência de dados deve garantir que o LUN de origem de cópia e o LUN de destino de cópia sejam ODX capazes antes de chamar as rotinas de API ODX
-   No Windows Explorer, os usuários podem usar "arrastar" ou "copiar e colar" para executar o descarregamento de cópia
-   Quando o LUN de origem e o LUN de destino são montados com o sistema de arquivos, o aplicativo deve chamar somente a gravação de descarregamento de FSCTL \_ \_ e leitura de \_ descarregamento de fsctl \_ para executar a transferência de dados do LUN de origem para o LUN de destino
-   Se uma operação de descarregamento de cópia falhar, o Gerenciador de cópia do dispositivo de armazenamento deverá retornar os dados de detecção adicionais apropriados para o tratamento de erros dos aplicativos
-   Quando o LUN de origem ou o LUN de destino não é montado com o sistema de arquivos e bloqueado, o aplicativo deve chamar o \_ armazenamento \_ de IOCTL gerenciar \_ \_ \_ atributos de conjunto de dados com a \_ ação DeviceDsmAction OffloadRead ou DeviceDsmAction \_ OffloadWrite para executar o descarregamento de cópia
-   Os aplicativos de gerenciamento de armazenamento podem usar \_ \_ a API de passagem SCSI para executar transferências de dados descarregadas quando os LUNs de origem e de destino não são montados com nenhum sistema de arquivos e bloqueados

## <a name="tests"></a>Testes

-   Para garantir uma experiência de usuário robusta, verifique a certificação ODX do Windows da matriz de armazenamento
-   O dispositivo de armazenamento deve estar em conformidade com os requisitos de certificação de transferência de dados descarregados do Windows (usado para ser logotipo) para dar suporte ao recurso ODX
-   Usar o kit de certificação de hardware de transferência de dados descarregados do Windows para verificar o suporte do recurso ODX dos dispositivos de armazenamento

## <a name="resources"></a>Recursos

-   Especificação T10 XCOPY Lite (11-059r8)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf)
-   [Serviços de painel de hardware](/windows-hardware/drivers/dashboard/)
-   [\_Estrutura de passagem SCSI \_](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_scsi_pass_through)

 

 