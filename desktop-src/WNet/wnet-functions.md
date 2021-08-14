---
title: Funções WNet
description: Windows As funções de rede fornecem informações e utilitários para gerenciar recursos de rede.
ms.assetid: 8a83186f-a912-4c61-8137-1f6be1f3afd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771974bcc2967ddba32439bb655173f62b8478ad367e086e620ca02825a2567f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330781"
---
# <a name="wnet-functions"></a>Funções WNet

Windows As funções de rede fornecem informações e utilitários para gerenciar recursos de rede. As Windows funções de rede podem ser agrupadas da seguinte forma:

-   [Funções de conexão](#connection-functions)
-   [Funções de enumeração](#enumeration-functions)
-   [Funções informativas](#information-functions)
-   [Funções de usuário](#user-functions)

## <a name="connection-functions"></a>Funções de conexão

Chame as seguintes funções de conexão WNet para conectar um dispositivo local a um recurso de rede e cancelar conexões de rede.



| Função                                                                     | Descrição                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MultinetGetConnectionPerformance**](/windows/win32/api/winnetwk/nf-winnetwk-multinetgetconnectionperformancea) | Retorna informações sobre o desempenho esperado de uma conexão com um recurso de rede.                                                                                                                                      |
| [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)                               | Conecta um dispositivo local a um recurso de rede. (Fornecido para compatibilidade com versões de 16 bits do Windows.)                                                                                                                   |
| [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a)                             | Conecta um dispositivo local a um recurso de rede.                                                                                                                                                                                 |
| [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)                             | Conecta um dispositivo local a um recurso de rede. Essa função inclui mais um parâmetro do que a **função WNetAddConnection2,** um handle para uma janela que o provedor de rede pode usar como uma janela de proprietário para caixas de diálogo. |
| [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona)                         | Cancela uma conexão de rede. (Fornecido para compatibilidade com versões de 16 bits do Windows.)                                                                                                                                    |
| [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)                       | Cancela uma conexão de rede, fornecendo a capacidade de atualizar o perfil do usuário com informações sobre conexões persistentes.                                                                                                  |
| [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog)                         | Inicia uma caixa de diálogo de navegação geral para se conectar aos recursos de rede.                                                                                                                                                      |
| [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a)                       | Inicia uma caixa de diálogo de navegação geral para se conectar aos recursos de rede usando uma [**estrutura CONNECTDLGSTRUCT.**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa)                                                                                  |
| [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog)                         | Inicia uma caixa de diálogo de navegação geral para se desconectar dos recursos de rede.                                                                                                                                                 |
| [**WNetDisconnectDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog1a)                       | Inicia uma caixa de diálogo de navegação geral para se desconectar dos recursos de rede usando uma [**estrutura DISCDLGSTRUCT.**](/windows/win32/api/winnetwk/ns-winnetwk-discdlgstructa)                                                                                   |
| [**WNetGetConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona)                               | Recupera o nome do recurso de rede associado a um dispositivo local.                                                                                                                                                     |
| [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea)                         | Quando um caminho baseado em unidade é dado para um recurso de rede, retorna uma forma mais universal do nome.                                                                                                                               |
| [**WNetRestoreConnectionW**](/windows/win32/api/winnetwk/nf-winnetwk-wnetrestoreconnectionw)                     | Restaura a conexão com um recurso de rede, solicitando ao usuário, se necessário, um nome e uma senha.                                                                                                                      |
| [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona)                               | Conecta um dispositivo local a um recurso de rede; seleciona automaticamente um dispositivo local não usuário para redirecionar para o recurso de rede.                                                                                               |



 

> [!Note]  
> As [**funções WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) e [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) têm suporte para compatibilidade com Windows para grupos de trabalho. No entanto, novos aplicativos devem usar [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) ou [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)e [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).

 

## <a name="enumeration-functions"></a>Funções de enumeração

Chame as funções WNet a seguir para enumerar recursos de rede.



| Função                                     | Descrição                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum)       | Encerra uma enumeração de recurso de rede.                                                    |
| [**Wnetenumresource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) | Continua uma enumeração de recursos de rede iniciada pela **função WNetOpenEnum.** |
| [**Wnetopenenum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma)         | Inicia uma enumeração de recursos de rede.                                             |



 

## <a name="information-functions"></a>Funções informativas

Chame as funções informativas e de utilitário WNet a seguir para recuperar o provedor de rede e outras informações.



| Função                                                         | Descrição                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora)                     | Retorna o código de erro mais recente definido por uma função WNet, o relatado por um provedor de rede.  |
| [**WNetGetNetworkInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetnetworkinformationa)   | Retorna informações estendidas sobre um provedor de rede específico.                                     |
| [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)               | Retorna o nome do provedor para um tipo específico de rede.                                           |
| [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) | Retorna o provedor de rede que possui um recurso e obtém informações sobre o tipo de recurso. |
| [**WNetGetResourceParent**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceparenta)           | Retorna o pai de um recurso de rede.                                                           |



 

## <a name="user-functions"></a>Funções de usuário

Chame a função WNet a seguir para recuperar o nome do usuário associado a um dispositivo local.



| Função                           | Descrição                                                                              |
|------------------------------------|------------------------------------------------------------------------------------------|
| [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) | Retorna o nome de usuário padrão atual ou o nome de usuário que estabeleceu a conexão. |



 

Muitas das funções WNet usam uma estrutura [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) para armazenar informações sobre um recurso de rede.

 

 