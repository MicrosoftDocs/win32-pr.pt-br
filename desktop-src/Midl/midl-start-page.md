---
title: linguagem IDL da Microsoft
description: O linguagem IDL da Microsoft (MIDL) define interfaces entre programas cliente e servidor.
ms.assetid: 5ed1ff94-bbcb-4c6e-83aa-63d24eb84859
keywords:
- MIDL MIDL
- MIDL MIDL , (consulte linguagem IDL da Microsoft MIDL )
- linguagem IDL da Microsoft MIDL
- linguagem IDL da Microsoft MIDL, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9062d5b2af18f7c3aa5ad57a4cb8f606cccc43333e4eff17d3518f72b7a064a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534966"
---
# <a name="microsoft-interface-definition-language"></a>linguagem IDL da Microsoft

## <a name="purpose"></a>Finalidade

O linguagem IDL da Microsoft (MIDL) define interfaces entre programas cliente e servidor. A Microsoft inclui o compilador MIDL com o SDK (Kit de Desenvolvimento de Software de Plataforma) para permitir que os desenvolvedores criem os arquivos de IDL (linguagem de definição de interface) e os arquivos de configuração de aplicativo (ACF) necessários para interfaces RPC (chamada de procedimento remoto) e interfaces COM/DCOM. O MIDL também dá suporte à geração de bibliotecas de tipos para Automação OLE.

## <a name="where-applicable"></a>Quando aplicável

MIDL pode ser usado em todos os aplicativos cliente/servidor com base Windows operacionais. Ele também pode ser usado para criar programas de cliente e servidor para ambientes de rede heterogêneos que incluem sistemas operacionais como Unix e Apple. A Microsoft dá suporte ao padrão de DCE Open Group (anteriormente conhecido como Open Software Foundation) para interoperabilidade RPC.

## <a name="developer-audience"></a>Público de desenvolvedores

Ao usar MIDL com RPC, é necessária familiaridade com a programação C/C++ e o paradigma RPC. Ao usar MIDL com COM, a familiaridade com a programação C++ e o paradigma RPC como ela se aplica ao COM é necessária ou, como alternativa, é necessária familiaridade com scripts de modelo de Automação OLE e bibliotecas de tipos.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

As bibliotecas de tempo de run time apropriadas para usar MIDL são incluídas com Windows. O compilador MIDL e os componentes do ambiente de desenvolvimento RPC são instalados quando você instala o SDK do Windows. Para obter mais informações, [consulte Usando o compilador MIDL](using-the-midl-compiler-2.md) e [Instalando o ambiente de programação RPC](/windows/desktop/Rpc/installing-the-rpc-programming-environment).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                               | Descrição                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Visão geral](about-this-guide-2.md)<br/>                                                       | Informações gerais sobre MIDL e o compilador MIDL.<br/>                   |
| [Usando o compilador MIDL](using-the-midl-compiler-2.md)<br/>                                 | Informações sobre como usar o compilador MIDL para gerar stubs RPC.<br/>       |
| [Definições de interface e bibliotecas de tipos](interface-definitions-and-type-libraries.md)<br/> | Documentação de definições de interface específicas de RPC e bibliotecas de tipos.<br/> |
| [Referência de Command-Line MIDL](midl-command-line-reference.md)<br/>                           | Documentação das opções de linha de comando do compilador MIDL.<br/>               |
| [Referência da linguagem MIDL](midl-language-reference.md)<br/>                                   | A referência de linguagem do compilador MIDL.<br/>                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[RPC (Chamada de Procedimento Remoto)](/windows/desktop/Rpc/rpc-start-page)
</dt> </dl>

 

