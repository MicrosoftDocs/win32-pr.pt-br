---
description: Se essa política de sistema por computador for definida como 1, nenhum pacote no sistema obtém a funcionalidade de componente compartilhado habilitada pelo atributo msidbComponentAttributesShared na tabela Componente.
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: DisableSharedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7576406e14b0f9ac48a26735b984302c2d765b784484022a85ec50244ee8df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143097"
---
# <a name="disablesharedcomponent"></a>DisableSharedComponent

Se essa política [](system-policy.md) de sistema por computador for definida como 1, nenhum pacote no sistema obtém a funcionalidade de componente compartilhado habilitada pelo atributo **msidbComponentAttributesShared** na tabela [Componente](component-table.md). O valor padrão é 0, que habilita a funcionalidade de componente compartilhado para componentes marcados com **msidbComponentAttributesShared** em todos os pacotes.

**[Windows Instalador 4.0 e anterior:](not-supported-in-windows-installer-4-0.md)** Sem suporte. Essa função está disponível a partir do Windows Installer 4.5.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ Instalador \_ do** Microsoft machine \\ **software** \\ **policies** \\  \\ **Windows** \\ **LOCAL** MACHINE

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

 

 



