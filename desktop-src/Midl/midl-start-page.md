---
title: linguagem IDL da Microsoft
description: O linguagem IDL da Microsoft (MIDL) define as interfaces entre os programas cliente e servidor.
ms.assetid: 5ed1ff94-bbcb-4c6e-83aa-63d24eb84859
keywords:
- MIDL MIDL
- MIDL MIDL, (consulte linguagem IDL da Microsoft MIDL)
- MIDL de linguagem IDL da Microsoft
- MIDL linguagem IDL da Microsoft, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e274d66ae234205f5db1f41b2d191ea409561bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007445"
---
# <a name="microsoft-interface-definition-language"></a>linguagem IDL da Microsoft

## <a name="purpose"></a>Finalidade

O linguagem IDL da Microsoft (MIDL) define as interfaces entre os programas cliente e servidor. A Microsoft inclui o compilador MIDL com o SDK (Software Development Kit) da plataforma para permitir que os desenvolvedores criem os arquivos IDL (Interface Definition Language) e os ACF (arquivos de configuração de aplicativo) necessários para as interfaces RPC (chamada de procedimento remoto) e interfaces COM/DCOM. O MIDL também dá suporte à geração de bibliotecas de tipos para automação OLE.

## <a name="where-applicable"></a>Quando aplicável

O MIDL pode ser usado em todos os aplicativos cliente/servidor baseados em sistemas operacionais Windows. Ele também pode ser usado para criar programas de cliente e servidor para ambientes de rede heterogêneos que incluem sistemas operacionais como UNIX e Apple. A Microsoft dá suporte ao grupo aberto (anteriormente conhecido como o padrão DCE da Open Software Foundation) para a interoperabilidade RPC.

## <a name="developer-audience"></a>Público de desenvolvedores

Ao usar MIDL com RPC, familiaridade com programação C/C++ e o paradigma de RPC é necessária. Ao usar MIDL com com, familiaridade com programação em C++ e o paradigma de RPC como se aplica ao COM é necessária ou, como alternativa, familiaridade com scripts de modelo de automação OLE e bibliotecas de tipos é necessária.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

As bibliotecas de tempo de execução apropriadas para usar o MIDL estão incluídas no Windows. O compilador MIDL e os componentes do ambiente de desenvolvimento RPC são instalados quando você instala o SDK do Windows. Para obter mais informações, consulte [usando o compilador MIDL](using-the-midl-compiler-2.md) e [instalando o ambiente de programação RPC](/windows/desktop/Rpc/installing-the-rpc-programming-environment).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                               | Descrição                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Visão geral](about-this-guide-2.md)<br/>                                                       | Informações gerais sobre MIDL e o compilador MIDL.<br/>                   |
| [Usando o compilador MIDL](using-the-midl-compiler-2.md)<br/>                                 | Informações sobre como usar o compilter MIDL para gerar stubs RPC.<br/>       |
| [Definições de interface e bibliotecas de tipos](interface-definitions-and-type-libraries.md)<br/> | Documentação de definições de interface específicas de RPC e bibliotecas de tipos.<br/> |
| [Referência de Command-Line de MIDL](midl-command-line-reference.md)<br/>                           | Documentação das opções de linha de comando do compilador MIDL.<br/>               |
| [Referência da linguagem MIDL](midl-language-reference.md)<br/>                                   | A referência de linguagem do compilador MIDL.<br/>                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[RPC (chamada de procedimento remoto)](/windows/desktop/Rpc/rpc-start-page)
</dt> </dl>

 

