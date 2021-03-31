---
description: O objeto Microsoft. Windows. ActCtx faz referência a manifestos e fornece uma maneira para os mecanismos de script acessarem assemblies lado a lado. O objeto Microsoft. Windows. ActCtx pode ser usado para criar uma instância de um assembly lado a lado com componentes COM.
ms.assetid: 818e175e-2c58-4c44-87ce-4e97352fc3f3
title: Objeto Microsoft. Windows. ActCtx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Microsoft.Windows.ActCtx
api_type:
- COM
api_location: ''
ms.openlocfilehash: 58290ec9d36d8e8428000422d0e1014335870149
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827936"
---
# <a name="microsoftwindowsactctx-object"></a>Objeto Microsoft. Windows. ActCtx

O objeto **Microsoft. Windows. ActCtx** faz referência a manifestos e fornece uma maneira para os mecanismos de script acessarem assemblies lado a lado. O objeto **Microsoft. Windows. ActCtx** pode ser usado para criar uma instância de um assembly lado a lado COM componentes com.

O objeto **Microsoft. Windows. ActCtx** é fornecido como um assembly no Windows Server 2003. Ele também pode ser instalado por aplicativos que usam o Windows Installer para instalação e o incluem como um módulo de mesclagem em seu pacote de instalação.

## <a name="members"></a>Membros

O objeto **Microsoft. Windows. ActCtx** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **Microsoft. Windows. ActCtx** tem esses métodos.



| Método                               | Descrição                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [**CreateObject**](createobject.md) | Cria um objeto no contexto do manifesto atual.<br/>            |
| [**GetObject**](getobject.md)       | Obtém uma instância de um objeto **Microsoft. Windows. ActCtx** existente.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **Microsoft. Windows. ActCtx** tem essas propriedades.



| Propriedade                                | Tipo de acesso          | Descrição                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [**Manifesto**](manifest.md)<br/> | Somente leitura<br/> | Obtém o contexto de ativação ativa.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



 

 




