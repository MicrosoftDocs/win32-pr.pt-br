---
title: Projetando interfaces remotas
description: Com o advento do modelo de objeto de componente distribuído, é importante que sua interface personalizada seja remota, mesmo que você pretenda usá-la somente em processo.
ms.assetid: 2ee4d950-dfd5-4965-bd77-a600e878be59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3502604d62e6a5129ca3e3538761722909c0198f
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "103823537"
---
# <a name="designing-remotable-interfaces"></a>Projetando interfaces remotas

Com o advento do modelo de objeto de componente distribuído, é importante que sua interface personalizada seja remota, mesmo que você pretenda usá-la somente em processo.

MIDL é mais do que apenas uma maneira de gerar arquivos de cabeçalho para suas interfaces. É uma linguagem de programação para comunicação remota que permite que você use suas interfaces em limites de máquina, processo e thread. Isso significa que você precisa verificar o comportamento de suas interfaces definidas pelo MIDL sob essas condições antes de liberar seu programa para os clientes. Se você cometer um erro em sua IDL e a interface não for remota corretamente, poderá ser difícil corrigir esse erro. Você precisa revisar sua interface com um novo IID e deixar o antigo no para compatibilidade com versões anteriores ou você precisa converter cada cliente e cada computador do servidor em qualquer lugar ao mesmo tempo.

Mesmo que sua interface nunca seja usada fora do processo, ela pode ser usada entre threads. O pior problema para um arquivo IDL não verificado pode surgir em servidores em processo que não dão suporte a vários [Apartments de thread único](single-threaded-apartments.md)). Um servidor que não especifica um modelo de threading é implicitamente de thread único. Tudo marcado como single-thread é forçado para o thread que primeiro chamou [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Se algum outro thread fosse aquele que ativou o objeto, todas as interfaces nesse servidor de thread único devem ser remotas de volta para o thread de ativação, o que pode resultar em um retorno de REGDB \_ E \_ IIDNOTREG em resposta a uma chamada para [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))). A menos que você possa declarar absolutamente que sua interface está em processo e sempre será chamada no mesmo thread, você será remoto em algum momento.

Por fim, como um designer de interface, você precisa considerar como os aplicativos cliente usarão sua interface. Duas coisas, juntas, determinam se uma interface será eficiente entre os limites do processo e da máquina: a frequência das chamadas de método entre o limite da interface e a quantidade de dados a serem transferidos em uma determinada chamada de método. Embora o COM faça chamadas entre processos e entre redes transparentes para programas, ele não pode fazer chamadas de alta frequência e alta largura de banda eficientes em espaços de endereço. Em alguns casos, é mais apropriado criar interfaces que normalmente serão implementadas apenas como servidores em processo, enquanto outras interfaces são mais apropriadas para uso remoto.

 

 




