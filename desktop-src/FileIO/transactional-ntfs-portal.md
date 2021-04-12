---
description: O NTFS Transacional (TxF) permite que as operações de arquivo em um volume do sistema de arquivos NTFS sejam executadas em uma transação.
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: NTFS Transacional (TxF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7553bfc7cae0b5389762527f0ac726c674a6a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501280"
---
# <a name="transactional-ntfs-txf"></a>NTFS Transacional (TxF)

\[A Microsoft recomenda enfaticamente que os desenvolvedores utilizem meios alternativos para atender às necessidades do seu aplicativo. Muitos cenários para os quais o TxF foi desenvolvido podem ser obtidos por meio de técnicas mais simples e mais prontamente disponíveis. Além disso, o TxF pode não estar disponível em versões futuras do Microsoft Windows. Para obter mais informações e alternativas para o TxF, consulte [alternativas para usar o NTFS Transacional](deprecation-of-txf.md).\]

## <a name="purpose"></a>Finalidade

O NTFS Transacional (TxF) permite que as operações de arquivo em um volume do sistema de arquivos NTFS sejam executadas em uma transação. As transações de TxF aumentam a confiabilidade do aplicativo protegendo a integridade dos dados entre falhas e simplificam o desenvolvimento de aplicativos, reduzindo muito a quantidade de código de tratamento de erros.

O TxF usa a estrutura de transação fornecida pelo KTM ( [kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal) ). Isso permite que as operações de arquivo TxF façam parte de uma transação que envolve outras fontes de dados, como SQL Server e registro transacionado (TxR).

## <a name="where-applicable"></a>Quando aplicável

Um aplicativo pode usar o TxF para preservar a integridade dos dados em disco causados por condições de erro inesperadas e ajudar a resolver cenários de usuário simultâneos do sistema de arquivos isolando suas alterações de outros enquanto as alterações estão sendo feitas.

## <a name="developer-audience"></a>Público de desenvolvedores

Antes de usar o TxF, você deve ter um conhecimento funcional das transações usando o KTM ou o [Coordenador de transações distribuídas (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)).

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O TxF está disponível a partir do Windows Vista.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                    | Descrição                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Sobre](about-transactional-ntfs.md)<br/>         | Informações gerais sobre o NTFS Transacional.<br/>                                                   |
| [Referência](transactional-ntfs-reference.md)<br/> | Documentação para as funções, estruturas de dados, enumerações e outros elementos de programação.<br/> |



 

 

