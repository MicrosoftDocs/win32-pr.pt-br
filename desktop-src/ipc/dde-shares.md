---
description: Os compartilhamentos DDE são um recurso de máquina.
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: Compartilhamentos DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5e3416235f78e48c68b7d2e35c7ac042f8ff5d6eac79cc2471efa5ea12d82b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602116"
---
# <a name="dde-shares"></a>Compartilhamentos DDE

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

Os compartilhamentos DDE são um recurso de máquina. Eles são semelhantes aos compartilhamentos de arquivos porque são usados para controlar o acesso a um recurso. Com compartilhamentos de arquivos, o recurso é um arquivo. Com compartilhamentos DDE, o recurso é trocado de dados dinamicamente. O tipo de dados trocado é determinado pelo aplicativo de servidor que fornece os dados e o aplicativo cliente que solicita os dados.

O servidor chama a função [**NDdeShareAdd**](nddeshareadd.md) para criar o compartilhamento DDE, que é armazenado no DSDM (Gerenciador de banco de dados de compartilhamento DDE).

O cliente inicia a conversa DDE conectando-se ao compartilhamento DDE. O cliente deve chamar a função [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) para inicializar o ddeml e chamar a função [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) para se conectar ao compartilhamento de DDE. Na chamada **DdeConnect** , o cliente especifica o nome do serviço da seguinte maneira:

\\\\*ComputerName* \\ NDDE $

em que *ComputerName* é o nome do computador que executa o aplicativo de servidor. O NDDE $ indica que o tópico fornecido para [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) é o nome do compartilhamento DDE no computador remoto chamado *ComputerName*.

Há três tipos de compartilhamentos DDE: estilo antigo, novo estilo e estático. É comum dar suporte apenas ao tipo estático. Os nomes de compartilhamentos estáticos usam a seguinte convenção: *ShareName*$.

 

 
