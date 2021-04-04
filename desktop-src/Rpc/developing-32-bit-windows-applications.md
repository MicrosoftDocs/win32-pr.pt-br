---
title: Desenvolvendo aplicativos RPC do Windows
description: Quando você instala o SDK (Software Development Kit) da plataforma, o seguinte ambiente de desenvolvimento RPC, as bibliotecas de tempo de execução e as ferramentas são instaladas automaticamente
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b418358649d0cf7205b9a3bde236cf66d3ce81e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008055"
---
# <a name="developing-rpc-windows-applications"></a>Desenvolvendo aplicativos RPC do Windows

Quando você instala o SDK (Software Development Kit) da plataforma, o seguinte ambiente de desenvolvimento RPC, as bibliotecas de tempo de execução e as ferramentas são instaladas automaticamente:

-   Cabeçalho da linguagem C/C++ (. H) arquivos
-   Arquivos de bibliotecas de importação RPC (. lib)
-   Programas de exemplo
-   Arquivos de ajuda de referência RPC
-   O utilitário **Uuidgen**

Quando você instala o Windows, os seguintes itens são instalados:

-   DLLs de tempo de execução RPC
-   Microsoft Locator (sem suporte no Windows Vista e posterior)
-   Ponto de extremidade RPC-serviços de mapeamento

As seguintes bibliotecas de importação RPC.



| Biblioteca de importação | Descrição                |
|----------------|----------------------------|
| Rpcns4. lib     | Funções de nome-serviço     |
| Rpcrt4. lib     | Funções de tempo de execução do Windows |



 

> [!Note]  
> Rpcns4. lib está obsoleto e não tem mais suporte.

 

As bibliotecas RPC a seguir estão incluídas para o suporte de nível inferior.



| Biblioteca de vínculo dinâmico | Descrição                 | Plataforma                           |
|----------------------|-----------------------------|------------------------------------|
| Rpcltc1.dll          | Transporte de pipe nomeado do cliente | Windows NT, Windows 98, Windows 95 |
| Rpclts1.dll          | Servidor denominado-transporte de pipe | Windows NT, Windows 98, Windows 95 |
| Rpcltc3.dll          | Transporte TCP/IP do cliente     | Windows NT, Windows 98, Windows 95 |
| Rpclts3.dll          | Transporte TCP/IP do servidor     | Windows NT, Windows 98, Windows 95 |
| Rpcltc5.dll          | Transporte NetBIOS de cliente    | Windows NT, Windows 98, Windows 95 |
| Rpclts5.dll          | Transporte NetBIOS do servidor    | Windows NT, Windows 98, Windows 95 |
| Rpcltc6.dll          | Transporte SPX de cliente        | Windows NT, Windows 98, Windows 95 |
| Rpclts6.dll          | Transporte SPX do servidor        | Windows NT, Windows 98, Windows 95 |
| Rpcdgc6.dll          | Transporte IPX do cliente        | Windows NT                         |
| Rpcdgs6.dll          | Transporte IPX do servidor        | Windows NT                         |
| Rpcdgc3.dll          | Transporte UDP de cliente        | Windows NT                         |
| Rpcdgs3.dll          | Transporte UDP do servidor        | Windows NT                         |



 

Você também precisará do compilador linguagem IDL da Microsoft (MIDL). Para obter mais informações, consulte [usando o compilador MIDL](/windows/desktop/Midl/using-the-midl-compiler-2).

 

 