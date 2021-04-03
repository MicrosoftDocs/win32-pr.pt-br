---
description: Os compartilhamentos DDE são um recurso de máquina.
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: Compartilhamentos DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 012c219897187c9e68b5b9e662b93678b77974c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828625"
---
# <a name="dde-shares"></a>Compartilhamentos DDE

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

Os compartilhamentos DDE são um recurso de máquina. Eles são semelhantes aos compartilhamentos de arquivos porque são usados para controlar o acesso a um recurso. Com compartilhamentos de arquivos, o recurso é um arquivo. Com compartilhamentos DDE, o recurso é trocado de dados dinamicamente. O tipo de dados trocado é determinado pelo aplicativo de servidor que fornece os dados e o aplicativo cliente que solicita os dados.

O servidor chama a função [**NDdeShareAdd**](nddeshareadd.md) para criar o compartilhamento DDE, que é armazenado no DSDM (Gerenciador de banco de dados de compartilhamento DDE).

O cliente inicia a conversa DDE conectando-se ao compartilhamento DDE. O cliente deve chamar a função [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) para inicializar o ddeml e chamar a função [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) para se conectar ao compartilhamento de DDE. Na chamada **DdeConnect** , o cliente especifica o nome do serviço da seguinte maneira:

\\\\*ComputerName* \\ NDDE $

em que *ComputerName* é o nome do computador que executa o aplicativo de servidor. O NDDE $ indica que o tópico fornecido para [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) é o nome do compartilhamento DDE no computador remoto chamado *ComputerName*.

Há três tipos de compartilhamentos DDE: estilo antigo, novo estilo e estático. É comum dar suporte apenas ao tipo estático. Os nomes de compartilhamentos estáticos usam a seguinte convenção: *ShareName*$.

 

 
