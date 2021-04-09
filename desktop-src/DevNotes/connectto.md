---
description: HKLM \\ software \\ Microsoft \\ MSSQLSERVER \\ Client.
ms.assetid: d6eb774b-d7ae-4f51-9947-90fb176e9acf
title: ConnectTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b1f77fc90bca467e90a3c3b7f407b8ba6d33d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010165"
---
# <a name="connectto"></a>ConnectTo

**HKLM \\ software \\ Microsoft \\ MSSQLSERVER \\ Client**

## <a name="description"></a>Descrição

A subchave **connectto** armazena informações de conexão para clientes baseados no Windows que se conectam a instâncias do mecanismo de banco de dados Microsoft SQL Server. As entradas do registro nessa subchave são do tipo de dados REG \_ sz, e seus valores especificam o Net-Library a ser usado para se conectar à instância, bem como quaisquer parâmetros específicos da rede.

As informações de conexão armazenadas nesta subchave são lidas pelo provedor de OLE DB para SQL Server, o driver ODBC SQL Server ou o SQL Server DB-Library biblioteca de vínculo dinâmico (DLL).

## <a name="change-method"></a>Alterar Método

Você não deve modificar entradas nesta subchave usando o editor do registro. Use o utilitário SQL Server Client Network para configurar o nome do servidor e as informações de conexão. Confira SQL Server ajuda do utilitário de rede do cliente para obter mais instruções.

## <a name="notes"></a>Observações

-   A subchave **connectto** é usada pelo provedor de OLE DB para SQL Server, o Driver ODBC SQL Server e o SQL Server DB-Library dll. As entradas nessa subchave identificam quais Net-Library esses componentes da API (interface de programação de aplicativo) de acesso a dados chamam.
-   Net-Libraries são componentes SQL Server que protegem os componentes da API de acesso a dados dos detalhes do uso de diferentes métodos de comunicação entre processos (IPC) para se comunicar com uma instância do mecanismo de banco de dados do SQL Server.
-   A atualização incorreta da subchave **connectto** pode impedir que os aplicativos se conectem com êxito a uma instância do mecanismo de banco de dados SQL Server.

 

 



