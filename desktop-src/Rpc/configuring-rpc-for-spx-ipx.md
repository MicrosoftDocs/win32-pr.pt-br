---
title: Configurando o RPC para SPX/IPX
description: Ao usar os \_ transportes IPX ncacn SPX e ncadg \_ , o nome do servidor é exatamente o mesmo que o nome do servidor no Windows.
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90fa82c216413f1ea745b90ae03749ede4331310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453662"
---
# <a name="configuring-rpc-for-spxipx"></a>Configurando o RPC para SPX/IPX

Ao usar os transportes **\_ IPX** **ncacn \_ SPX** e ncadg, o nome do servidor é exatamente o mesmo que o nome do servidor no Windows. No entanto, como os nomes são distribuídos usando protocolos Novell, eles devem estar em conformidade com as convenções de nomenclatura da Novell. Se um nome de servidor não for um nome de Novell válido, os servidores não poderão criar pontos de extremidade com os transportes **\_ IPX** **ncacn \_ SPX** ou ncadg.

Um nome de servidor Novell válido contém apenas os caracteres entre 0x20 e 0x7f. Caracteres minúsculos são alterados para letras maiúsculas. Os seguintes caracteres não podem ser usados:

" \* ,./:; <=>?\[\]\\\|\]

Para manter a compatibilidade com a primeira versão do Windows NT, o **ncacn \_ SPX** e o **ncadg \_ IPX** também permitem que você use um formato especial do nome do servidor conhecido como o nome do til. O nome de til consiste em um til (~), seguido pelo número de rede de oito dígitos do servidor e seguido por seu endereço Ethernet de 12 dígitos. Os nomes de til têm uma vantagem em que eles não exigem nenhum recurso de serviço de nome. Portanto, se você estiver conectado a um servidor, o nome de til funcionará.

As tabelas a seguir contêm duas configurações de exemplo que ilustram os pontos descritos anteriormente.



| Componente                            | Configurado como      |
|--------------------------------------|--------------------|
| Windows Server                       | NWCS               |
| Windows Client                       | NWCS               |
| cliente Windows de 16 bits, cliente MS-DOS | Redirecionador do NetWare |



 

A configuração na tabela anterior requer que você tenha servidores de arquivos ou roteadores do NetWare em sua rede. Ele produzirá o melhor desempenho, pois os nomes de servidor são armazenados na ligação do NetWare.



| Componente                            | Configurado como |
|--------------------------------------|---------------|
| Windows Server                       | Agente SAP     |
| Windows Client                       | IPX/SPX       |
| cliente Windows de 16 bits, cliente MS-DOS | IPX/SPX       |



 

A segunda configuração funciona em um ambiente que não contém servidores de arquivos ou roteadores do NetWare (por exemplo, uma rede de dois computadores: um Windows Server e um cliente MS-DOS). A resolução de nomes, que é realizada durante a primeira chamada em um identificador de ligação, será um pouco mais lenta do que na primeira configuração. Além disso, a segunda configuração resulta em mais tráfego gerado pela rede.

Para implementar a resolução de nomes, quando um servidor RPC usa um ponto de extremidade SPX ou IPX, o nome do servidor e o ponto de extremidade são registrados como um servidor SAP (Service Advertising Protocol) do tipo 640 (hexadecimal). Para resolver um nome de servidor, o cliente RPC envia uma solicitação SAP para todos os serviços do mesmo tipo e, em seguida, verifica a lista de respostas para o nome do servidor. Esse processo ocorre durante a primeira chamada RPC em cada identificador de ligação. Para obter informações adicionais sobre o protocolo SAP para Novell, consulte a documentação do NetWare.

> [!Note]  
> Os aplicativos cliente do Windows de 16 bits que usam os transportes **\_ IPX** **ncacn \_ SPX** ou ncadg exigem que o arquivo Nwipxspx.dll ser instalado para ser executado no subsistema WOW. Contate a Novell para obter esse arquivo.

 

 

 




