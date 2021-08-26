---
description: Implemente O NTFS Transacional (TxF) e o Registro Transacional (TxR). O TxF permite operações transacionados do sistema de arquivos no NTFS. O TxR permite operações de registro transacionados. Coordene o sistema de arquivos e as operações do Registro com uma transação.
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: Gerenciador de Transações do Kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c446931fff4f119217a5f6e5f1b7ae8cf351cf94966a9da5abc4e4d2e88d787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897526"
---
# <a name="kernel-transaction-manager"></a>Gerenciador de Transações do Kernel

## <a name="purpose"></a>Finalidade

O KTM (Kernel Transaction Manager) permite o desenvolvimento de aplicativos que usam transações. O próprio mecanismo de transação está dentro do kernel, mas as transações podem ser desenvolvidas para transações de modo de usuário ou kernel e dentro de um único host ou entre hosts distribuídos.

O KTM é usado para implementar O TxF (Transactional NTFS) e o TxR (Registro Transacional). O TxF permite operações transacionados do sistema de arquivos no sistema de arquivos NTFS. O TxR permite operações de registro transacionados. O KTM permite que os aplicativos cliente coordenem o sistema de arquivos e as operações do Registro com uma transação.

Para desenvolver um aplicativo que coordena transações com recursos que não são TxF ou TxR, primeiro você deve desenvolver um serviço com conhecimento de transação Win32, também chamado de gerenciador de recursos.

Aplicativos gerenciados e COM+ devem usar seus gerenciadores de transações nativos.

## <a name="where-applicable"></a>Quando aplicável

O KTM pode ser usado com aplicativos e gerenciadores de recursos hospedados no Windows Vista ou Windows Server 2008.

## <a name="developer-audience"></a>Público de desenvolvedores

A API KTM foi projetada para uso por programadores C e C++.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Há suporte para KTM a partir do Windows Vista.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                     | Descrição                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Sobre](about-ktm.md)<br/>         | Informações gerais sobre transações e os recursos fornecidos pela KTM.<br/>                           |
| [Referência](ktm-reference.md)<br/> | Documentação para as funções, estruturas de dados, enumerações e outros elementos de programação do KTM.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema de Arquivos de Log Comum](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[NTFS transacional (TxF)](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

[Coordenador de Transações Distribuídas](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> </dl>

 

