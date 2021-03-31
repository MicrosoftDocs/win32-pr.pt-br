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
- carregando BITS de arquivos
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: a531821665490735b391ab2714f5b37146c6bc1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917551"
---
# <a name="background-intelligent-transfer-service"></a>BITS

## <a name="purpose"></a>Finalidade

Serviço de Transferência Inteligente em Segundo Plano (BITS) é usado por programadores e administradores de sistema para baixar arquivos de ou carregar arquivos para servidores Web HTTP e compartilhamentos de arquivos SMB. O BITS levará o custo da transferência em consideração, bem como o uso da rede para que o trabalho em primeiro plano do usuário tenha o menor impacto possível. O BITS também lida com interuptions de rede, pausando e retomando transferências automaticamente, mesmo após uma reinicialização. O BITS inclui cmdlets do PowerShell para criar e gerenciar transferências, bem como o utilitário de linha de comando BitsAdmin.

> [!Note]  
> O BITS pode ser usado pelo Windows para baixar atualizações para seu sistema local. Se você for um usuário final pesquisando maneiras de solucionar problemas de instalação do BITS, consulte [corrigir problemas de Windows Update](https://support.microsoft.com/help/10164/fix-windows-update-errors). 
 

## <a name="where-applicable"></a>Quando aplicável

Use o BITS para aplicativos que precisam:

-   Baixar de ou carregar arquivos para um servidor Web ou servidor de arquivos SMB de HTTP ou REST.
-   Retome automaticamente as transferências de arquivos após a desconexão da rede e a reinicialização do computador.
-   Preserve a capacidade de resposta de outros aplicativos de rede.
-   Lembre-se do custo de rede em como, por exemplo, redes móveis
-   Opcionalmente, trabalhar com o [BranchCache](/windows-server/networking/branchcache/branchcache) para otimizar o tráfego de WAN (rede de longa distância)

## <a name="developer-audience"></a>Público de desenvolvedores

O BITS é uma interface COM criada para desenvolvedores C e C++ que também podem ser usados por desenvolvedores do .NET. Os desenvolvedores de UWP devem usar a API [Windows. Networking. BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) e não a API bits.

## <a name="bits-versions"></a>Versões do BITS

Para obter o histórico de versão completo e informações sobre o sistema operacional anterior, consulte [novidades](what-s-new.md).


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                           | Descrição                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre BITS](about-bits.md)<br/>                         | Informações gerais sobre o BITS.<br/>                                                                                                                                      |
| [Usando BITS](using-bits.md)<br/>                         | Guia de procedimentos para o desenvolvimento de clientes BITS que transferem arquivos entre um cliente e um servidor.<br/>                                                                        |
| [Referência BITS](bits-reference.md)<br/>                 | Informações de referência para as interfaces de programação BITS. Também contém informações sobre exemplos, ferramentas, configurações de servidor para trabalhos de upload e o protocolo de upload.<br/> |
| [Práticas recomendadas](best-practices-when-using-bits.md)<br/> | Informações a serem consideradas ao criar um aplicativo que usa BITS.<br/>                                                                                                |



 

## <a name="additional-resources"></a>Recursos adicionais

A seguir estão os recursos adicionais.


|             |                                                                                                                                                 |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL de referência do .NET   | Para obter informações sobre como usar BITS do .NET usando DLLs de referência, consulte [chamando em bits do .NET usando DLLs de referência](/windows/desktop/Bits/bits-dot-net)      |
| Wrapper do .NET   | Para outros wrappers .NET para BITS, você pode pesquisar [NuGet](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) para projetos marcados com a marca bits.        |



 

 

