---
title: Desenvolvendo aplicativos de Windows RPC
description: Quando você instala o SDK (Kit de Desenvolvimento de Software de Plataforma), o ambiente de desenvolvimento RPC a seguir, as bibliotecas em tempo de run time e as ferramentas são instalados automaticamente
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ddb48a38faadb8235064fa735fa8a75a80a62308990373ab1971d4a6cd9ecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930791"
---
# <a name="developing-rpc-windows-applications"></a>Desenvolvendo aplicativos de Windows RPC

Quando você instala o SDK (Kit de Desenvolvimento de Software de Plataforma), o seguinte ambiente de desenvolvimento RPC, as bibliotecas em tempo de run time e as ferramentas são instalados automaticamente:

-   Header da linguagem C/C++ (. H) arquivos
-   Arquivos de bibliotecas de importação RPC (.lib)
-   Programas de exemplo
-   Arquivos de Ajuda de referência RPC
-   O **utilitário uuidgen**

Quando você instala Windows, o seguinte é instalado:

-   DLLs de tempo de executar RPC
-   Microsoft Locator (sem suporte no Windows Vista e posterior)
-   Serviços de mapeamento de ponto de extremidade RPC

As bibliotecas de importação RPC a seguir.



| Biblioteca de importação | Description                |
|----------------|----------------------------|
| Rpcns4.lib     | Funções de serviço de nome     |
| Rpcrt4.lib     | Windows funções em tempo de run time |



 

> [!Note]  
> Rpcns4.lib está obsoleto e não tem mais suporte.

 

As bibliotecas RPC a seguir são incluídas para suporte de nível inferior.



| Biblioteca de vínculo dinâmico | Descrição                 | Plataforma                           |
|----------------------|-----------------------------|------------------------------------|
| Rpcltc1.dll          | Transporte de pipe nomeado do cliente | Windows NT, Windows 98, Windows 95 |
| Rpclts1.dll          | Transporte de pipe nomeado do servidor | Windows NT, Windows 98, Windows 95 |
| Rpcltc3.dll          | Transporte TCP/IP do cliente     | Windows NT, Windows 98, Windows 95 |
| Rpclts3.dll          | Transporte TCP/IP do servidor     | Windows NT, Windows 98, Windows 95 |
| Rpcltc5.dll          | Transporte NetBIOS do cliente    | Windows NT, Windows 98, Windows 95 |
| Rpclts5.dll          | Transporte netBIOS do servidor    | Windows NT, Windows 98, Windows 95 |
| Rpcltc6.dll          | Transporte SPX do cliente        | Windows NT, Windows 98, Windows 95 |
| Rpclts6.dll          | Transporte SPX do servidor        | Windows NT, Windows 98, Windows 95 |
| Rpcdgc6.dll          | Transporte IPX do cliente        | Windows NT                         |
| Rpcdgs6.dll          | Transporte IPX do servidor        | Windows NT                         |
| Rpcdgc3.dll          | Transporte UDP do cliente        | Windows NT                         |
| Rpcdgs3.dll          | Transporte UDP do servidor        | Windows NT                         |



 

Você também precisará do compilador linguagem IDL da Microsoft (MIDL). Para obter mais informações, [consulte Usando o compilador MIDL](/windows/desktop/Midl/using-the-midl-compiler-2).

 

 