---
title: Restauração do Sistema
description: Define pontos de restauração do sistema e monitora as principais alterações do sistema de um programa para permitir a reversão do sistema para um estado anterior. Grave código de recuperação automática ou script WMI para restaurar o estado do sistema para um ponto de restauração registrado.
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- Restauração do Sistema
- Restauração do sistema, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bdc4555171ad867f6e6b925144d9ed673ffc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084690"
---
# <a name="system-restore"></a>Restauração do Sistema

## <a name="purpose"></a>Finalidade

A restauração do sistema monitora e registra automaticamente as principais alterações do sistema no computador de um usuário. Ele foi projetado para reduzir os custos de suporte e aumentar a satisfação do cliente, permitindo que um usuário desfaça uma alteração que possa ter causado um problema com o sistema ou reverta para um dia em que o sistema estava sendo executado de forma ideal.

> [!Note]  
> A documentação a seguir destina-se a desenvolvedores. Se você for um usuário final procurando informações sobre como usar a restauração do sistema, consulte [o que é a restauração do sistema?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)

 

## <a name="developer-audience"></a>Público de desenvolvedores

A API de restauração do sistema foi projetada para uso por programadores C/C++. Uma familiaridade com o Instrumentação de Gerenciamento do Windows (WMI) é necessária para usar a interface de script.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

A API de restauração do sistema tem suporte em sistemas operacionais cliente que começam com o Windows XP. Para obter informações sobre quais sistemas operacionais são necessários para usar um elemento de API específico, consulte a seção requisitos de sua documentação.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                | Descrição                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [Visão geral](about-system-restore.md)<br/>      | Uma visão geral de como funciona a restauração do sistema.<br/>                            |
| [Referência](system-restore-reference.md)<br/> | Documentação das funções, estruturas e classes de restauração do sistema.<br/> |
| [Amostras](using-system-restore.md)<br/>       | Um programa de exemplo escrito em C.<br/>                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[WMI](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

