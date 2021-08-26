---
title: Novo Histórico de Arquivos recurso
description: Novo Histórico de Arquivos recurso
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1502450c1376a57f9de99badc5188c8ce07761e0c28ae3ac2245a84437b5e66d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932186"
---
# <a name="new-file-history-feature"></a>Novo Histórico de Arquivos recurso

## <a name="platform"></a>Plataforma

**Clientes** – Windows 8 


## <a name="description"></a>Descrição

O novo Histórico de Arquivos substitui a função de Backup e Restauração existente e oferece proteção para arquivos de usuário armazenados em bibliotecas de usuário. Um conjunto de APIs é fornecido que permite aos desenvolvedores habilitar programaticamente Histórico de Arquivos e selecionar um destino de armazenamento específico. A documentação dessas APIs está disponível no MSDN.

Isso pode afetar os fluxos de trabalho relacionados à proteção de dados e à documentação que dependem do recurso Backup do Windows e Restauração.

Não recomendamos o uso de ambos os recursos ao mesmo tempo. Histórico de Arquivos verifica se um agendamento de Backup existe e se está ativo e se encontra um, ele não permitirá que os usuários o a liguem. Nesse caso, os usuários que quiserem usar Histórico de Arquivos terão que excluir a agenda Backup do Windows dados.

## <a name="manifestation"></a>Manifestação

Os fluxos de trabalho podem ser interrompidos e a documentação do método anterior para acessar o Backup do Windows e o recurso De restauração precisarão ser atualizados para refletir essas alterações.

## <a name="solution"></a>Solução

Revise os aplicativos que contêm fluxos de trabalho que são afetados negativamente pelo novo recurso Histórico de Arquivos para remover conflitos e incorporar o novo conjunto de APIs.

## <a name="tests"></a>Testes

A API permite que os desenvolvedores determinem se Histórico de Arquivos está ligado.

 

 




