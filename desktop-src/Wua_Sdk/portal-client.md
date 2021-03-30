---
description: A API do WUA (agente de Windows Update) é um conjunto de interfaces COM que permitem que os administradores de sistema e os programadores acessem o Windows Update e o Windows Server Update Services (WSUS).
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: API do agente de Windows Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c34cb76619c9739c84e650a32590fdc4f61022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646774"
---
# <a name="windows-update-agent-api"></a>API do agente de Windows Update

## <a name="purpose"></a>Finalidade

A API do WUA (agente de Windows Update) é um conjunto de interfaces COM que permitem que os administradores de sistema e os programadores acessem o Windows Update e o [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)). Scripts e programas podem ser escritos para examinar quais atualizações estão disponíveis no momento para um computador e, em seguida, você pode instalar ou desinstalar atualizações.

## <a name="where-applicable"></a>Quando aplicável

Os administradores do sistema podem usar o WUA para determinar programaticamente quais atualizações devem ser aplicadas a um computador, baixar essas atualizações e instalá-las com pouca ou nenhuma intervenção do usuário.

ISVs (fornecedores independentes de software) e desenvolvedores de usuários finais podem integrar recursos do WUA ao gerenciamento do computador ou ao software de gerenciamento de atualizações para fornecer um ambiente operacional perfeitamente integrado.

## <a name="developer-audience"></a>Público de desenvolvedores

Você pode escrever aplicativos WUA em várias linguagens de programação. O WUA define interfaces e objetos que são acessíveis de Visual Basic, Visual Basic Scripting Edition (VBScript), JScript e de C e C++. Uma familiaridade com a programação COM é útil para o programador do WUA.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O WUA tem suporte a partir do Windows XP. O WUA tem suporte no servidor a partir do Windows Server 2003.

## <a name="in-this-section"></a>Nesta seção

-   [Usando a API do agente de Windows Update](using-the-windows-update-agent-api.md)
-   [Referência da API do WUA](windows-update-agent--wua--api-reference.md)

 

 
