---
title: Configurando o RPC para SPX/IPX
description: Ao usar os transportes ncacn spx e \_ ncadg ipx, o nome do servidor é exatamente o mesmo que o nome do servidor no \_ Windows.
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5557541b296c436f2c3c1de007eb0e331e1c77d0529be83e758a25b76ac5e55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022446"
---
# <a name="configuring-rpc-for-spxipx"></a>Configurando o RPC para SPX/IPX

Ao usar os **transportes ncacn \_ spx** e **ncadg \_ ipx,** o nome do servidor é exatamente o mesmo que o nome do servidor no Windows. No entanto, como os nomes são distribuídos usando protocolos Novell, eles devem estar em conformidade com as convenções de nomenu da Novell. Se um nome de servidor não for um nome Válido da Novell, os servidores não poderão criar pontos de extremidade com os transportes **ncacn \_ spx** ou **ncadg \_ ipx.**

Um nome válido do servidor Novell contém apenas os caracteres entre 0x20 e 0x7f. Os caracteres minúsculos são alterados para maiúsculas. Os seguintes caracteres não podem ser usados:

" \* ,./:;<=>?\[\]\\\|\]

Para manter a compatibilidade com a primeira versão do Windows NT, **o ncacn \_ spx** e **o ncadg \_ ipx** também permitem que você use um formato especial do nome do servidor conhecido como o nome do til. O nome do til consiste em um til (~), seguido pelo número de rede de oito dígitos do servidor e seguido pelo endereço Ethernet de 12 dígitos. Os nomes de til têm uma vantagem de que eles não exigem recursos de serviço de nome. Portanto, se você estiver conectado a um servidor, o nome do til funcionará.

As tabelas a seguir contêm duas configurações de exemplo que ilustram os pontos descritos anteriormente.



| Componente                            | Configurado como      |
|--------------------------------------|--------------------|
| Windows Server                       | NWCS               |
| Windows Client                       | NWCS               |
| Cliente de 16 Windows, cliente MS-DOS | Redirecionador do NetWare |



 

A configuração na tabela anterior requer que você tenha roteadores ou servidores de arquivos do NetWare em sua rede. Ele produzirá o melhor desempenho porque os nomes de servidor são armazenados no NetWare Bindery.



| Componente                            | Configurado como |
|--------------------------------------|---------------|
| Windows Server                       | Agente SAP     |
| Windows Client                       | IPX/SPX       |
| Cliente de 16 Windows, cliente MS-DOS | IPX/SPX       |



 

A segunda configuração funciona em um ambiente que não contém roteadores ou servidores de arquivos NetWare (por exemplo, uma rede de dois computadores: um servidor Windows e um cliente MS-DOS). A resolução de nomes, que é realizada durante a primeira chamada sobre um alça de associação, será um pouco mais lenta do que na primeira configuração. Além disso, a segunda configuração resulta em mais tráfego gerado pela rede.

Para implementar a resolução de nomes, quando um servidor RPC usa um ponto de extremidade SPX ou IPX, o nome do servidor e o ponto de extremidade são registrados como um servidor SAP do tipo 640 (hexadecimal). Para resolver um nome de servidor, o cliente RPC envia uma solicitação SAP para todos os serviços do mesmo tipo e, em seguida, examina a lista de respostas para o nome do servidor. Esse processo ocorre durante a primeira chamada RPC sobre cada alça de associação. Para obter informações adicionais sobre o protocolo SAP para Novell, consulte a documentação do NetWare.

> [!Note]  
> Os aplicativos cliente Windows de 16 bits que usam os transportes **ncacn \_ spx** ou **ncadg \_ ipx** exigem que o arquivo Nwipxspx.dll seja instalado para ser executado no subsistema WOW. Contate a Novell para obter esse arquivo.

 

 

 




