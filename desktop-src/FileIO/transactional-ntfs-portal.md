---
description: O NTFS transacional (TxF) permite que as operações de arquivo em um volume do sistema de arquivos NTFS sejam executadas em uma transação.
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: NTFS transacional (TxF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5b44a35e4f83c1389d1fc2e6bc3de4f97f5ad203bbdee4750c2fcd26d87f47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119431906"
---
# <a name="transactional-ntfs-txf"></a>NTFS transacional (TxF)

\[A Microsoft recomenda fortemente que os desenvolvedores utilizem meios alternativos para atingir as necessidades do aplicativo. Muitos cenários para os que o TxF foi desenvolvido podem ser obtidos por meio de técnicas mais simples e prontamente disponíveis. Além disso, o TxF pode não estar disponível em versões futuras do Microsoft Windows. Para obter mais informações e alternativas ao TxF, consulte Alternativas ao uso [de NTFS transacional.](deprecation-of-txf.md)\]

## <a name="purpose"></a>Finalidade

O NTFS transacional (TxF) permite que as operações de arquivo em um volume do sistema de arquivos NTFS sejam executadas em uma transação. As transações TxF aumentam a confiabilidade do aplicativo protegendo a integridade dos dados contra falhas e simplificando o desenvolvimento de aplicativos, reduzindo consideravelmente a quantidade de código de tratamento de erros.

O TxF usa a estrutura de transação fornecida pelo [KTM (Kernel Transaction Manager).](/windows/desktop/Ktm/kernel-transaction-manager-portal) Isso permite que as operações de arquivo TxF sejam parte de uma transação que envolve outras fontes de dados, como SQL Server e TxR (Registro Transacionado).

## <a name="where-applicable"></a>Quando aplicável

Um aplicativo pode usar o TxF para preservar a integridade dos dados no disco causados por condições de erro inesperadas e ajudar a resolver cenários simultâneos de usuário do sistema de arquivos isolando suas alterações de outros enquanto as alterações estão sendo feitas.

## <a name="developer-audience"></a>Público de desenvolvedores

Antes de usar o TxF, você deve ter um conhecimento prático das transações usando KTM [ou Coordenador de Transações Distribuídas (DTC).](/previous-versions/windows/desktop/ms684146(v=vs.85))

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O TxF está disponível a partir do Windows Vista.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                    | Descrição                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Sobre](about-transactional-ntfs.md)<br/>         | Informações gerais sobre NTFS transacional.<br/>                                                   |
| [Referência](transactional-ntfs-reference.md)<br/> | Documentação para as funções, estruturas de dados, enumerações e outros elementos de programação.<br/> |



 

 

