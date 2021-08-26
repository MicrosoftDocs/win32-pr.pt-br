---
title: Restauração do Sistema
description: Define pontos de restauração do sistema e monitora as principais alterações do sistema de um programa para habilitar uma reversões do sistema para um estado anterior. Escreva o código de recuperação automática ou o script wmi para restaurar o estado do sistema para um ponto de restauração registrado.
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- Restauração do Sistema
- Restauração do Sistema, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4472806aa2c0b6f8a29cc4e687d16e262639a66c65bda37fdca970c6c38b656f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111286"
---
# <a name="system-restore"></a>Restauração do Sistema

## <a name="purpose"></a>Finalidade

Restauração do Sistema monitora e registra automaticamente as principais alterações do sistema no computador do usuário. Ele foi projetado para reduzir os custos de suporte e aumentar a satisfação do cliente, permitindo que um usuário desfaça uma alteração que possa ter causado um problema com o sistema ou revertido para um dia em que o sistema estava com um desempenho ideal.

> [!Note]  
> A documentação a seguir é direcionada para desenvolvedores. Se você for um usuário final que procura informações sobre como usar Restauração do Sistema, confira [O que é Restauração do Sistema?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)

 

## <a name="developer-audience"></a>Público de desenvolvedores

A API Restauração do Sistema é projetada para uso por programadores C/C++. Uma familiaridade com Windows WMI (Instrumentação de Gerenciamento) é necessária para usar a interface de script.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

A API Restauração do Sistema é suportada em sistemas operacionais cliente a partir do Windows XP. Para obter informações sobre quais sistemas operacionais são necessários para usar um elemento de API específico, consulte a seção Requisitos de sua documentação.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                | Descrição                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [Visão geral](about-system-restore.md)<br/>      | Uma visão geral de como Restauração do Sistema funciona.<br/>                            |
| [Referência](system-restore-reference.md)<br/> | Documentação Restauração do Sistema funções, estruturas e classes.<br/> |
| [Amostras](using-system-restore.md)<br/>       | Um programa de exemplo escrito em C.<br/>                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[WMI](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

