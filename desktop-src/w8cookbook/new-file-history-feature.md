---
title: Novo recurso de histórico de arquivo
description: Novo recurso de histórico de arquivo
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70aad84f4d052d6a872c7b0cfc979d0fa05cb84
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104084958"
---
# <a name="new-file-history-feature"></a>Novo recurso de histórico de arquivo

## <a name="platform"></a>Plataforma

**Clientes** – Windows 8 


## <a name="description"></a>Descrição

O novo recurso de histórico de arquivo substitui a função de backup e restauração existente e oferece proteção para arquivos de usuário armazenados em bibliotecas de usuário. É fornecido um conjunto de APIs que permite aos desenvolvedores habilitar programaticamente o histórico de arquivos e selecionar um destino de armazenamento específico. A documentação para essas APIs está disponível no MSDN.

Ele pode afetar os fluxos de trabalho relacionados à proteção e à documentação dos dados que dependem do recurso de backup e restauração do Windows.

Não recomendamos o uso de ambos os recursos ao mesmo tempo. O histórico de arquivos verifica se um agendamento de backup existe e se está ativo e se encontra um, ele não permitirá que os usuários o ativem. Nesse caso, os usuários que desejarem usar o histórico de arquivos precisarão excluir o agendamento de backup do Windows.

## <a name="manifestation"></a>Manifestação

Os fluxos de trabalho podem ser interrompidos e a documentação do método anterior para acessar o recurso de backup e restauração do Windows precisará ser atualizada para refletir essas alterações.

## <a name="solution"></a>Solução

Revisar aplicativos que contêm fluxos de trabalho que são afetados negativamente pelo novo recurso de histórico de arquivo para remover conflitos e incorporar o novo conjunto de APIs.

## <a name="tests"></a>Testes

A API permite que os desenvolvedores determinem se o histórico de arquivos está ativado.

 

 




