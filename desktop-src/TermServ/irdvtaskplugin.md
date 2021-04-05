---
title: Interface IRDVTaskPlugin
description: A interface IRDVTaskPlugin é implementada por um agente de tarefa de atualização de máquina virtual para permitir que o agente de tarefa gerencie atualizações do sistema para uma máquina virtual.
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IRDVTaskPlugin
- Serviços de Área de Trabalho Remota da interface IRDVTaskPlugin, descrita
topic_type:
- apiref
api_name:
- IRDVTaskPlugin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59e90e899e8084f7fbc6b0b6f11067061eaa807b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919134"
---
# <a name="irdvtaskplugin-interface"></a>Interface IRDVTaskPlugin

A interface **IRDVTaskPlugin** é implementada por um agente de *tarefa* de atualização de máquina virtual para permitir que o agente de tarefa gerencie atualizações do sistema para uma máquina virtual. Essa interface é usada pelo *agente de gatilho*, que é implementado pelo sistema host.

## <a name="members"></a>Membros

A interface **IRDVTaskPlugin** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IRDVTaskPlugin** também tem estes tipos de membros:

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

O agente de tarefa é executado na máquina virtual quando essa máquina virtual está agendada para uma atualização do sistema. O agente de tarefa atualiza a máquina virtual quando o método [**StartTask**](irdvtaskplugin-starttask.md) é chamado.

Para registrar o agente de tarefa, adicione a seguinte chave ao registro da máquina virtual:

**HKEY \_ Software do \_ computador local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Terminal Server** \\ plugins da **tarefa** \\  \\ **TaskAgentName**

Nessa chave do registro, adicione os seguintes valores:



| Nome                     | Tipo                      | Descrição                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| **CLSID**<br/>     | **REG \_ sz**<br/>    | Uma cadeia de caracteres que representa o **CLSID** do agente de tarefa.<br/>          |
| **IsEnabled**<br/> | **REG \_ DWORD**<br/> | 0 se o agente de tarefa estiver desabilitado ou 1 se o agente de tarefa estiver habilitado.<br/> |



 

> [!Note]  
> Mais de um agente de tarefa pode ser registrado, mas apenas um agente de tarefa será usado. Se mais de um agente de tarefa estiver habilitado, somente o primeiro encontrado será usado.

 

Embora essa interface tenha suporte nos sistemas operacionais identificados nos requisitos abaixo, ela só será usada se a máquina virtual estiver hospedada no Windows Server 2012.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/> |



 

