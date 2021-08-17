---
title: Interface IRDVTaskPlugin
description: A interface IRDVTaskPlugin é implementada por um agente de tarefa de atualização de máquina virtual para permitir que o agente de tarefa gerencie atualizações do sistema para uma máquina virtual.
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- Interface IRDVTaskPlugin Serviços de Área de Trabalho Remota
- Interface IRDVTaskPlugin Serviços de Área de Trabalho Remota , descrita
topic_type:
- apiref
api_name:
- IRDVTaskPlugin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe76f0b0b92286d5a4b7db5126706fd55bdb6f580c11fda1dcaa55a47be4678c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129165"
---
# <a name="irdvtaskplugin-interface"></a>Interface IRDVTaskPlugin

A interface **IRDVTaskPlugin** é implementada  por um agente de tarefa de atualização de máquina virtual para permitir que o agente de tarefa gerencie atualizações do sistema para uma máquina virtual. Essa interface é usada pelo agente *de gatilho*, que é implementado pelo sistema host.

## <a name="members"></a>Membros

A interface **IRDVTaskPlugin** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IRDVTaskPlugin** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IRDVTaskPlugin** tem esses métodos.



| Método                                          | Descrição                                                        |
|:------------------------------------------------|:-------------------------------------------------------------------|
| [**Inicializar**](irdvtaskplugin-initialize.md) | Chamado para inicializar o agente de tarefa.<br/>                    |
| [**StartTask**](irdvtaskplugin-starttask.md)   | Chamado para iniciar a tarefa de atualização na máquina virtual.<br/> |
| [**Encerrar**](irdvtaskplugin-terminate.md)   | Chamado quando o agente de tarefa está sendo desligado.<br/>          |



 

### <a name="properties"></a>Propriedades

A interface **IRDVTaskPlugin** tem essas propriedades.



| Propriedade                                                   | Tipo de acesso          | Descrição                                             |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------|
| [**PluginName**](irdvtaskplugin-pluginname.md)<br/> | Somente leitura<br/> | Contém o nome de exibição do agente de tarefa.<br/> |



 

## <a name="remarks"></a>Comentários

O agente de tarefa é executado na máquina virtual quando essa máquina virtual está agendada para uma atualização do sistema. O agente de tarefa atualiza a máquina virtual quando o [**método StartTask**](irdvtaskplugin-starttask.md) é chamado.

Para registrar o agente de tarefa, adicione a seguinte chave ao registro da máquina virtual:

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows NT** Plug-ins de tarefa do servidor do terminal \\ **CurrentVersion** \\  \\  \\  \\ **TaskAgentName**

Nessa chave do Registro, adicione os seguintes valores:



| Nome                     | Tipo                      | Descrição                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| **Clsid**<br/>     | **REG \_ SZ**<br/>    | Uma cadeia de caracteres que **representa o CLSID** do agente de tarefa.<br/>          |
| **IsEnabled**<br/> | **REG \_ DWORD**<br/> | 0 se o agente de tarefa estiver desabilitado ou 1 se o agente de tarefa estiver habilitado.<br/> |



 

> [!Note]  
> Mais de um agente de tarefa pode ser registrado, mas apenas um agente de tarefa será usado. Se mais de um agente de tarefa estiver habilitado, somente o primeiro encontrado será usado.

 

Embora essa interface tenha suporte nos sistemas operacionais identificados nos Requisitos abaixo, ela só será usada se a máquina virtual estiver hospedada no Windows Server 2012.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/> |



 

