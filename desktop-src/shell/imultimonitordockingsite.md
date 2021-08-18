---
description: Implementado pelo navegador. expõe métodos que gerenciam qual monitor contém a barra de tarefas Windows em um sistema de vários monitores.
title: Interface IMultiMonitorDockingSite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite
api_type:
- COM
api_location: ''
ms.assetid: af9a7a9e-bd7c-4b17-9cb6-008df5c820d8
ms.openlocfilehash: a5a17e8206af8f0821833f4b2ea250606de29b6fbe74b7a29ced6c5b5dc13ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458216"
---
# <a name="imultimonitordockingsite-interface"></a>Interface IMultiMonitorDockingSite

Implementado pelo navegador. expõe métodos que gerenciam qual monitor contém a barra de tarefas Windows em um sistema de vários monitores.

## <a name="members"></a>Membros

A interface **IMultiMonitorDockingSite** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMultiMonitorDockingSite** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IMultiMonitorDockingSite** tem esses métodos.



| Método                                                            | Descrição                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**Getmonitor**](imultimonitordockingsite-getmonitor.md)         | Obtém o monitor padrão atual.<br/>                                               |
| [**RequestMonitor**](imultimonitordockingsite-requestmonitor.md) | Verifica se o monitor está ativo e disponível.<br/>                              |
| [**Setmonitor**](imultimonitordockingsite-setmonitor.md)         | Altera qual monitor é usado para barras de ferramentas encaixadas em um sistema de vários monitores.<br/> |



 

## <a name="remarks"></a>Comentários

Normalmente, você não implementa a interface **IMultiMonitorDockingSite** . O navegador de shell implementa essa interface para dar suporte a vários monitores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/> |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                   |



 

 
