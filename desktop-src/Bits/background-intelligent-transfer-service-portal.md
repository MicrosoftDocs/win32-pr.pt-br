---
title: BITS
description: O BITS (Serviço de Transferência Inteligente em Segundo Plano) transfere arquivos (downloads ou uploads) entre um cliente e um servidor e fornece informações de progresso relacionadas às transferências.
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- BITS
- Serviço de Transferência Inteligente em Segundo Plano, página inicial
- BITS (consulte Serviço de Transferência Inteligente em Segundo Plano)
- baixando arquivos BITS
- BITS de transferência de arquivo em segundo plano
- carregando arquivos BITS
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 66bc9af5231454ef63d8c74f9e500baaeb7c8cec9dbdd694943a3809da4a391d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588726"
---
# <a name="background-intelligent-transfer-service"></a>BITS

## <a name="purpose"></a>Finalidade

Serviço de Transferência Inteligente em Segundo Plano bits (BITS) é usado por programadores e administradores de sistema para baixar ou carregar arquivos em servidores Web HTTP e compartilhamentos de arquivos SMB. O BITS levará em consideração o custo da transferência, bem como o uso da rede para que o trabalho em primeiro plano do usuário tenha o menor impacto possível. O BITS também lida com interupções de rede, pausando e retomando automaticamente as transferências, mesmo após uma reinicialização. O BITS inclui cmdlets do PowerShell para criar e gerenciar transferências, bem como o utilitário de linha de comando BitsAdmin.

> [!Note]  
> O BITS pode ser usado por Windows para baixar atualizações para seu sistema local. Se você for um usuário final que está procurando maneiras de solucionar problemas de instalação do BITS, consulte [Corrigir Windows problemas de atualização.](https://support.microsoft.com/help/10164/fix-windows-update-errors) 
 

## <a name="where-applicable"></a>Quando aplicável

Use BITS para aplicativos que precisam:

-   Baixe ou carregue arquivos em um servidor Web HTTP ou REST ou servidor de arquivos SMB.
-   Retomar automaticamente as transferências de arquivos depois que a rede se desconectar e o computador reiniciar.
-   Preservar a capacidade de resposta de outros aplicativos de rede.
-   Cuidado com o custo de rede em redes móveis, por exemplo,
-   Opcionalmente, trabalhe com [o BranchCache](/windows-server/networking/branchcache/branchcache) para otimizar o tráfego de WAN (rede de ampla área)

## <a name="developer-audience"></a>Público de desenvolvedores

BITS é uma interface COM projetada para desenvolvedores C e C++ que também pode ser usada por desenvolvedores do .NET. Os desenvolvedores da UWP devem usar [o Windows. API Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) e não a API bits.

## <a name="bits-versions"></a>Versões do BITS

Para obter o histórico completo de versões e informações sobre o sistema operacional anterior, consulte [Novidades.](what-s-new.md)


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                           | Descrição                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre BITS](about-bits.md)<br/>                         | Informações gerais sobre BITS.<br/>                                                                                                                                      |
| [Usando BITS](using-bits.md)<br/>                         | Guia de procedimento para desenvolver clientes BITS que transferem arquivos entre um cliente e um servidor.<br/>                                                                        |
| [Referência BITS](bits-reference.md)<br/>                 | Informações de referência para as interfaces de programação BITS. Também contém informações sobre exemplos, ferramentas, configurações de servidor para trabalhos de upload e o protocolo de upload.<br/> |
| [Práticas recomendadas](best-practices-when-using-bits.md)<br/> | Informações a considerar ao criar um aplicativo que usa BITS.<br/>                                                                                                |



 

## <a name="additional-resources"></a>Recursos adicionais

A seguir estão recursos adicionais.


|    Recurso         |    Descrição                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL de referência do .NET   | Para obter informações sobre como usar o BITS do .NET usando DLLs de referência, consulte Chamando bits do [.NET usando DLLs de referência](/windows/desktop/Bits/bits-dot-net)      |
| Wrapper do .NET   | Para outros wrappers do .NET para BITS, você pode pesquisar [projetos marcados](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) no nuget com a marca BITS.        |



 

 

