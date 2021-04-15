---
description: Se essa política do sistema por máquina estiver definida como 1, nenhum pacote no sistema obterá a funcionalidade de componente compartilhado habilitada pelo atributo msidbComponentAttributesShared na tabela de componentes.
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: DisableSharedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7a1d4c2bae3f499722890e06502c7a289e6921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501984"
---
# <a name="disablesharedcomponent"></a>DisableSharedComponent

Se essa [política do sistema](system-policy.md) por máquina estiver definida como 1, nenhum pacote no sistema obterá a funcionalidade de componente compartilhado habilitada pelo atributo **msidbComponentAttributesShared** na [tabela de componentes](component-table.md). O valor padrão é 0, que habilita a funcionalidade do componente compartilhado para componentes marcados com **msidbComponentAttributesShared** em todos os pacotes.

**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte. Essa função está disponível a partir do Windows Installer 4,5.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

 

 



