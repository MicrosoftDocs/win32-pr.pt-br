---
description: A Microsoft. Windows. O objeto ActCtx faz referência a manifestos e fornece uma maneira de os mecanismos de script acessarem assemblies lado a lado. A Microsoft. Windows. O objeto ActCtx pode ser usado para criar uma instância de um assembly lado a lado com componentes COM.
ms.assetid: 818e175e-2c58-4c44-87ce-4e97352fc3f3
title: Microsoft. Windows. Objeto ActCtx
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
ms.openlocfilehash: 7e84eadbc7489ddd91c34c0c9494515e89205849829625e850ad31dce3e92fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141999"
---
# <a name="microsoftwindowsactctx-object"></a>Microsoft. Windows. Objeto ActCtx

O **Microsoft.Windows. O objeto ActCtx** faz referência a manifestos e fornece uma maneira de os mecanismos de script acessarem assemblies lado a lado. O **Microsoft.Windows. O objeto ActCtx** pode ser usado para criar uma instância de um assembly lado a lado com componentes COM.

O **Microsoft.Windows. O objeto ActCtx** vem como um assembly no Windows Server 2003. Ele também pode ser instalado por aplicativos que usam o instalador Windows para instalação e o incluem como um módulo de mesclagem em seu pacote de instalação.

## <a name="members"></a>Membros

O **Microsoft.Windows. O objeto ActCtx** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **Microsoft.Windows. O objeto ActCtx** tem esses métodos.



| Método                               | Descrição                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [**Createobject**](createobject.md) | Cria um objeto no contexto do manifesto atual.<br/>            |
| [**Getobject**](getobject.md)       | Obtém uma instância de um **Microsoft.Windows. Objeto ActCtx.**<br/> |



 

### <a name="properties"></a>Propriedades

O **Microsoft.Windows. O objeto ActCtx** tem essas propriedades.



| Propriedade                                | Tipo de acesso          | Descrição                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [**Manifesto**](manifest.md)<br/> | Somente leitura<br/> | Obtém o contexto de ativação ativa.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |



 

 




