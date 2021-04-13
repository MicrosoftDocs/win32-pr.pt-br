---
title: Chamada de Procedimento Remoto
description: A RPC (chamada de procedimento remoto) da Microsoft define uma tecnologia poderosa para a criação de programas de cliente/servidor distribuídos.
ms.assetid: 27c7c352-5fc1-47cf-99b1-fdf3eca986bc
keywords:
- RPC
- RPC, (consulte chamada de procedimento remoto)
- RPC de chamada de procedimento remoto, página inicial
- RPC de chamada de procedimento remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3461116468bf1d686d1a5695924e5fe66007b35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366529"
---
# <a name="remote-procedure-call"></a>Chamada de Procedimento Remoto

## <a name="purpose"></a>Finalidade

A RPC (chamada de procedimento remoto) da Microsoft define uma tecnologia poderosa para a criação de programas de cliente/servidor distribuídos. As bibliotecas e os stubs de tempo de execução do RPC gerenciam a maioria dos processos relacionados aos protocolos de rede e à comunicação. Isso permite que você se concentre nos detalhes do aplicativo em vez dos detalhes da rede.

## <a name="where-applicable"></a>Quando aplicável

O RPC pode ser usado em todos os aplicativos cliente/servidor com base em sistemas operacionais Windows. Ele também pode ser usado para criar programas de cliente e servidor para ambientes de rede heterogêneos que incluem sistemas operacionais como UNIX e Apple.

## <a name="developer-audience"></a>Público de desenvolvedores

O RPC foi projetado para ser usado por programadores C/C++. É necessário ter familiaridade com o linguagem IDL da Microsoft (MIDL) e o compilador MIDL.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

As bibliotecas de tempo de execução RPC estão incluídas no Windows. Os componentes do ambiente de desenvolvimento RPC são instalados quando você instala o SDK (Software Development Kit) do Microsoft Windows. Para obter detalhes, consulte [instalando o ambiente de programação RPC](installing-the-rpc-programming-environment.md).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                           | Descrição                                                                                                                      |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Melhores práticas de programação RPC](best-rpc-programming-practices.md)<br/> | Orientação sobre as práticas de programação de RPC que ajudam a criar os melhores aplicativos RPC possíveis.<br/>                            |
| [Visão geral](overviews.md)<br/>                                            | Informações gerais sobre a incorporação de RPC em seus aplicativos cliente/servidor.<br/>                                     |
| [Referência](reference.md)<br/>                                           | Documentação de tipos, funções e constantes de RPC.<br/>                                                                 |
| [Mecanismo de NDR de RPC](rpc-ndr-engine.md)<br/>                                 | Documentação do mecanismo de marshaling para componentes RPC e DCOM, o mecanismo de representação de dados de rede (NDR) RPC.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Linguagem IDL da Microsoft (MIDL)](/windows/desktop/Midl/midl-start-page)
</dt> </dl>

 

