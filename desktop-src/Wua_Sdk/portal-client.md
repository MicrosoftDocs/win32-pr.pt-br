---
description: A API do WUA (Agente de Atualização do Windows) é um conjunto de interfaces COM que permitem que os administradores e programadores do sistema acessem o WSUS (Windows Update e Windows Server Update Services).
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: Windows ATUALIZAR API do Agente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82e7e2c79a707424128082f8f3123cb5fff506a9fc98203ab1fdf8063393310d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737998"
---
# <a name="windows-update-agent-api"></a>Windows ATUALIZAR API do Agente

## <a name="purpose"></a>Finalidade

A API do WUA (Agente de Atualização do Windows) é um conjunto de interfaces COM que permitem que os administradores e programadores do sistema acessem Windows Update [and Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)). Scripts e programas podem ser escritos para examinar quais atualizações estão disponíveis no momento para um computador e, em seguida, você pode instalar ou desinstalar atualizações.

## <a name="where-applicable"></a>Quando aplicável

Os administradores do sistema podem usar WUA para determinar programaticamente quais atualizações devem ser aplicadas a um computador, baixar essas atualizações e instalá-las com pouca ou nenhuma intervenção do usuário.

Fornecedores independentes de software (ISV) e desenvolvedores de usuário final podem integrar recursos WUA ao gerenciamento de computadores ou ao software de gerenciamento de atualizações para fornecer um ambiente operacional contínuo.

## <a name="developer-audience"></a>Público de desenvolvedores

Você pode escrever aplicativos WUA em várias linguagens de programação. O WUA define interfaces e objetos acessíveis de Visual Basic, Visual Basic VBScript (Scripting Edition), JScript e de C e C++. Uma familiaridade com a programação COM é útil para o programador WUA.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O WUA tem suporte a partir do Windows XP. O WUA tem suporte no servidor a partir do Windows Server 2003.

## <a name="in-this-section"></a>Nesta seção

-   [Usando a API Windows Update Agent](using-the-windows-update-agent-api.md)
-   [Referência da API WUA](windows-update-agent--wua--api-reference.md)

 

 
