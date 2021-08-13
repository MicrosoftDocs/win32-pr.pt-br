---
description: As funções de caixa de diálogo específicas do provedor permitem que um provedor exiba e manipule informações específicas da rede alterando caixas de diálogo do sistema ou exibindo caixas de diálogo personalizadas.
ms.assetid: c9a52867-0a0b-40d8-a09d-2b7bed517e13
title: Funções da caixa de diálogo Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d31a38f09dd0e0806fe21f491d02b5e18fe0abb1e5a181e40f0ab6370280b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920573"
---
# <a name="provider-specific-dialog-box-functions"></a>Funções da caixa de diálogo Provider-Specific

As funções de caixa de diálogo específicas do provedor permitem que um provedor exiba e manipule informações específicas da rede alterando caixas de diálogo do sistema ou exibindo caixas de diálogo personalizadas.

As funções da caixa de diálogo a seguir adicionam botões à caixa de diálogo **Propriedades** do Gerenciador de arquivos. Em seguida, o provedor pode manipular os eventos desses botões para executar tarefas específicas da rede. Observe que há um limite para o número de botões que podem ser adicionados. Por isso, os provedores devem usar essa funcionalidade com moderação. Além disso, um provedor pode não conseguir adicionar um botão porque o espaço disponível já foi usado por outros provedores. Um provedor de rede deve lidar com essa situação.



| Função                                           | Descrição                                                                                                                             |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)     | Determina os nomes dos botões adicionados a uma caixa de diálogo de propriedade para um recurso específico.<br/>                                      |
| [**NPPropertyDialog**](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)       | Chamado quando um usuário clica em um botão adicionado usando a função [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) .<br/>               |
| [**NPSearchDialog**](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)           | Permite que os provedores de rede implementem sua própria funcionalidade de pesquisa além da fornecida na caixa de diálogo de **conexão** .<br/> |
| [**NPFormatNetworkName**](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname) | Permite que os provedores de rede formatem ou modifiquem nomes de rede antes de serem apresentados ao usuário.<br/>                 |



 

 

 




