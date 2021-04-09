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
# <a name="connectto"></a><span data-ttu-id="3cb6a-103">ConnectTo</span><span class="sxs-lookup"><span data-stu-id="3cb6a-103">ConnectTo</span></span>

<span data-ttu-id="3cb6a-104">**HKLM \\ software \\ Microsoft \\ MSSQLSERVER \\ Client**</span><span class="sxs-lookup"><span data-stu-id="3cb6a-104">**HKLM\\SOFTWARE\\Microsoft\\MSSQLServer\\Client**</span></span>

## <a name="description"></a><span data-ttu-id="3cb6a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3cb6a-105">Description</span></span>

<span data-ttu-id="3cb6a-106">A subchave **connectto** armazena informações de conexão para clientes baseados no Windows que se conectam a instâncias do mecanismo de banco de dados Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-106">The **ConnectTo** subkey stores connection information for Windows-based clients that connect to instances of the Microsoft SQL Server database engine.</span></span> <span data-ttu-id="3cb6a-107">As entradas do registro nessa subchave são do tipo de dados REG \_ sz, e seus valores especificam o Net-Library a ser usado para se conectar à instância, bem como quaisquer parâmetros específicos da rede.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-107">Registry entries in this subkey are of data type REG\_SZ, and their values specify the Net-Library to use for connecting to the instance, as well as any network-specific parameters.</span></span>

<span data-ttu-id="3cb6a-108">As informações de conexão armazenadas nesta subchave são lidas pelo provedor de OLE DB para SQL Server, o driver ODBC SQL Server ou o SQL Server DB-Library biblioteca de vínculo dinâmico (DLL).</span><span class="sxs-lookup"><span data-stu-id="3cb6a-108">The connection information stored in this subkey is read by the OLE DB Provider for SQL Server, the SQL Server ODBC driver, or the SQL Server DB-Library dynamic-link library (DLL).</span></span>

## <a name="change-method"></a><span data-ttu-id="3cb6a-109">Alterar Método</span><span class="sxs-lookup"><span data-stu-id="3cb6a-109">Change Method</span></span>

<span data-ttu-id="3cb6a-110">Você não deve modificar entradas nesta subchave usando o editor do registro.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-110">You should not modify entries in this subkey by using the registry editor.</span></span> <span data-ttu-id="3cb6a-111">Use o utilitário SQL Server Client Network para configurar o nome do servidor e as informações de conexão.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-111">Use the SQL Server Client Network Utility to configure server name and connection information.</span></span> <span data-ttu-id="3cb6a-112">Confira SQL Server ajuda do utilitário de rede do cliente para obter mais instruções.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-112">See SQL Server Client Network Utility Help for further instructions.</span></span>

## <a name="notes"></a><span data-ttu-id="3cb6a-113">Observações</span><span class="sxs-lookup"><span data-stu-id="3cb6a-113">Notes</span></span>

-   <span data-ttu-id="3cb6a-114">A subchave **connectto** é usada pelo provedor de OLE DB para SQL Server, o Driver ODBC SQL Server e o SQL Server DB-Library dll.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-114">The **ConnectTo** subkey is used by the OLE DB Provider for SQL Server, the SQL Server ODBC Driver, and the SQL Server DB-Library DLL.</span></span> <span data-ttu-id="3cb6a-115">As entradas nessa subchave identificam quais Net-Library esses componentes da API (interface de programação de aplicativo) de acesso a dados chamam.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-115">Entries in this subkey identify which Net-Library these data access application programming interface (API) components call.</span></span>
-   <span data-ttu-id="3cb6a-116">Net-Libraries são componentes SQL Server que protegem os componentes da API de acesso a dados dos detalhes do uso de diferentes métodos de comunicação entre processos (IPC) para se comunicar com uma instância do mecanismo de banco de dados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-116">Net-Libraries are SQL Server components that shield the data access API components from the details of using different Interprocess Communication (IPC) methods to communicate with an instancess of the SQL Server database engine.</span></span>
-   <span data-ttu-id="3cb6a-117">A atualização incorreta da subchave **connectto** pode impedir que os aplicativos se conectem com êxito a uma instância do mecanismo de banco de dados SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3cb6a-117">Improperly updating the **ConnectTo** subkey might prevent applications from successfully connecting to an instance of the SQL Server database engine.</span></span>

 

 



