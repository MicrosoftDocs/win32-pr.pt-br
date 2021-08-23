---
title: Armazenamento Modelos
description: O armazenamento assíncrono dá suporte a dois modos de armazenamento que bloqueiam e não bloqueiam, que um cliente (um navegador ou o próprio objeto) pode especificar retornando BINDF \_ ASYNCSTORAGE da chamada do moniker para IBindStatusCallback GetBindInfo.
ms.assetid: df8f9e2c-40d2-4997-b5f9-bdbc524437cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db1a0a4c08daa1663f7513226dc25f4d5c8fd26341a6c8ee7d90a2ec0d1099db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661826"
---
# <a name="storage-modes"></a>Armazenamento Modelos

O armazenamento assíncrono dá suporte a dois modos de armazenamento: bloqueio e não bloqueio, que um cliente (um navegador ou o próprio objeto) pode especificar retornando BINDF \_ ASYNCSTORAGE da chamada do moniker para [**IBindStatusCallback:: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)). Se um cliente especificar BINDF \_ ASYNCSTORAGE, ele receberá um ponteiro para um armazenamento assíncrono não bloqueado. Caso contrário, ele receberá um ponteiro para um armazenamento assíncrono de bloqueio. Mesmo que o cliente não solicite uma operação de vinculação assíncrona (não registrando [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) com o contexto de associação), o moniker ainda retorna um armazenamento assíncrono de bloqueio, permitindo o carregamento progressivo de aplicativos herdados.

No modo de não bloqueio, um armazenamento assíncrono retorna E \_ pendente quando os dados estão indisponíveis. Após receber essa mensagem, o cliente aguardará a notificação de que os dados adicionais estão disponíveis antes de tentar novamente baixá-lo.

No modo de bloqueio, em vez de retornar E \_ pendente, o armazenamento assíncrono bloqueia a chamada até que novos dados estejam disponíveis, desbloqueia a chamada e retorna os novos dados. O cliente deve estar pronto para receber os dados. Embora o thread seja bloqueado, os dados já passados para o cliente estão totalmente disponíveis para o usuário.

O modo de bloqueio é necessário porque os clientes que não reconhecem o armazenamento assíncrono não reconhecerão E \_ pendentes e irão supor que ocorreu um erro irrecuperável. O bloqueio do armazenamento assíncrono permite que os clientes existentes façam renderização progressiva.

 

 