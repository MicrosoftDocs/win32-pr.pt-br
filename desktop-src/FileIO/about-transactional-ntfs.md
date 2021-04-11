---
description: O NTFS Transacional (TxF) integra as transações no sistema de arquivos NTFS, o que torna mais fácil para os desenvolvedores e administradores de aplicativos lidar normalmente com erros e preservar a integridade dos dados.
ms.assetid: 52341315-0412-4a87-aca0-9adea7aae62f
title: Sobre o NTFS Transacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf8cd99dfb1ff18ef7da88d3b3c7b0a647417e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296377"
---
# <a name="about-transactional-ntfs"></a>Sobre o NTFS Transacional

\[A Microsoft recomenda enfaticamente que os desenvolvedores utilizem meios alternativos para atender às necessidades do seu aplicativo. Muitos cenários para os quais o TxF foi desenvolvido podem ser obtidos por meio de técnicas mais simples e mais prontamente disponíveis. Além disso, o TxF pode não estar disponível em versões futuras do Microsoft Windows. Para obter mais informações e alternativas para o TxF, consulte [alternativas para usar o NTFS Transacional](deprecation-of-txf.md).\]

O NTFS Transacional (TxF) integra as transações no sistema de arquivos NTFS, o que torna mais fácil para os desenvolvedores e administradores de aplicativos lidar normalmente com erros e preservar a integridade dos dados.

O TxF pode participar de transações distribuídas que o [Coordenador de transações distribuídas (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) coordena, que permite que você use o TxF para o seguinte:

-   Transações que abrangem vários repositórios de dados, por exemplo, uma única transação para operações de arquivo e SQL
-   Transações que abrangem vários computadores, por exemplo, uma única transação para atualizações de arquivo em vários computadores

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                 | Descrição                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Quando usar o NTFS Transacional](when-to-use-transactional-ntfs.md)<br/>                                       | Use o NTFS transacional para manter a integridade dos dados.<br/>                                                                        |
| [Implantando o NTFS Transacional](deploying-transactional-ntfs.md)<br/>                                           | Controle de cache em NTFS Transacional.<br/>                                                                                    |
| [Como usar o NTFS Transacional](how-to-use-transactional-ntfs.md)<br/>                                         | Gerenciando identificadores de arquivo transacionais em NTFS Transacional.<br/>                                                                   |
| [Conceitos básicos do TxF](txf-basic-concepts.md)<br/>                                                               | Descreve a consistência de leitura confirmada, isolamento de confirmação de leitura e conceitos de bloqueio transacional em NTFS Transacional.<br/> |
| [Considerações de programação para NTFS Transacional](programming-considerations-for-transacted-fileio-.md)<br/> | Descreve várias considerações de programação para NTFS Transacional.<br/>                                                      |
| [Considerações de desempenho para NTFS Transacional](performance-considerations-for-transactional-ntfs.md)<br/> | Recomendações para transações de sistema de arquivos ideais.<br/>                                                                     |



 

 

