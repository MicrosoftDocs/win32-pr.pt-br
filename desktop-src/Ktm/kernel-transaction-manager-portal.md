---
description: Implemente o NTFS Transacional (TxF) e o registro transacional (TxR). O TxF permite operações de sistema de arquivos transacionadas no NTFS. TxR permite operações de registro transacionadas. Coordenar operações de registro e sistema de arquivos com uma transação.
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: Gerenciador de transações do kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281050461163d5fd0cde64af79e70569d613888e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751215"
---
# <a name="kernel-transaction-manager"></a>Gerenciador de transações do kernel

## <a name="purpose"></a>Finalidade

O KTM (kernel Transaction Manager) permite o desenvolvimento de aplicativos que usam transações. O mecanismo de transação em si está dentro do kernel, mas as transações podem ser desenvolvidas para transações de modo kernel ou de usuário e dentro de um único host ou entre hosts distribuídos.

O KTM é usado para implementar o NTFS Transacional (TxF) e o registro transacional (TxR). O TxF permite operações de sistema de arquivos transacionadas no sistema de arquivos NTFS. TxR permite operações de registro transacionadas. O KTM permite que os aplicativos cliente coordenem operações de registro e sistema de arquivos com uma transação.

Para desenvolver um aplicativo que coordena transações com recursos diferentes de TxF ou TxR, primeiro você deve desenvolver um serviço de reconhecimento de transações do Win32, também chamado de Gerenciador de recursos.

Os aplicativos gerenciados e COM+ devem usar seus gerenciadores de transações nativas.

## <a name="where-applicable"></a>Quando aplicável

O KTM pode ser usado com aplicativos e gerenciadores de recursos hospedados no Windows Vista ou no Windows Server 2008.

## <a name="developer-audience"></a>Público de desenvolvedores

A API de KTM foi projetada para uso por programadores C e C++.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O KTM tem suporte a partir do Windows Vista.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                     | Descrição                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Sobre](about-ktm.md)<br/>         | Informações gerais sobre transações e os recursos fornecidos pelo KTM.<br/>                           |
| [Referência](ktm-reference.md)<br/> | Documentação para as funções, estruturas de dados, enumerações e outros elementos de programação de KTM.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema de Arquivos de Log Comum](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[NTFS Transacional (TxF)](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

[Coordenador de Transações Distribuídas](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> </dl>

 

